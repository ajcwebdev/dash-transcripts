---
showLink: "https://www.youtube.com/watch?v=mPshY2tTMKk"
channel: "Dash Incubator"
channelURL: "https://www.youtube.com/@dashincubator"
title: "[audio @ 2:27:00] $DASH Code Hangout: HD Key Dev Tools #7: Node Buffer ️to Uint8Array & ArrayBuffers"
publishDate: "2023-01-27"
coverImage: "https://i.ytimg.com/vi/mPshY2tTMKk/maxresdefault.jpg"
---

## Episode Description

A developer works on converting an HD key library to use Uint8Array instead of Node.js Buffers, making it async-compatible and browser-friendly.

## Episode Summary

In this lengthy coding session, the developer tackles the challenge of updating an HD key library to use Uint8Array instead of Node.js Buffers, with the goal of making it async-compatible and browser-friendly. The process involves refactoring code, updating dependencies, and ensuring compatibility across different Node.js versions. Key tasks include replacing Buffer operations with Uint8Array equivalents, converting synchronous functions to async, and addressing crypto-related functions. The developer encounters and resolves various issues, including text encoding, HMAC implementation, and tweaking functions. Despite some setbacks, including initial audio issues, significant progress is made towards creating a more versatile and browser-compatible library.

## Chapters

00:00 - Introduction and Initial Setup

The developer begins the session, explaining the goal of converting an HD key library to use Uint8Array instead of Node.js Buffers. They set up the development environment and start reviewing the existing code.

27:00 - Refactoring Buffer Operations to Uint8Array

The developer begins the process of replacing Buffer operations with Uint8Array equivalents. This involves careful consideration of different methods for copying, setting, and manipulating data in Uint8Array format.

59:00 - Addressing Crypto Functions and Dependencies

Focus shifts to updating crypto-related functions and dependencies. The developer explores options for implementing HMAC and other cryptographic operations using Web Crypto API and discusses potential browser compatibility issues.

145:02 - Discovering and Fixing Audio Issues

The developer realizes the stream has been running without audio for a significant portion of time. They address the issue and summarize what has been covered so far.

148:18 - Continuing Refactoring and Testing

Work resumes on refactoring the library, with a focus on ensuring all functions work correctly with the new Uint8Array implementation. The developer runs tests and debugs issues as they arise.

215:15 - Converting Functions to Async

The developer begins the process of converting synchronous functions to async, preparing the library for better compatibility with browser environments and modern JavaScript practices.

263:37 - Final Testing and Cleanup

The session concludes with final testing of the refactored library. The developer addresses remaining issues, discusses future steps for improving browser compatibility, and considers updating dependencies to their latest versions.

## Transcript

[00:00] you
[00:02] you
[00:04] you
[00:06] you
[00:08] you
[00:10] you
[00:12] you
[00:14] you
[00:16] you
[00:18] you
[00:20] you
[00:22] you
[00:24] you
[00:26] you
[00:28] you
[00:30] you
[00:32] you
[00:35] you
[00:37] you
[00:39] you
[00:41] you
[00:43] you
[00:45] you
[00:47] you
[00:49] you
[00:51] you
[00:53] you
[00:55] you
[00:57] you
[00:59] you
[01:01] you
[01:03] you
[01:05] you
[01:07] you
[01:10] you
[01:12] you
[01:14] you
[01:16] you
[01:18] you
[01:20] you
[01:22] you
[01:24] you
[01:26] you
[01:28] you
[01:30] you
[01:32] you
[01:34] you
[01:36] you
[01:38] you
[01:40] you
[01:43] you
[01:45] you
[01:47] you
[01:49] you
[01:51] you
[01:53] you
[01:55] you
[01:57] you
[01:59] you
[02:01] you
[02:03] you
[02:05] you
[02:07] you
[02:09] you
[02:11] you
[02:13] you
[02:15] you
[02:18] you
[02:20] you
[02:22] you
[02:24] you
[02:26] you
[02:28] you
[02:30] you
[02:32] you
[02:34] you
[02:36] you
[02:38] you
[02:40] you
[02:42] you
[02:44] you
[02:46] you
[02:48] you
[02:50] you
[02:53] you
[02:55] you
[02:57] you
[02:59] you
[03:01] you
[03:03] you
[03:05] you
[03:07] you
[03:09] you
[03:11] you
[03:13] you
[03:15] you
[03:17] you
[03:20] you
[03:22] you
[03:24] you
[03:27] you
[03:29] you
[03:31] you
[03:33] you
[03:35] you
[03:37] you
[03:39] you
[03:41] you
[03:43] you
[03:46] you
[03:48] you
[03:54] you
[04:06] you
[04:08] you
[04:18] you
[04:28] you
[04:30] you
[04:32] you
[04:42] you
[04:52] you
[04:54] you
[05:04] you
[05:14] you
[05:16] you
[05:18] you
[05:28] you
[05:31] you
[05:34] you
[05:36] you
[05:39] you
[05:42] you
[05:44] you
[05:52] you
[05:54] you
[06:04] you
[06:14] you
[06:16] you
[06:22] you
[06:30] you
[06:47] you
[06:49] you
[06:59] you
[07:09] you
[07:11] you
[07:17] you
[07:29] you
[07:31] you
[07:36] you
[07:46] you
[08:03] you
[08:05] you
[08:10] you
[08:20] you
[08:37] you
[08:39] you
[08:49] you
[08:59] you
[09:01] you
[09:15] you
[09:33] you
[09:35] you
[09:41] you
[09:47] you
[09:54] you
[10:01] you
[10:03] you
[10:18] you
[10:43] you
[10:45] you
[10:55] you
[11:05] you
[11:07] you
[11:17] you
[11:27] you
[11:29] you
[11:35] you
[11:45] you
[11:47] you
[12:03] you
[12:05] you
[12:21] you
[12:23] you
[12:43] you
[12:45] you
[12:55] you
[13:05] you
[13:07] you
[13:23] you
[13:25] you
[13:43] you
[13:45] you
[14:03] you
[14:05] you
[14:15] you
[14:17] you
[14:27] you
[14:37] you
[14:40] you
[14:50] you
[14:52] you
[15:02] you
[15:12] you
[15:14] you
[15:34] you
[15:36] you
[15:46] you
[15:56] you
[15:58] you
[16:12] you
[16:14] you
[16:24] you
[16:34] you
[16:36] you
[16:47] you
[16:49] you
[17:00] you
[17:02] you
[17:13] you
[17:15] you
[17:17] you
[17:37] you
[17:39] you
[17:49] you
[17:59] you
[18:01] you
[18:11] you
[18:13] you
[18:27] you
[18:29] you
[18:47] you
[18:49] you
[19:03] you
[19:20] you
[19:23] you
[19:37] you
[19:39] you
[19:49] you
[19:59] you
[20:01] you
[20:11] you
[20:23] you
[20:25] you
[20:35] you
[20:37] you
[20:47] you
[20:49] you
[21:09] you
[21:11] you
[21:21] you
[21:23] you
[21:33] you
[21:35] you
[21:45] you
[21:47] you
[21:57] you
[21:59] you
[22:15] you
[22:17] you
[22:19] you
[22:21] you
[22:35] you
[22:37] you
[22:39] you
[22:49] you
[22:51] you
[22:54] you
[23:02] you
[23:14] you
[23:16] you
[23:26] you
[23:28] you
[23:38] you
[23:40] you
[23:56] you
[23:58] you
[24:08] you
[24:10] you
[24:12] you
[24:22] you
[24:32] you
[24:34] you
[24:44] you
[24:46] you
[25:11] you
[25:13] you
[25:15] you
[25:28] you
[25:30] you
[25:55] you
[25:57] you
[26:09] you
[26:11] you
[26:22] you
[26:25] you
[26:27] you
[26:32] you
[26:43] you
[26:46] you
[26:52] you
[27:05] you
[27:07] you
[27:17] you
[27:19] you
[27:33] you
[27:35] you
[27:51] you
[27:53] you
[27:55] you
[28:05] you
[28:07] you
[28:21] you
[28:23] you
[28:33] you
[28:35] you
[28:45] you
[28:55] you
[28:57] you
[29:07] you
[29:17] you
[29:19] you
[29:35] you
[29:37] you
[29:55] you
[29:57] you
[30:21] you
[30:23] you
[30:33] you
[30:45] you
[30:47] you
[30:57] you
[31:09] you
[31:11] you
[31:21] you
[31:23] you
[31:26] you
[31:46] you
[31:48] you
[31:58] you
[32:08] you
[32:10] you
[32:30] you
[32:32] you
[32:42] you
[32:52] you
[32:54] you
[33:04] you
[33:14] you
[33:16] you
[33:32] you
[33:34] you
[33:48] you
[33:50] you
[34:10] you
[34:12] you
[34:22] you
[34:32] you
[34:34] you
[34:54] you
[34:56] you
[35:14] you
[35:16] you
[35:30] you
[35:32] you
[35:42] you
[35:52] you
[35:54] you
[36:10] you
[36:12] you
[36:23] you
[36:25] you
[36:27] you
[36:37] you
[36:40] you
[36:42] you
[36:44] you
[36:46] you
[36:48] you
[36:50] you
[37:00] you
[37:10] you
[37:12] you
[37:14] you
[37:30] you
[37:32] you
[37:48] you
[37:50] you
[38:00] you
[38:02] you
[38:22] you
[38:24] you
[38:34] you
[38:36] you
[38:46] you
[38:48] you
[38:50] you
[39:00] you
[39:10] you
[39:12] you
[39:26] you
[39:29] you
[39:31] you
[39:41] you
[39:43] you
[39:45] you
[39:56] you
[39:58] you
[40:00] you
[40:11] you
[40:13] you
[40:15] you
[40:19] you
[40:25] you
[40:35] you
[40:37] you
[40:39] you
[40:49] you
[40:59] you
[41:01] you
[41:11] you
[41:13] you
[41:15] you
[41:31] you
[41:33] you
[41:47] you
[41:49] you
[41:51] you
[42:01] you
[42:11] you
[42:13] you
[42:23] you
[42:33] you
[42:36] you
[42:48] you
[42:50] you
[43:00] you
[43:02] you
[43:22] you
[43:24] you
[43:34] you
[43:36] you
[43:52] you
[43:54] you
[43:59] you
[44:10] you
[44:12] you
[44:28] you
[44:30] you
[44:40] you
[44:42] you
[45:02] you
[45:04] you
[45:14] you
[45:16] you
[45:32] you
[45:34] you
[45:50] you
[45:52] you
[46:08] you
[46:10] you
[46:12] you
[46:20] you
[46:32] you
[46:34] you
[46:36] you
[46:42] you
[46:52] you
[46:55] you
[47:05] you
[47:07] you
[47:09] you
[47:19] you
[47:29] you
[47:31] you
[47:51] you
[47:53] you
[48:13] you
[48:15] you
[48:25] you
[48:35] you
[48:37] you
[48:47] you
[48:57] you
[48:59] you
[49:09] you
[49:19] you
[49:21] you
[49:31] you
[49:33] you
[49:35] you
[49:37] you
[49:39] you
[49:41] you
[49:43] you
[49:45] you
[49:48] you
[49:50] you
[49:56] you
[50:06] you
[50:08] you
[50:10] you
[50:16] you
[50:26] you
[50:28] you
[50:48] you
[50:50] you
[51:02] you
[51:04] you
[51:24] you
[51:26] you
[51:46] you
[51:48] you
[51:58] you
[52:08] you
[52:10] you
[52:28] you
[52:30] you
[52:40] you
[52:42] you
[52:44] you
[52:50] you
[53:00] you
[53:02] you
[53:04] you
[53:14] you
[53:24] you
[53:26] you
[53:37] you
[53:39] you
[53:42] you
[53:48] you
[53:54] you
[54:01] you
[54:03] you
[54:19] you
[54:21] you
[54:31] you
[54:33] you
[54:43] you
[54:53] you
[54:55] you
[55:01] you
[55:15] you
[55:17] you
[55:33] you
[55:48] you
[55:55] you
[55:57] you
[56:13] you
[56:15] you
[56:25] you
[56:27] you
[56:37] you
[56:47] you
[56:49] you
[57:00] you
[57:02] you
[57:18] you
[57:20] you
[57:30] you
[57:40] you
[57:42] you
[57:48] you
[57:58] you
[58:00] you
[58:21] you
[58:23] you
[58:35] you
[58:45] you
[58:47] you
[58:56] you
[59:06] you
[59:09] you
[59:23] you
[59:25] you
[59:37] you
[59:47] you
[59:49] you
[59:59] you
[60:09] you
[60:11] you
[60:21] you
[60:23] you
[60:41] you
[60:43] you
[60:49] you
[60:59] you
[61:01] you
[61:11] you
[61:23] you
[61:25] you
[61:36] you
[61:38] you
[61:49] you
[61:51] you
[62:02] you
[62:04] you
[62:23] you
[62:25] you
[62:43] you
[62:45] you
[62:47] you
[63:05] you
[63:07] you
[63:13] you
[63:25] you
[63:27] you
[63:33] you
[63:43] you
[63:46] you
[63:48] you
[64:01] you
[64:03] you
[64:19] you
[64:21] you
[64:31] you
[64:33] you
[64:35] you
[64:41] you
[64:51] you
[64:53] you
[64:55] you
[65:01] you
[65:13] you
[65:15] you
[65:35] you
[65:37] you
[65:47] you
[65:49] you
[65:51] you
[65:57] you
[66:09] you
[66:11] you
[66:29] you
[66:31] you
[66:42] you
[66:44] you
[66:46] you
[67:05] you
[67:07] you
[67:17] you
[67:20] you
[67:39] you
[67:41] you
[67:51] you
[67:53] you
[68:11] you
[68:13] you
[68:15] you
[68:26] you
[68:29] you
[68:31] you
[68:39] you
[68:42] you
[68:44] you
[68:47] you
[68:50] you
[68:52] you
[69:11] you
[69:13] you
[69:18] you
[69:29] you
[69:31] you
[69:49] you
[69:51] you
[69:56] you
[70:07] you
[70:09] you
[70:19] you
[70:21] you
[70:35] you
[70:38] you
[70:49] you
[70:51] you
[70:53] you
[70:59] you
[71:05] you
[71:12] you
[71:14] you
[71:32] you
[71:34] you
[71:44] you
[71:54] you
[71:56] you
[72:07] you
[72:09] you
[72:27] you
[72:29] you
[72:47] you
[72:49] you
[72:51] you
[73:01] you
[73:11] you
[73:13] you
[73:29] you
[73:31] you
[73:41] you
[73:51] you
[73:53] you
[74:05] you
[74:07] you
[74:19] you
[74:21] you
[74:31] you
[74:41] you
[74:43] you
[74:53] you
[74:56] you
[75:06] you
[75:16] you
[75:18] you
[75:36] you
[75:38] you
[75:44] you
[75:56] you
[75:58] you
[76:18] you
[76:20] you
[76:30] you
[76:40] you
[76:42] you
[76:55] you
[76:57] you
[77:08] you
[77:10] you
[77:20] you
[77:30] you
[77:32] you
[77:42] you
[77:52] you
[77:54] you
[78:12] you
[78:14] you
[78:24] you
[78:34] you
[78:36] you
[78:50] you
[78:52] you
[79:02] you
[79:12] you
[79:14] you
[79:24] you
[79:26] you
[79:36] you
[79:46] you
[79:48] you
[80:08] you
[80:10] you
[80:20] you
[80:23] you
[80:25] you
[80:31] you
[80:41] you
[80:43] you
[81:03] you
[81:05] you
[81:23] you
[81:25] you
[81:27] you
[81:29] you
[81:35] you
[81:45] you
[81:47] you
[81:49] you
[81:59] you
[82:09] you
[82:11] you
[82:17] you
[82:27] you
[82:29] you
[82:39] you
[82:41] you
[82:51] you
[83:01] you
[83:03] you
[83:13] you
[83:23] you
[83:25] you
[83:35] you
[83:45] you
[83:47] you
[84:05] you
[84:07] you
[84:27] you
[84:29] you
[84:39] you
[84:42] you
[85:02] you
[85:04] you
[85:22] you
[85:24] you
[85:34] you
[85:36] you
[85:38] you
[85:40] you
[85:42] you
[85:44] you
[85:46] you
[85:56] you
[86:06] you
[86:08] you
[86:18] you
[86:20] you
[86:30] you
[86:32] you
[86:46] you
[86:48] you
[86:50] you
[87:00] you
[87:10] you
[87:12] you
[87:22] you
[87:32] you
[87:34] you
[87:40] you
[87:50] you
[87:53] you
[88:17] you
[88:19] you
[88:29] you
[88:39] you
[88:41] you
[89:01] you
[89:03] you
[89:14] you
[89:16] you
[89:27] you
[89:29] you
[89:31] you
[89:47] you
[89:49] you
[90:03] you
[90:05] you
[90:15] you
[90:17] you
[90:33] you
[90:35] you
[90:49] you
[90:51] you
[90:53] you
[91:03] you
[91:05] you
[91:07] you
[91:17] you
[91:19] you
[91:35] you
[91:37] you
[91:53] you
[91:56] you
[92:12] you
[92:14] you
[92:24] you
[92:26] you
[92:42] you
[92:44] you
[92:54] you
[92:56] you
[93:12] you
[93:14] you
[93:16] you
[93:26] you
[93:28] you
[93:38] you
[93:40] you
[93:49] you
[93:51] you
[93:54] you
[94:02] you
[94:10] you
[94:12] you
[94:22] you
[94:32] you
[94:34] you
[94:44] you
[94:54] you
[94:56] you
[95:06] you
[95:16] you
[95:18] you
[95:28] you
[95:38] you
[95:40] you
[95:46] you
[95:56] you
[95:58] you
[96:04] you
[96:10] you
[96:18] you
[96:20] you
[96:38] you
[96:41] you
[96:51] you
[97:01] you
[97:03] you
[97:13] you
[97:23] you
[97:25] you
[97:43] you
[97:45] you
[98:03] you
[98:05] you
[98:15] you
[98:25] you
[98:27] you
[98:37] you
[98:47] you
[98:49] you
[98:51] you
[98:53] you
[98:55] you
[98:57] you
[99:05] you
[99:17] you
[99:19] you
[99:21] you
[99:27] you
[99:37] you
[99:39] you
[99:41] you
[100:01.88] you
[100:03.94] you
[100:23.94] you
[100:26.00] you
[100:46.00] you
[100:48.06] you
[101:08.06] you
[101:10.12] you
[101:20.12] you
[101:22.18] you
[101:24.24] you
[101:34.24] you
[101:44.24] you
[101:46.30] you
[101:48.36] you
[101:54.36] you
[102:04.36] you
[102:06.42] you
[102:08.48] you
[102:20.48] you
[102:22.54] you
[102:32.54] you
[102:34.60] you
[102:44.60] you
[102:46.66] you
[102:48.72] you
[103:04.72] you
[103:06.78] you
[103:08.84] you
[103:14.84] you
[103:24.84] you
[103:26.90] you
[103:28.96] you
[103:38.96] you
[103:48.96] you
[103:51.02] you
[104:01.02] you
[104:03.08] you
[104:23.08] you
[104:25.14] you
[104:35.14] you
[104:37.20] you
[104:39.26] you
[104:49.26] you
[104:59.26] you
[105:01.32] you
[105:11.32] you
[105:13.38] you
[105:23.38] you
[105:25.44] you
[105:27.50] you
[105:43.50] you
[105:45.56] you
[106:05.56] you
[106:07.62] you
[106:17.62] you
[106:27.62] you
[106:29.68] you
[106:42.68] you
[106:44.74] you
[107:02.74] you
[107:04.80] you
[107:20.80] you
[107:22.86] you
[107:28.86] you
[107:38.86] you
[107:40.92] you
[107:46.92] you
[107:56.92] you
[107:58.98] you
[108:08.98] you
[108:11.04] you
[108:25.04] you
[108:27.10] you
[108:37.10] you
[108:39.16] you
[108:53.16] you
[108:55.22] you
[109:07.22] you
[109:09.28] you
[109:15.28] you
[109:25.28] you
[109:27.34] you
[109:37.34] you
[109:47.34] you
[109:49.40] you
[109:59.40] you
[110:01.46] you
[110:11.46] you
[110:21.46] you
[110:23.52] you
[110:25.58] you
[110:35.58] you
[110:45.58] you
[110:47.64] you
[110:57.64] you
[110:59.70] you
[111:17.70] you
[111:19.76] you
[111:31.76] you
[111:33.82] you
[111:43.82] you
[111:53.82] you
[111:55.88] you
[112:05.88] you
[112:07.94] you
[112:17.94] you
[112:20.00] you
[112:36.00] you
[112:38.06] you
[112:40.12] you
[112:56.12] you
[112:58.18] you
[113:14.18] you
[113:16.24] you
[113:26.24] you
[113:28.30] you
[113:42.30] you
[113:44.36] you
[114:00.36] you
[114:02.42] you
[114:18.42] you
[114:20.48] you
[114:22.54] you
[114:32.54] you
[114:34.60] you
[114:36.66] you
[114:50.66] you
[114:52.72] you
[115:04.72] you
[115:06.78] you
[115:16.78] you
[115:26.78] you
[115:28.84] you
[115:34.84] you
[115:44.84] you
[115:46.90] you
[116:06.90] you
[116:08.96] you
[116:18.96] you
[116:28.96] you
[116:31.02] you
[116:41.02] you
[116:51.02] you
[116:53.08] you
[116:55.14] you
[117:11.14] you
[117:13.20] you
[117:33.20] you
[117:35.26] you
[117:45.26] you
[117:47.32] you
[117:57.32] you
[117:59.38] you
[118:09.38] you
[118:19.38] you
[118:21.44] you
[118:31.44] you
[118:33.50] you
[118:51.50] you
[118:53.56] you
[118:55.62] you
[118:57.68] you
[119:03.68] you
[119:15.68] you
[119:17.74] you
[119:19.80] you
[119:25.80] you
[119:33.80] you
[119:35.86] you
[119:37.92] you
[119:47.92] you
[119:49.98] you
[119:59.98] you
[120:02.04] you
[120:08.04] you
[120:18.04] you
[120:20.10] you
[120:40.10] you
[120:42.16] you
[120:48.16] you
[120:56.16] you
[121:11.22] you
[121:13.28] you
[121:19.28] you
[121:31.28] you
[121:33.34] you
[121:43.34] you
[121:53.34] you
[121:55.40] you
[122:05.40] you
[122:15.40] you
[122:17.46] you
[122:23.46] you
[122:33.46] you
[122:55.52] you
[122:57.58] you
[123:07.58] you
[123:17.58] you
[123:19.64] you
[123:33.64] you
[123:50.70] you
[123:52.76] you
[124:04.76] you
[124:12.76] you
[124:14.82] you
[124:26.82] you
[124:28.88] you
[124:39.88] you
[124:48.88] you
[124:50.94] you
[125:03.94] you
[125:06.00] you
[125:16.00] you
[125:26.00] you
[125:28.06] you
[125:38.06] you
[125:48.06] you
[125:50.12] you
[126:08.12] you
[126:10.18] you
[126:16.18] you
[126:27.18] you
[126:29.24] you
[126:39.24] you
[126:41.30] you
[126:43.36] you
[126:45.42] you
[126:55.42] you
[126:57.48] you
[127:15.48] you
[127:17.54] you
[127:27.54] you
[127:29.60] you
[127:35.60] you
[127:43.60] you
[127:45.66] you
[128:05.66] you
[128:07.72] you
[128:25.72] you
[128:27.78] you
[128:51.78] you
[128:53.84] you
[129:13.84] you
[129:15.90] you
[129:25.90] you
[129:35.90] you
[129:37.96] you
[129:47.96] you
[129:57.96] you
[130:00.02] you
[130:12.02] you
[130:14.08] you
[130:16.14] you
[130:26.14] you
[130:28.20] you
[130:46.20] you
[130:48.26] you
[131:00.26] you
[131:02.32] you
[131:12.32] you
[131:14.38] you
[131:20.38] you
[131:30.38] you
[131:32.44] you
[131:38.44] you
[131:48.44] you
[131:50.50] you
[132:04.50] you
[132:06.56] you
[132:12.56] you
[132:22.56] you
[132:24.62] you
[132:38.62] you
[132:40.68] you
[132:50.68] you
[133:00.68] you
[133:02.74] you
[133:16.74] you
[133:18.80] you
[133:28.80] you
[133:30.86] you
[133:50.86] you
[133:52.92] you
[134:08.92] you
[134:10.98] you
[134:20.98] you
[134:23.04] you
[134:33.04] you
[134:43.04] you
[134:45.10] you
[134:51.10] you
[135:03.10] you
[135:05.16] you
[135:21.16] you
[135:23.22] you
[135:33.22] you
[135:43.22] you
[135:45.28] you
[135:57.28] you
[135:59.34] you
[136:09.34] you
[136:19.34] you
[136:21.40] you
[136:31.40] you
[136:41.40] you
[136:43.46] you
[136:49.46] you
[137:01.46] you
[137:03.52] you
[137:13.52] you
[137:23.52] you
[137:25.58] you
[137:37.58] you
[137:39.64] you
[137:41.70] you
[138:01.70] you
[138:03.76] you
[138:14.76] you
[138:16.82] you
[138:26.82] you
[138:34.82] you
[138:36.88] you
[138:42.88] you
[138:54.88] you
[138:56.94] you
[139:06.94] you
[139:09.00] you
[139:19.00] you
[139:29.00] you
[139:31.06] you
[139:49.06] you
[139:51.12] you
[140:01.12] you
[140:03.18] you
[140:23.18] you
[140:25.24] you
[140:35.24] you
[140:45.24] you
[140:47.30] you
[140:57.30] you
[141:07.30] you
[141:09.36] you
[141:19.36] you
[141:29.36] you
[141:31.42] you
[141:41.42] you
[141:43.48] you
[141:57.48] you
[141:59.54] you
[142:15.54] you
[142:17.60] you
[142:19.66] you
[142:29.66] you
[142:37.66] you
[142:39.72] you
[142:41.78] you
[143:01.78] you
[143:03.84] you
[143:15.84] you
[143:17.90] you
[143:27.90] you
[143:29.96] you
[143:39.96] you
[143:49.96] you
[143:52.02] you
[144:02.02] you
[144:12.02] you
[144:14.08] you
[144:24.08] you
[144:26.14] you
[144:44.14] you
[144:46.20] you
[145:02.20] okay so apparently my mic has been muted this whole time
[145:13.20] well that stinks
[145:16.26] two hours in my mic is muted
[145:23.26] okay
[145:27.26] we have audio again
[145:31.26] oh no
[145:35.26] okay let me comment here on youtube whoops no over here
[145:48.32] uh
[145:57.32] uh
[146:08.38] i thought i had tested everything
[146:22.38] um
[146:24.44] all right so i've got no local backup on that audio either
[146:31.44] oh well
[146:35.44] here we go
[146:50.38] um
[146:52.44] just one second here
[146:56.44] um
[146:59.50] uh
[147:01.56] uh
[147:27.50] okay
[147:29.56] well that stinks yeah i'm glad
[147:47.56] uh
[147:52.56] oh
[147:54.62] okay audio audios audios back oh well oopsie
[148:18.56] all right where was i all right let's let's forget about that
[148:23.62] it's been kind of a slog anyway there was some good stuff at the beginning and i've talked about
[148:29.62] i've talked about the differences between the array buffers and and uh allocation and
[148:36.62] there was some good stuff in here maybe we'll repeat some of it tomorrow i'm getting kind of tired
[148:42.62] i want to finish this tonight i want to get to the point where we have testing
[148:47.62] um
[148:49.68] okay serialize
[149:05.68] so
[149:08.74] i'm a little bit confused
[149:31.74] so
[149:34.80] so
[149:52.80] so
[149:55.86] okay
[150:18.86] so
[150:21.92] so key is gonna be mostly empty i'm a little confused let's see what serialize looks like
[150:32.92] serialize can cat private key okay
[150:42.92] so
[150:45.98] private key so one plus key dot byte length
[151:09.92] ua dot set zero at zero ua dot set
[151:17.98] private key so it seems like private key is 44 bytes long is that what we're saying
[151:30.98] so
[151:34.04] so
[151:56.98] i can cat a zero byte and then the private key
[152:03.04] okay 148
[152:22.04] so
[152:25.10] oh
[152:31.10] yeah i just need to move this up here
[152:49.04] so there's the public key just have an extra byte oh
[152:54.10] i'm a little bit confused about this still though because a public key i think is just 32 bytes
[153:05.10] i'm not sure
[153:16.10] so
[153:19.16] the serial is the serialized function doesn't quite make sense to me right now
[153:42.10] so it seems like there'd just be a bunch of zeros in there
[153:46.16] serialize hdk versions private key
[154:00.16] okay serialize
[154:11.16] okay hdk depth
[154:15.22] the data view is the u8
[154:23.22] chain code
[154:39.16] okay well i mean i guess i can just run and run the test and figure out what's going on
[154:45.22] let me see if i can understand from this one yeah version
[154:59.22] sorry 13 chain code
[155:04.22] so
[155:07.28] so it makes sense if this was setting to key
[155:22.28] let me do a git diff on this
[155:32.28] and see chain code
[155:59.28] okay
[156:02.34] oops node buffer copy
[156:08.34] copy target start
[156:26.28] just seems like there's going to be a bunch of zeros
[156:30.34] so we're starting at 45
[156:52.28] i'm just so confused here because we're just going to throw the u8 away aren't we
[156:58.34] so we create a new u8 we create a data view for it we write a bunch of crap to it
[157:06.34] and then
[157:10.34] we're returning
[157:20.28] the serialized version oh wait i think i i think i understand now serialize
[157:28.34] let me look at this so we are returning the buffer
[157:41.34] okay i get it now
[157:46.28] i see where i was confused okay so we're setting the x key as what i want to call this
[157:53.34] we're creating a data view for the x key
[157:58.34] xkeydb
[158:03.34] all right i'm just gonna go ahead and set this up here like that
[158:13.34] all right and then
[158:20.40] okay
[158:24.46] so
[158:52.46] all right so there's the keys data view
[158:55.52] x key x key
[159:02.52] x key all right so there's there's 13 bytes of stuff going on here so we've got
[159:12.52] the version oh and this this makes more sense now this comment so the version and then the depth
[159:19.46] which is just one byte got it so that takes us to five and then the fingerprint
[159:23.52] that takes us up to nine and then the index that's four that takes up to 32
[159:29.52] i mean up to 13 and then the chain that gets us to the 45 and then the key is 33 bytes
[159:37.52] gotcha okay and the key is always 33 bytes regardless of whether it's a private key or
[159:44.46] a public key so i kind of want to go up here and say now i don't know where this lin comes from
[159:52.52] oh it's the whole length got it
[160:00.52] i can call that x key size
[160:08.52] i'm more okay with that
[160:14.58] and then we could say that key size is always going to be 33 because for a public key it's the
[160:26.58] quadrant and then 32 bytes so that's 33 and for a private key it's zero and then 32 bytes
[160:37.52] and so then here we could just do key size and that makes sense
[160:57.58] and then i'm not really sure what we would call this
[161:06.58] so it's the
[161:17.64] so it would kind of be
[161:32.64] um
[161:33.70] key index size would be
[161:42.70] okay
[162:01.76] all right so here's a plus four so this would be indexed key size
[162:12.76] and that's going to be the same no matter what
[162:15.82] so let's go ahead and move that here
[162:23.82] okay
[162:36.88] so
[162:47.94] okay that makes more sense now
[163:01.94] and this one is going to be
[163:13.94] 5, 11, 15, 47, 80
[163:39.94] is that what we're saying wait why is it not
[163:46.00] so why is this one different these two look exactly the same
[164:06.94] let's try this again 4 plus 1 is 5
[164:12.00] plus 4 is 9 plus 4 is 13
[164:20.00] plus 32 is 45
[164:28.00] plus 30 is 75 plus 3 is 78
[164:36.00] these two are exactly the same so we'd also do
[164:43.06] so
[165:00.12] do i need a key weight here
[165:07.12] i guess i do
[165:20.18] yeah all right
[165:23.18] okay i think i think i've finished the conversion the problem is
[165:30.18] there's no way to really test this in pieces you it's kind of an all or nothing deal
[165:35.18] so
[165:55.18] let's do a proceed buffer
[166:14.24] all right well let's at least uh give it a good old add
[166:24.24] whoop he went eight array
[166:29.30] okay let's get rid of that well i should have gotten rid of that a while ago
[166:48.30] so
[166:59.36] all right here we go so this would just be
[167:05.36] a mix safe buffer there
[167:14.30] okay
[167:18.36] i think that's going to be fine
[167:43.30] we're going to need a function x2u8
[167:51.30] array x dot length divided by two
[168:19.30] i equal zero i less than or equal to size right no what x dot length i plus equals two
[168:37.30] and then we got x i
[168:52.36] uh let's see hello
[168:56.36] subster whoops that's not what i wanted to do can we get that undone
[169:05.30] subster and then help me remember here two two versus substring okay subster okay
[169:16.36] subster this is the format that i like
[169:22.36] and then we can say i two
[169:27.36] let h equals
[169:33.30] u8 i won't let b equals
[169:38.36] parse int h16
[169:47.36] and then
[169:54.30] h8
[170:11.36] j equals b
[170:14.36] but i already did this so many times why am i doing this again i just did this
[170:19.30] and um
[170:21.36] dash tx let me just grab it from there x2 why in the world was was i writing that again i have no idea
[170:31.36] well i do have an idea it's because i was just a little sleepy i was just a little bit sleepy
[170:48.36] there we go
[170:53.36] hex to u8
[171:22.36] parse int
[171:24.42] right yeah that makes sense
[171:34.42] there we go
[171:37.42] okay so that's what i needed up here
[171:40.42] we don't need to buffer that from we need a hex to u8
[171:47.36] and we can get rid of that
[171:59.42] okay and then we need
[172:05.42] well that could just be u8 array
[172:10.36] i will i will my mind will be blown and i'll be so sad and so happy if from
[172:18.42] supports a
[172:26.42] element
[172:29.42] index
[172:32.42] from map function
[172:36.36] interesting
[172:42.42] okay i would be so happy if it supported hex after all this time
[172:49.42] but alas of course it doesn't
[172:54.42] you've taken happy pills
[173:03.36] secure random why in the world
[173:07.42] i mean
[173:10.42] the way to do this is var
[173:15.42] priv equals new u8 array 32
[173:24.36] then crypto dot ran get random values priv
[173:34.42] that's it where's the secure random idea coming from secure random
[173:45.36] what are they smoking
[174:10.36] hey it's some breath of the wild
[174:20.42] crypto equals require
[174:25.42] node crypto actually we just put that up here
[174:35.36] weird secure random
[174:42.42] okay oh one thing i was mentioned earlier is we got new musics
[174:59.42] okay
[175:04.36] i'm not sure oh
[175:24.36] this curve thing
[175:41.42] okay buffer
[175:46.36] that's interesting
[175:53.42] okay
[176:22.42] okay
[176:42.42] new u8 array 32
[176:56.48] okay i see what's going on there just checking that the different zeros still
[177:03.42] and 8 array 99 i don't know what that's about
[177:07.48] oh just to get just to see that the length is not correct okay hex 2 u8
[177:22.42] more of that
[177:33.48] and we're still all right we're getting close to the bottom
[177:48.42] oh man to believe that i got all of this right though it's uh
[177:57.42] it's harder to imagine
[178:20.42] guess we'll see
[178:31.48] here we go let's go
[178:37.48] that's my best let's go my very best one i saved it just for you
[178:49.42] the difference of this is so low
[179:16.42] let's see what happens
[179:35.42] all right run npm install
[179:46.48] npm test
[179:55.42] okay that's not so bad this is some stuff that actually makes a lot of sense
[180:14.42] 39 failing
[180:21.48] i should properly derive the chain path m
[180:27.48] so it's probably something super fundamental which is always good
[180:40.42] fixtures whoops test fixtures hd key
[180:56.42] public private seed cool well let's go ahead and try this out and see what we get
[181:25.48] test one
[181:50.48] here we go
[182:04.48] let's see here from master seed
[182:15.48] we need a little x2u8 here
[182:39.48] it's nice when the very first test fails because that's not subtle
[182:47.48] these bugs are difficult
[183:16.54] all right let's take a look here
[183:25.54] oh
[183:54.60] cannot find module
[184:08.66] whoa
[184:19.60] oh no now i've done it i've installed all of npm the whole thing
[184:40.60] my system is critically vulnerable okay
[184:52.66] okay valid
[185:07.60] the offset is out of bounds that's super easy you just need to put the offset in bounds
[185:36.60] i'm a little confused here
[185:38.66] this is console
[185:41.66] console.log
[185:44.66] take a peek at the chain key
[185:47.66] and take a look at the X key
[186:01.60] okay
[186:29.60] let's see what happened here
[186:31.66] so what it's supposed to be is xkey.set because this one was for copy but that's not
[186:39.66] it's not how it worketh over here
[186:43.66] and same thing here this should be
[186:52.60] xkey is going to call .set i've probably messed that up in another place as well let's see
[187:01.66] that looks right well now we don't use concat anymore
[187:05.66] because it turns out that it's not actually really helpful
[187:20.60] okay
[187:24.66] so we're setting that on the X key
[187:31.66] that makes more sense
[187:35.66] hello
[187:41.66] all right well good news my friends
[187:48.60] this has been it my confidence level has never been higher
[187:53.66] huh yo rune hey you found me i was trying to hide from you
[187:59.66] i thought maybe if i streamed under a different channel you wouldn't be able to catch me but oh you did
[188:07.60] uh how you doing man
[188:19.66] yeah well i'm i've got a few different channels now there's a channel for utah rest there's a channel for utah stack js
[188:27.66] there's a channel for coolage86 there's a channel for dash incubator
[188:34.60] so we got all the rounds now
[188:40.66] and then i i got the suggestion stuff set up too
[189:02.60] okay
[189:19.66] so i'm a little bit tired
[189:31.66] type of hd versions is not assignable to hd versions
[189:59.66] oh i need to not put that one there oh we need to get rid of these console dot logs
[190:07.66] put that back
[190:32.66] oops i accidentally deleted that
[190:37.72] that's okay
[190:46.72] so what i'm trying to do here
[190:51.66] is i've ported this from using node buffer to using uint8 array and it's been a little winding road because i had to refamiliarize myself with all the ins and outs and and you've got some ridiculous stuff so check this out all right so for example
[191:09.66] um if you use a data view set then the first parameter is the offset and the second is the value
[191:22.72] but if you use uint8 array set you can guess the first parameter is the value and the second parameter is the offset
[191:38.66] and if you use node.js copy then it's the target
[191:48.72] the source and the target are reversed so with set and both of these the caller is the target but with the node buffer the caller is the source
[192:05.66] so it's just a lot of little things like that where it's did i get it all right
[192:13.66] and then who knows about to find out for the second time oh wait uh hd so yeah we just with these two we just i accidentally changed a copy into a set but then that just needed to be a set wait that doesn't make any sense
[192:37.66] key oh sorry yeah so this one corresponds to this one x keyset chain code this oh yeah earlier i was looking at the thing i couldn't figure out wait something doesn't feel right but i can't articulate it right now
[192:51.66] all right so this is going to be you went eight okay so now i suspect it's going to get much further
[193:16.66] will it pass the tests that'd be cool i'm not going to hold my breath yet but
[193:36.66] miracles happen every day
[193:55.72] so
[194:08.78] let's see that's the correct one that's the correct one is that it is there anything else
[194:37.84] is there anything else
[195:05.84] let's see what's going on here
[195:09.90] so
[195:22.96] so
[195:41.02] there we go
[196:03.08] so
[196:13.14] versions
[196:31.08] all right let's see what it says
[196:38.14] canceled after 25 seconds well let's see why node 14 failed node 14 could have failed because lots of reasons
[196:55.08] all right
[197:05.08] all right nine failing which ones failed as it's showing down here these are the ones that failed
[197:26.08] oh get random values is not a function right okay so that one's failing because of its old node
[197:36.14] okay so with that
[197:43.14] i should just take that i should step that back a little
[197:54.08] so let's take a look here
[198:15.08] here
[198:29.14] get random whoops let me go to my test here so get random values
[198:38.08] what we should actually be doing here is get random bytes 32
[198:48.08] barrands there we go
[199:14.08] node crypto dot get random
[199:20.14] random bytes 32
[199:27.14] there we go
[199:29.14] so this should actually be random bytes
[199:43.08] that's what we do when we swap over to the web crypto all right so no big deal there
[199:48.14] no harm no foul
[200:04.08] all right you want a test there we go
[200:14.14] let's see how far we go this time
[200:21.08] oh i really just care about probably node 16 or so
[200:35.14] don't time out after 20 seconds on me you can do it you can make it all the way
[200:43.14] all right so it looks like there really is something wrong
[200:50.14] seven failing
[200:55.20] all right and this one's nice and easy too i like that
[201:00.20] so what happened here is that it's comparing with a double equals string coercion
[201:08.14] between and it's expecting the two string method to result in
[201:18.20] hex but it's not resulting in hex so it's actually not a problem at all
[201:29.20] so everything might be correct
[201:33.14] could be it may just be that we need to get the test updated to use the right
[201:40.20] format of key so assertion error
[201:45.20] what does it say when private should parse it
[201:58.14] equal chain code to string hex okay to string hex there is no to string hex
[202:06.20] we can do hex to u8 or we can do so we can do u8 to hex
[202:13.14] let me go grab that real quick much simpler function
[202:27.20] that just needs to be baked into the standard library it just really really
[202:31.20] does i just can't i can't think of any reason why it wouldn't be
[202:35.20] it seems so strange you know why would you not want this in the standard
[202:42.14] library why just why just why why spend months and years on these standard
[202:54.20] bodies and just never come up with usable standards that's the big question
[203:00.14] all right so we need to do
[203:21.20] there's gonna be a lot of these let's see if I can find a good way to do a
[203:26.14] replacer on these so we're gonna have a space and then there's going to be a
[203:31.20] bunch of stuff and then there's going to be a dot to string hex and we want to
[203:41.14] replace that with u8 to hex some stuff does that work looks like it did
[204:06.14] what is a that's going to be a buffer buffer buffer buffer buffer buffer
[204:16.20] buffer no but we'll come back to it no we'll come back to it no no okay what
[204:25.20] we need is to revise here hdkey that I think we can do
[204:35.20] okay then we need to find these ones that one
[204:53.20] all right there we go all right so this one is now yeah we're updating the test
[205:11.20] again test test all right I think it's possible it could it could pass now it
[205:25.26] could have just been that one was I don't remember what the thing was oh it
[205:30.26] was it was copying the copy was in the wrong order and this one it was just
[205:37.20] the wrong string method bless me the blessings are heavy with this one
[206:06.26] all right let's just see what no really
[206:17.32] deriving a child key must not mutate
[206:25.32] wait how could we even have more failing than we had before is this is
[206:46.38] this even the right do I need to just refresh this or something
[206:53.38] okay so I think let's see why node 14 failed
[207:10.44] driving a child does not mutate the internal state should not mutate when
[207:16.44] deriving with a private key okay I think I understand what's going on there
[207:22.38] that one that one doesn't blow my mind so this one if we're gonna derive a
[207:34.44] child there's a shared buffer when we derive a child we need to replace the
[207:47.38] shared buffer because I was trying to give it the same performance
[207:54.38] so let's see
[208:16.38] okay this is a new buffer
[208:28.44] okay let's see what's going on here so drive child passes in an index these are
[208:39.38] very variables so they're they're single use and we set and we make a copy of
[208:49.44] private key make a prop copy of index buffer we make a copy of the iBuff we
[209:01.38] make two versions HD here we set private key and then we do a tweaker so I wonder
[209:19.44] it wasn't clear to me why there were some of these new it new UN8 arrays and
[209:26.38] I'm wondering if the reason for it wasn't to make a copy it's one of these
[209:38.44] things about doing things on multiple lines is it's not super clear why
[209:46.44] something is the way that it is parent private parent key private child key so
[209:54.38] I think this tweaker my return whatever it tweaks so I'll slice iBuff okay
[210:06.44] that's all new data so let's see we make a copy here derived child and next plus
[210:15.38] one and let's try the same thing here let's do do public key copy and we'll
[210:25.44] take the public key and we'll make sure that this tweaker gets the public key
[210:35.44] copy just in case it operates directly on it then we've got the derived child
[210:43.38] and then this seems like it should be probably a child is that what this is
[210:53.44] HD set private key so that's derived child how about derive let's take a look
[211:04.44] at derive again and let's see is there anything where we would be modifying
[211:12.44] something that's the original HD key no it doesn't seem like it nothing
[211:24.50] there's attached to any sort of state so I'm gonna guess that what I thought was
[211:37.44] making a copy internally because I thought it was it why is there a buffer
[211:41.50] dot from on a buffer dot from you know you just we just made this thing it's
[211:46.50] obviously a buffer why is it a buffer dot from because it's not doing it to
[211:52.50] make a buffer it's doing it to make a copy and it's calling dot from because
[211:56.50] new is unsafe so so dot from does the business of allocating and copying
[212:06.50] in one function but this is why this is why I I'm becoming more and more
[212:11.56] convinced do one thing per line because then your variable name is the comment
[212:15.56] of what you're doing and so if you only do one thing for per line you actually
[212:20.50] don't need a lot of comments anyway copy key all right so let me go back here
[212:43.50] all right and let's see if we can just watch 16 again
[212:51.56] well that kind of sucks or is that you only get 26 seconds to run I mean
[213:04.56] that's that's npm install right there and then we're done hey did that work
[213:12.56] did that work that worked hey hey are you that worked all right cool so let's
[213:37.56] see according to that we can I want to see why node 10 fails but I'm sure it's
[213:44.62] something to do with you in 8 array or something you cannot find module node
[213:51.62] crypto okay all right let's let's let's not do the node crypto then just for the
[214:06.62] sake I want to see how low can it go you know I'm saying it's more of a
[214:33.62] complexity thing than anything else but all right cool so this is good
[215:02.68] all right I'm not surprised that this is failing but I would like to know why
[215:09.74] that's that's really text encoders not defined okay we're dropping support for
[215:22.68] node 10 obviously okay it was gonna come sooner or later
[215:47.74] all right what else do we need to do here so from this point we could apply
[216:12.74] some crypto stuff I'm too tired to do it but then we just need to figure out
[216:28.80] what to do about this tweak function which there is an issue open about where
[216:35.74] to get the different tweak function or where to something or other words and
[216:41.80] stuff I probably find it
[216:49.86] oops
[216:55.58] all right
[217:23.56] okay so we're gonna do this one here okay so we're gonna do this one here and
[217:39.62] then we're gonna do this one here okay so we're gonna do this one here okay so
[217:56.68] we're gonna do this one here and then we're gonna do this one here okay so
[218:17.68] okay oh and we still have the music I stopped the music that was me I can turn
[218:36.68] music on what to do here what to do what to do
[218:49.74] well it's time for me to go to bed that's what it's time for but trying to
[219:04.94] is there anything else before I go
[219:26.94] okay buffer buffer buffer buffer oh what the hey am I sultan or am I sultan
[219:43.10] let's go ahead and break the havoc of well
[219:51.74] okay
[219:54.74] oops
[220:23.74] whoops
[220:26.74] okay
[220:37.74] all right
[221:05.74] and then let's see here Nick's safe buffer add types to push out that get
[221:21.14] checkout ref simple chess cherry can get rebase - I'm a and then remove safe
[221:41.70] buffer no problems there and then check out rough types
[221:58.62] a race - I mean
[222:04.42] and we could check out rough you're a ray
[222:25.86] don't need that don't need that don't need that
[222:51.54] okay so first what I want to call this
[222:57.26] replace buffer node buffer with an 8 array
[223:07.30] what
[223:18.50] okay
[223:21.50] okay
[223:37.50] hmm
[223:40.50] okay
[223:43.50] okay
[223:46.50] okay
[223:49.50] okay
[223:52.50] okay
[223:55.50] okay
[224:22.50] let's see
[224:25.50] all right so I was going to reword this and this is fix update tests for you at
[224:44.02] a ray fix move not be 10 from test matrix
[225:09.70] no text encoder support okay
[225:23.78] so
[225:26.78] okay
[225:29.78] okay
[225:32.78] okay
[225:35.78] okay
[225:38.78] okay
[225:41.78] okay
[225:44.78] okay
[225:47.78] okay
[225:50.78] okay
[225:53.78] okay
[225:56.78] legacy
[226:03.78] legacy
[226:07.78] we're gonna go in this direction
[226:22.78] okay
[226:25.78] okay
[226:31.78] okay
[226:46.78] so if we really wanted to we don't have to drop node v10 we could do something
[226:54.30] else for text encoder if that's the only thing that's causing us die but but when
[227:00.50] we go to replace we could still maybe replace noble crypto first maybe I will
[227:08.66] do that next we could let node crypto be the last to die that would be kind of
[227:19.02] interesting so I would say well it's you know like I said it could could provide
[227:32.66] some sort of show let me think about this so with the text encoder how else
[227:43.98] could we do so this is just ascii text so there's nothing too cray-cray about
[227:48.66] it trying to think what would we need to do I think in that particular case we
[228:02.46] could do an ascii function ascii to uint8 array and then we could take in a
[228:16.02] str and we could just do str dot split or maybe it would be better just to go
[228:25.54] let u8 equals new uint8 array str dot length that's gonna work for ascii I
[228:41.30] mean even even we could just let me think for let i equals 0 i less than or
[228:59.86] equal to str dot length no i less than str dot length i plus equals 1 and then
[229:10.22] we could do u8 i equals str dot char code at 0 well this is what we'd have
[229:22.30] to do actually be let code equal let is that the byte is that the same as the
[229:47.24] byte I think maybe it is
[230:02.64] char code at yeah
[230:06.44] a pram string
[230:33.60] ascii plain 7-bit ascii string no special characters or emojis
[230:52.80] and I mean that's something we could precompute - I mean really if you think
[231:20.52] about it
[231:29.04] yeah so let's give that a try hold on just one second
[231:38.36] so new text encoder dot encode dot to string 16
[231:49.60] nope
[232:03.44] so we could do buffer dot from all that business
[232:10.88] let's see but then we still we still have no way to get that if we wanted to
[232:23.28] get that in bytes what would we have to do
[232:33.68] just thinking out loud here if I didn't want to use text encoder just keep
[232:40.12] compatibility broad if there's relatively no cost to it
[232:46.40] what do I do? u8 array dot from and I just put in
[233:08.40] 0x42, 0x69, 0x76, 0x63, 0x69, I guess 69 is letter island
[233:29.28] maybe not oh there's space yeah 69 is in what?
[233:44.96] no 6e is in okay
[234:01.60] I think that's reasonable actually
[234:31.12] okay
[234:32.12] so I'm going to do that again so I'm going to do that again so I'm going to do that again
[234:59.96] all right and that's fair enough
[235:15.08] wow I can't believe this keeps compatibility all the way back to node 10 if we just make
[235:19.96] that change there all right that's I mean that's not a bad trade-off okay but now I
[235:26.36] need to go to bed because I can't really think through problems anymore
[235:29.22] and then at the very end that's when we'll
[235:58.50] that's when we'll uh we'll drop the node support at the very because we can get literally everything
[236:09.26] we can't have everything working all the way back to node 10 apparently and then just the
[236:15.66] last commit will be dropping all that stuff because I really don't want to try to support
[236:20.98] it when well I mean even then I probably just have a couple lines I probably can support
[236:30.46] it because I just do one a single if just do a single if if crypto dot get random values
[236:38.22] or if crypto dot subtle and if not if not crypto dot subtle then you know put you know
[236:48.90] let's what it'll be I mean it's three lines per function it's three functions not 10 lines
[236:56.00] of code total 11 lines of code total I mean there's some spaces or whatever but yeah it's
[237:00.74] probably worth it that's not that's not a big deal to to not break things that work
[237:06.18] right as I'm always saying
[237:31.50] all right cool let's uh I just want to check and see and then I'm off
[237:58.88] so basically just just to kind of prototype this out while that's thinking maybe I can
[238:04.10] go ahead and click on details here so it doesn't time out on me um but what I'm thinking whoops
[238:12.12] that yeah yeah look at that ba da da da da da da da da da da da da da da da da da da da
[238:40.24] da da da da da da da da so here's what I'm thinking
[238:47.92] (soft music)
[238:50.34] (soft music)
[238:52.76] (soft music)
[238:55.18] (soft music)
[238:57.60] (soft music)
[239:00.02] (soft music)
[239:02.44] (soft music)
[239:05.00] (soft music)
[239:07.42] (soft music)
[239:10.04] (soft music)
[239:12.46] (soft music)
[239:18.34] (soft music)
[239:24.26] (soft music)
[239:30.26] (soft music)
[239:36.64] (soft music)
[239:39.06] - All right.
[239:44.44] So I'm thinking we have a function
[239:47.80] somewhere down here in the depths.
[239:51.72] Let's say it goes right here.
[239:55.36] Create HMAC 512.
[240:00.02] (soft music)
[240:02.44] (soft music)
[240:04.86] So we add
[240:17.30] entropy and data.
[240:24.94] So there's entropy and there's data.
[240:31.92] And we say, if not crypto.subtle.
[240:35.08] (soft music)
[240:37.50] And there we go.
[240:43.76] Secret, salt or key.
[240:58.04] (soft music)
[241:00.46] Message or data.
[241:27.24] So let hash equals.
[241:29.16] (soft music)
[241:31.58] (soft music)
[241:34.00] (soft music)
[241:36.42] Hmm, okay.
[242:03.08] So that's it.
[242:05.28] That's our create HMAC function.
[242:07.26] And then
[242:09.68] to do webcrypto.
[242:26.84] So I had that one, but that one was kind of annoying
[242:29.16] and long, but I can copy that back.
[242:31.84] (soft music)
[242:34.26] Again.
[242:42.64] Oh, but then we gotta have the async.
[242:51.68] It's gonna go crazy.
[242:52.88] Yeah.
[243:00.80] So we have to, we still have to update everything
[243:03.92] for async either way.
[243:05.22] SHA-256.
[243:17.62] Buff.
[243:21.04] So there's our create HMAC 512.
[243:31.56] And similarly, we just have a SHA here.
[243:36.56] Function SHA-256.
[243:39.72] Buff at param UN8 array.
[243:50.68] And then buff and then returns UN8 array.
[243:59.04] UN8 array.
[244:00.50] Hash.
[244:02.98] Hash.update.
[244:19.96] Hash.digest is
[244:25.00] let's SHA-256 equals UN8 equals new
[244:30.00] UN8 array SHA-256 return UN8.
[244:38.00] And this would actually be async.
[244:53.00] So if crypto create hash.
[244:58.00] And then we get a little bit faster to do webcrypto.
[245:05.00] It'd still be async, but we can get a little faster.
[245:07.60] SHA-256.
[245:12.62] All right.
[245:20.80] My random bytes.
[245:22.18] Okay, so this one would be
[245:50.32] the same thing.
[245:51.16] Oops, else.
[246:02.00] (keyboard clacking)
[246:05.00] Get random values.
[246:25.16] And then we just, boop, plop it right on in.
[246:29.80] (keyboard clacking)
[246:32.80] Create HMAC 512, and then we would pass in here
[246:58.52] master secret and seed buffer.
[247:03.42] That's, I think, what we're looking at there.
[247:10.34] As possibly undefined.
[247:14.08] All right, we'll just do throw new error not implemented.
[247:26.58] (keyboard clacking)
[247:29.58] All right.
[247:40.08] Hmm, right.
[247:49.20] That's one of the reasons I wanted to use global this
[247:52.60] is because then with global this,
[247:54.24] it actually understands the type a bit better.
[247:57.06] Hmm.
[248:00.60] Yeah, I see that, okay.
[248:04.52] Window equals window.
[248:17.06] App type window.
[248:22.72] (keyboard clacking)
[248:25.72] Hmm.
[248:48.84] (keyboard clacking)
[248:51.84] Okay, this one.
[249:17.48] (keyboard clacking)
[249:20.48] Hmm, that's weird.
[249:35.68] (keyboard clacking)
[249:38.68] All right, so I'm just gonna tell that one
[249:43.96] not to grape at me about it, and we're done.
[249:47.44] Okay.
[249:51.08] (keyboard clacking)
[249:54.08] Okay.
[250:09.68] (keyboard clacking)
[250:12.68] Oh, okay.
[250:15.40] Oh, we'll check that out, Mr. Jojobite.
[250:18.92] Well, it's because of the way I'm detecting it.
[250:21.32] If I switch it back to detecting global this.window,
[250:23.92] then it works.
[250:25.28] But I was doing this for node 10
[250:27.56] 'cause I figured, eh, you know.
[250:29.80] (keyboard clacking)
[250:32.80] (soft music)
[250:35.22] No, this will not work because this is not JavaScript.
[250:44.92] This is ES20XDX.
[250:48.16] Well, at least up at the top,
[250:51.20] it says export default function,
[250:53.36] and then it's got, yeah, so that's 20XDX.
[250:56.28] It would need to be JavaScript, not ES20XDX.
[251:02.24] (soft music)
[251:04.66] Let's see.
[251:09.80] Yeah, so the global this.window will work,
[251:14.44] but the problem is just, and this is not a big deal.
[251:18.80] It doesn't really matter, but I was just,
[251:21.16] I was just thinking it'd be nice if it worked in node 10
[251:23.88] since basically the only things I found
[251:26.72] that don't work in node 10 are things like this,
[251:31.40] where, I wish I knew a simpler way to do that,
[251:35.12] but that's kind of,
[251:36.42] that's kind of it.
[251:41.76] Okay, what else was I looking for?
[251:44.48] Oh, okay, that solves all the linter problems, I think.
[251:49.32] Oh, right, I was checking to see
[251:54.72] was there anything else to do with crypto.
[251:58.52] Crypto, so we just create HMAC and then create hash,
[252:03.52] and so then if I put the browser version of that,
[252:08.34] I wonder, is there, there's not one for signing,
[252:13.48] but is there one for creating a hash web crypto sync?
[252:18.48] (computer chiming)
[252:21.40] Let's see, is there any sync?
[252:32.32] Nope.
[252:34.32] Sync.
[252:36.96] (computer chiming)
[252:44.20] (computer chiming)
[252:47.12] Okay, well, that's that then.
[253:03.30] Okay.
[253:09.76] (computer chiming)
[253:13.20] So if I could just,
[253:15.56] do you know anything about Mocha and async Jojobite?
[253:19.80] 'Cause supposedly you're supposed to be able
[253:25.50] to run these asynchronously.
[253:27.64] (computer chiming)
[253:30.56] (computer chiming)
[253:33.48] Let's see, for each.
[253:41.96] (computer chiming)
[253:44.88] (computer chiming)
[253:47.80] Okay.
[254:12.48] (computer chiming)
[254:15.40] I wonder if I just push this.
[254:29.42] Oh, it should.
[254:33.48] (computer chiming)
[254:37.66] (computer chiming)
[254:40.58] NPM, install Mocha at latest.
[254:49.74] (computer chiming)
[254:53.14] Mocho.
[254:57.54] Mocha.
[254:59.98] (computer chiming)
[255:02.90] (computer chiming)
[255:05.82] Mocha 5.
[255:15.58] Eh, whatever.
[255:22.46] Let's see, can I run the test locally?
[255:29.20] Nah.
[255:31.78] (computer chiming)
[255:34.70] Okay, hash 160.
[255:49.26] Okay, 418, let's see, what's on line 418?
[255:54.82] (computer chiming)
[255:57.74] (computer chiming)
[256:00.66] Hmm.
[256:18.24] (computer chiming)
[256:21.16] Get there.
[256:24.60] (computer chiming)
[256:27.52] Let me try.
[256:53.52] (computer chiming)
[256:56.44] Just for the sake of testing locally,
[256:59.76] I'm gonna see what happens if I run the test like this.
[257:04.26] Data must be a string or a buffer.
[257:07.90] Where's hash base coming from?
[257:15.82] (computer chiming)
[257:22.88] (computer chiming)
[257:25.80] Oh, did I forget to return?
[257:37.56] (computer chiming)
[257:41.68] UN8Array, hash.digest.
[257:51.36] (computer chiming)
[257:54.28] All right, let's try this one, 256.
[258:03.22] (computer chiming)
[258:06.14] That seems like that should work.
[258:19.50] (computer chiming)
[258:21.38] Okay, everything passes.
[258:23.74] So, npm install, save RIPEMD 160 at latest.
[258:28.74] And then what happens if I go back to saying
[258:44.50] that this npm test, hmm, data must be a string or a buffer.
[258:49.50] Okay, what about npm install save-incubator/ripemd160?
[259:11.78] Okay, and then ripe-incubator, ripemd.create.
[259:16.78] Okay, huh, I wonder why that makes such a big difference.
[259:38.34] Or did I not actually, let's see, SHA-256.
[259:43.34] Okay, yeah, it's returning U8, okay.
[259:52.74] Let U8 equals return U8, console.log U8, npm run test.
[260:04.06] U8, npm run test, un8array.
[260:09.06] Okay, so it is in fact returning the un8array
[260:16.06] in that version of it.
[260:31.38] Okay, okay, good to know.
[260:59.22] Okay, so how could this be a string, I don't know.
[261:04.22] RipeMD, that just doesn't seem right.
[261:16.26] Does the one that's packaged with this really not support?
[261:27.42] Great, did I add that, change?
[261:29.46] I think I must have.
[261:40.30] Okay, so this, oh.
[261:41.54] What is this hash-based stuff?
[261:52.18] (soft music)
[261:54.60] It doesn't do anything.
[261:59.94] What is the dash-incubator one based on then?
[262:12.26] Ah, whatever, who cares.
[262:16.14] Okay, I'm taking one last look
[262:19.14] and then I really am going to bed.
[262:21.28] (soft music)
[262:23.70] Okay, so.
[262:28.56] All right, so does this npm run test?
[262:50.52] (soft music)
[262:52.94] All right.
[262:54.96] Okay, so I guess I need to PR that or something.
[263:13.42] (soft music)
[263:15.84] Okay, so at least I can run the test now.
[263:37.92] So let me take another look at this.
[263:42.78] (soft music)
[263:45.20] Okay, do I have any more console.log in here?
[263:54.10] Console.log, nope.
[263:55.78] And then do I have any more crypto stuff?
[264:00.66] Nope.
[264:02.62] (soft music)
[264:05.04] Okay.
[264:17.42] Async plus crypto.
[264:25.86] And then if I go into here,
[264:32.42] (soft music)
[264:34.84] if I just turn,
[264:37.98] can I just turn every function in an async function?
[264:41.90] 'Cause if I can,
[264:44.62] let's do it,
[264:51.18] doot, doot, dot, star, function.
[264:58.14] (soft music)
[265:01.14] (keyboard clicking)
[265:04.14] I do one async function.
[265:15.14] All right.
[265:18.58] (soft music)
[265:21.00] (keyboard clicking)
[265:24.00] Oh, whoops, hold on.
[265:51.10] (soft music)
[265:53.52] There we go.
[266:10.24] It should work.
[266:13.98] That's hilarious.
[266:19.22] (soft music)
[266:21.64] (keyboard clicking)
[266:24.64] All right, so it says 45 passing.
[266:51.00] All right, I'm gonna take it a little further.
[266:53.00] I said I wasn't, but I lied.
[266:59.52] (soft music)
[267:04.34] Motrify, what is Motrify?
[267:20.60] Does that do anything?
[267:21.44] Are we using it?
[267:22.28] (keyboard clicking)
[267:29.94] Okay.
[267:50.52] (soft music)
[267:52.94] I think,
[267:56.12] (keyboard clicking)
[268:01.04] 6.3.
[268:09.60] I can get rid of that thing there.
[268:14.58] I'll just leave that alone for now.
[268:18.80] (keyboard clicking)
[268:21.80] 1.4.
[268:32.86] Let's see, will this run the test?
[268:37.62] Yeah, it'll run the test, okay.
[268:41.04] So I don't even need to change that.
[268:45.48] Okay.
[268:46.32] (soft music)
[268:48.74] Oh, whoops.
[268:59.56] (keyboard clicking)
[269:02.56] (sighs)
[269:15.68] Async the tests.
[269:17.22] All right, so.
[269:28.86] 256, so, at least the hash 160.
[269:40.60] This needs to go async.
[269:43.52] And if that goes async,
[269:46.04] (keyboard clicking)
[269:48.60] then it means that this needs to go async.
[269:52.56] And this needs to go async.
[269:56.64] (keyboard clicking)
[269:59.64] And then that means this needs to go,
[270:14.04] this needs to go,
[270:15.68] this needs to go,
[270:18.70] this needs to go,
[270:21.86] and then, oh, that one already is.
[270:26.52] Which means that this goes,
[270:33.20] which means that derive goes.
[270:36.28] So everything, basically,
[270:37.80] just everything becomes asynchronous.
[270:42.92] This becomes asynchronous.
[270:45.00] And then again, let's see.
[270:49.22] Oh.
[270:54.00] (keyboard clicking)
[270:57.16] Arrow I less than entries dot length.
[271:01.80] I plus equals one.
[271:05.60] (keyboard clicking)
[271:08.82] (keyboard clicking)
[271:11.82] Oh, then I need to do, let's see, equals entries I.
[271:18.20] And then this needs to become async.
[271:22.78] I don't think that serialize has to.
[271:34.08] Well, no.
[271:34.92] These are actually gonna become async too,
[271:38.48] 'cause the BS 58 check, when that's converted,
[271:41.54] that becomes async, which means these become async.
[271:45.20] And then this becomes await.
[271:46.80] And then this becomes await.
[271:50.40] Pretty much from the top,
[271:54.64] everything, I think every single function
[271:59.84] becomes async, except for create.
[272:02.86] (keyboard clicking)
[272:05.86] And the fingerprint.
[272:13.54] That one doesn't seem to get it either.
[272:15.46] (keyboard clicking)
[272:20.76] This one does.
[272:31.28] (keyboard clicking)
[272:34.28] (soft music)
[272:44.14] (keyboard clicking)
[272:47.14] (soft music)
[272:49.56] Let's see here.
[273:17.26] (keyboard clicking)
[273:19.26] Set buffer, maybe get string.
[273:21.22] I don't know.
[273:23.50] (keyboard clicking)
[273:26.50] Prompt seed.
[273:29.18] (keyboard clicking)
[273:32.18] HD from JSON, turns promise.
[273:46.16] (keyboard clicking)
[273:49.16] Fingerprint.
[273:56.42] Derive path.
[274:01.60] (keyboard clicking)
[274:04.60] (soft music)
[274:07.02] All right, we're gonna await that.
[274:27.18] Async this, await that.
[274:30.64] Okay, wipe private data.
[274:32.80] That one gets to stay.
[274:34.08] (keyboard clicking)
[274:37.08] All right.
[274:50.14] (keyboard clicking)
[274:54.14] (soft music)
[274:56.56] Okay, drive child.
[275:07.42] (keyboard clicking)
[275:11.38] Get private.
[275:19.22] (keyboard clicking)
[275:21.20] Okay, maybe get string.
[275:22.78] Maybe get buffer.
[275:24.10] (keyboard clicking)
[275:32.88] Promise.
[275:38.28] (keyboard clicking)
[275:42.78] Get private, extended.
[275:50.76] (keyboard clicking)
[275:53.76] Promise.
[276:12.64] Okay.
[276:16.94] (keyboard clicking)
[276:19.94] All right, there it goes.
[276:25.30] So there's that whole thing.
[276:26.66] (keyboard clicking)
[276:29.66] Async full send.
[276:33.40] (keyboard clicking)
[276:36.40] Let's see if we can get this thing to test.
[276:40.02] Basically, just anywhere there's a function, await it.
[276:47.66] (keyboard clicking)
[277:15.50] Arrive.
[277:17.00] (keyboard clicking)
[277:20.00] Child key to JSON that.
[277:24.90] Maybe I should actually have those,
[277:29.36] revert the behavior a little bit on that
[277:31.22] so that they compute ahead of time when you set the key.
[277:36.22] (keyboard clicking)
[277:40.00] (keyboard clicking)
[277:43.00] 'Cause the two JSON, it really stinks if it...
[277:49.84] (keyboard clicking)
[277:52.84] Where's this assert from?
[278:01.88] Right, right, okay.
[278:06.12] Oh, I remember what I did with this.
[278:08.88] But...
[278:10.40] (keyboard clicking)
[278:13.40] Probably doesn't handle asynchronous functions.
[278:25.88] (keyboard clicking)
[278:28.88] Oh no.
[278:34.12] Wait, this doesn't seem right.
[278:39.70] (keyboard clicking)
[278:42.70] Oh, so those have two hex on them, but they still work out
[278:51.78] because they both end up being the same thing.
[278:58.66] Yeah, okay, that makes sense.
[279:00.10] All right.
[279:02.38] 'Cause the strings are still the same,
[279:08.00] even though...
[279:08.90] Oh, their checking is wrong.
[279:15.10] We don't have to await that.
[279:23.42] We don't have to await private data,
[279:25.58] we do have to wait for the extended key.
[279:27.62] I don't think we have to await getPrivateKey,
[279:36.50] let me double check on that.
[279:38.80] (keyboard clicking)
[279:41.80] Oh my goodness.
[279:56.34] (keyboard clicking)
[280:00.82] (keyboard clicking)
[280:03.82] Oh my goodness, this is gonna be just so...
[280:12.86] This is impossible.
[280:14.08] Okay.
[280:22.94] It doesn't need it for getPrivateKey though.
[280:25.14] (keyboard clicking)
[280:28.14] Okay.
[280:33.80] So nothing like that for getPrivateKey,
[280:38.46] just for everything else.
[280:39.76] (keyboard clicking)
[280:47.12] (keyboard clicking)
[280:50.12] Okay, yeah.
[280:59.04] I think I will go back on the API
[281:02.00] for the getPrivateExtended
[281:03.88] and just have it eagerly create it.
[281:08.80] Otherwise, it's gonna be pure madness.
[281:12.92] (keyboard clicking)
[281:15.92] Okay, almost there, I think.
[281:31.92] That one technically doesn't need to have an await.
[281:41.96] (keyboard clicking)
[281:42.80] That one can...
[281:44.12] That one will throw right away,
[281:49.60] but I think...
[281:52.84] (keyboard clicking)
[282:10.00] Okay.
[282:11.40] So public key...
[282:14.84] Should not throw if the key is not compressed.
[282:24.76] I disagree.
[282:25.60] I think it should throw.
[282:26.64] But we'll cross that bridge when we get there.
[282:30.18] (keyboard clicking)
[282:33.22] (keyboard clicking)
[282:36.22] Okay.
[282:44.86] I don't think I'm gonna be able
[282:49.96] to finish this tomorrow, unfortunately.
[282:51.42] I'll have to wait till Saturday or next Monday.
[282:55.00] Or, I mean, the upcoming Monday.
[283:02.90] All right, where are we at?
[283:04.86] FromExtended, there's some awaits there.
[283:07.78] Versions, dev, dah, dah, dah, dah, dah, dah, dah, dah.
[283:13.50] HG, should getPrivateKey.
[283:16.30] Describe, it should work.
[283:20.22] Okay, fromExtendedKey.
[283:22.46] And that sign's gonna have to have it, of course.
[283:29.60] (keyboard clicking)
[283:32.60] Verify's gonna have to have it.
[283:36.24] (keyboard clicking)
[283:40.24] (keyboard clicking)
[283:43.24] All right.
[284:01.08] (keyboard clicking)
[284:07.94] (keyboard clicking)
[284:10.94] All right.
[284:24.70] Get more private keys.
[284:29.46] All right, we're past the halfway point
[284:33.10] in terms of having a wait
[284:36.50] in front of literally everything.
[284:38.18] Well, not literally everything.
[284:41.82] (keyboard clicking)
[285:05.80] Oh, master seed.
[285:07.72] Derive, derive, derive, derive.
[285:16.76] Wow, there's a ton of them.
[285:18.98] Who would've thought you'd have so many function calls
[285:22.84] in a code, what, in a code?
[285:26.74] Did I just say that in a program?
[285:29.82] Oh.
[285:32.80] (keyboard clicking)
[285:36.40] Okay, getPublicExtended, getPrivateExtended.
[285:41.40] Oh no.
[285:47.62] Oh, that's something I may not have been
[285:53.68] thinking about in other places.
[285:55.24] Wait, that's only allowed within async functions.
[286:01.52] Where is it not within an async function?
[286:03.68] On line 270?
[286:05.44] Let's go back and take a look.
[286:06.94] All right, 283.
[286:21.82] (keyboard clicking)
[286:24.82] Where are we at here?
[286:43.52] Okay, from master key.
[286:46.76] (keyboard clicking)
[286:49.76] Wiped key, verify.
[286:56.88] Extended key.
[287:02.60] All right, I think that's it.
[287:13.04] I think that's all of 'em.
[287:14.48] (keyboard clicking)
[287:17.48] Okay.
[287:19.72] Failed every single one of 'em.
[287:26.68] Well, almost.
[287:27.56] Okay, let's see.
[287:35.84] Derive, where's derive used?
[287:40.92] Where's derive child?
[287:44.84] (keyboard clicking)
[287:45.96] There's derive child, there's derive child.
[287:48.32] Okay, why is it not working?
[287:57.80] Let's go back to this, to the test,
[288:00.48] and look for derive.
[288:03.18] Okay, let's look inside of derive
[288:08.32] and see if there's anything that we're missing.
[288:10.62] (keyboard clicking)
[288:13.62] It's hardened.
[288:18.82] Set.
[288:21.38] Await.
[288:24.86] Await.
[288:33.70] Await.
[288:40.38] Await.
[288:41.22] Await.
[288:48.58] Await.
[288:49.42] Await.
[288:54.34] (keyboard clicking)
[289:08.42] Okay, should properly derive chain path.
[289:11.66] Derive.
[289:19.34] Hmm.
[289:38.38] (keyboard clicking)
[289:41.38] I mean, this looks right.
[289:50.94] So let's take a look at from master seed,
[289:54.02] get private extended,
[289:55.38] console.log,
[289:58.66] HD key,
[289:59.98] child key.
[290:03.16] (keyboard clicking)
[290:06.16] X-prove.
[290:11.04] (keyboard clicking)
[290:16.48] F not private.
[290:26.80] All right, let's try running this now.
[290:30.40] (keyboard clicking)
[290:33.40] Okay.
[290:35.76] Okay.
[290:46.68] Should properly derive.
[290:51.32] Hmm.
[290:58.72] (keyboard clicking)
[291:01.72] (keyboard clicking)
[291:04.72] (keyboard clicking)
[291:07.72] (keyboard clicking)
[291:10.72] (keyboard clicking)
[291:13.72] All right.
[291:41.16] (keyboard clicking)
[291:44.16] C and I.
[291:48.00] (keyboard clicking)
[291:52.16] I don't know what's going on here.
[292:09.28] Any thoughts, Chet?
[292:10.28] (keyboard clicking)
[292:14.64] (keyboard clicking)
[292:17.64] (keyboard clicking)
[292:20.64] (keyboard clicking)
[292:23.64] (keyboard clicking)
[292:26.64] (keyboard clicking)
[292:30.24] (keyboard clicking)
[292:33.24] (keyboard clicking)
[292:40.24] (keyboard clicking)
[292:53.16] (keyboard clicking)
[292:56.16] I'm gonna go back to ref.
[293:08.32] (keyboard clicking)
[293:20.36] (keyboard clicking)
[293:23.36] Okay.
[293:30.44] Get checkout ref uint8 array.
[293:32.32] Oh, get checkout ref async.
[293:37.72] Let's push that up.
[293:39.06] (keyboard clicking)
[293:42.06] All right, so it updated the types.
[293:49.24] So let's say that we don't do
[293:50.56] any of the script test stuff at all.
[293:52.56] (keyboard clicking)
[293:55.56] And then let's say that we just change entries here.
[294:03.96] For let I equals zero I plus an entries dot length.
[294:14.36] I plus equals one, do all the things.
[294:19.36] Let's equals entries I.
[294:28.28] (keyboard clicking)
[294:43.96] Interesting.
[294:44.80] (keyboard clicking)
[294:49.24] Hmm.
[295:06.22] Okay, let's take a look at the last one
[295:13.56] that was passing.
[295:14.50] So git stash.
[295:16.88] Huh.
[295:20.00] (keyboard clicking)
[295:23.00] So something kind of subtle is happening here.
[295:42.24] (keyboard clicking)
[295:45.24] Because literally the difference between this
[295:49.76] is a for each.
[295:50.60] That does not make sense.
[295:53.06] (keyboard clicking)
[296:00.32] Is there maybe a return in there?
[296:05.16] Ah, there's a turn that needs to be a continue.
[296:11.62] (keyboard clicking)
[296:12.46] This is the way.
[296:13.28] All right, that makes sense.
[296:16.10] NPM run test, ah yes.
[296:20.70] (keyboard clicking)
[296:23.70] For each, for and prep for async.
[296:30.54] (keyboard clicking)
[296:36.66] (keyboard clicking)
[296:39.66] Okay, check out ref async.
[297:00.22] (keyboard clicking)
[297:06.26] Okay.
[297:07.10] (keyboard clicking)
[297:13.26] (humming)
[297:28.54] Hey, we've come all the way around.
[297:30.94] We've exhausted a few hundred songs.
[297:33.70] Wow, that's crazy.
[297:35.60] (keyboard clicking)
[297:38.60] All right, I don't know what the difference
[297:47.28] between these two is really.
[297:48.78] If we just put a wait in front of here,
[297:53.00] are they the same thing?
[297:54.20] They look like the same thing.
[297:56.66] (keyboard clicking)
[298:01.88] (keyboard clicking)
[298:04.88] Just ghosting the machine, maybe?
[298:08.26] (keyboard clicking)
[298:12.24] Okay.
[298:21.00] So way more passing now.
[298:25.46] All right, it should throw an error.
[298:30.00] (keyboard clicking)
[298:33.00] Okay.
[298:58.94] Realm master seed.
[299:00.72] (keyboard clicking)
[299:05.70] Okay, the other thing was,
[299:27.40] (keyboard clicking)
[299:29.90] should fail.
[299:31.42] (keyboard clicking)
[299:34.42] (keyboard clicking)
[299:37.42] (keyboard clicking)
[299:40.42] (keyboard clicking)
[299:43.42] - What a firework.
[300:05.82] (keyboard clicking)
[300:08.82] (keyboard clicking)
[300:11.82] - Let me see what we can do here.
[300:23.08] So we want to assert that
[300:25.80] this function throws.
[300:30.72] (keyboard clicking)
[300:33.72] (keyboard clicking)
[300:36.72] Wait, can that even work?
[300:49.06] How do we assert that it throws?
[300:53.48] (keyboard clicking)
[300:56.48] (keyboard clicking)
[300:59.48] Hmm.
[301:16.40] Hmm.
[301:24.40] I don't know what we do about that.
[301:26.96] (keyboard clicking)
[301:29.96] So if not regex.test
[301:47.08] error,
[301:49.56] throw
[301:53.08] (keyboard clicking)
[301:56.08] No error.
[301:58.80] (keyboard clicking)
[302:03.80] So, should fail, good fail.
[302:17.32] (keyboard clicking)
[302:20.32] (keyboard clicking)
[302:23.32] I think this is basically it.
[302:34.76] (keyboard clicking)
[302:37.76] (keyboard clicking)
[302:40.76] Okay, do we have, does node have a
[303:01.60] async throw?
[303:04.52] (keyboard clicking)
[303:08.52] (keyboard clicking)
[303:11.52] Okay, assert.regex.
[303:17.04] Okay, there we go.
[303:18.86] That's what we need.
[303:21.08] So let's undo all that.
[303:23.20] (keyboard clicking)
[303:26.20] (keyboard clicking)
[303:29.20] (keyboard clicking)
[303:33.20] (keyboard clicking)
[303:36.20] (keyboard clicking)
[303:39.20] (keyboard clicking)
[303:42.20] (keyboard clicking)
[303:45.20] (keyboard clicking)
[303:48.30] Okay.
[303:49.14] (keyboard clicking)
[303:52.14] (keyboard clicking)
[303:55.14] Okay.
[304:20.24] (keyboard clicking)
[304:23.24] (keyboard clicking)
[304:26.24] (keyboard clicking)
[304:29.24] (keyboard clicking)
[304:32.24] (keyboard clicking)
[304:35.24] All right, let's try this one.
[305:02.22] Okay, we've only got one failing.
[305:04.26] And I think that that's just because
[305:07.78] wipe private data from here.
[305:12.78] (keyboard clicking)
[305:17.90] There we go.
[305:19.80] (keyboard clicking)
[305:23.02] So we gotta clean that up, but oh wait, nope.
[305:25.46] Should be able to verify signatures.
[305:30.12] Verify.
[305:33.18] (keyboard clicking)
[305:36.18] Hmm.
[306:00.68] (keyboard clicking)
[306:03.68] All right, so should be able to verify signatures.
[306:11.50] Full key sign hash.
[306:25.76] Wiped key verify.
[306:30.56] (keyboard clicking)
[306:33.56] Oh, whoops.
[306:38.84] There it is.
[306:39.66] (keyboard clicking)
[306:44.84] Oh, come on, still?
[306:50.54] I thought I got it.
[306:58.24] (keyboard clicking)
[307:01.24] Let's try this.
[307:24.96] Suspected sig.
[307:27.52] Okay, that's a little too,
[307:34.16] about 22 and then,
[307:36.98] nope.
[307:39.72] 272, 272.
[307:43.40] Okay.
[307:53.84] All right, and where was this problem?
[307:55.74] Verify.
[307:57.68] 346.
[308:00.36] Let's look for it on the test.
[308:03.70] 346 and then 269.
[308:06.36] 346.
[308:08.08] 346 hash.
[308:11.68] Sign hash.
[308:15.80] Okay, let's see if we can break that down.
[308:19.76] What was the other one?
[308:21.56] 269.
[308:23.84] 269.
[308:27.28] It makes it difficult to tell where an error's coming from
[308:29.76] when it's like this because, let's see.
[308:33.16] Public key hash.
[308:36.32] So verify hash and signature.
[308:38.84] Sign.
[308:40.48] ECDSA sign.signature.
[308:42.48] It seems like.
[308:45.26] (keyboard clicking)
[308:48.26] Give it a raise the hash.
[308:58.70] Okay.
[309:03.54] Sig.
[309:09.46] Let sig equals.
[309:11.22] (keyboard clicking)
[309:14.22] Probably the await.
[309:19.14] Hey!
[309:29.10] All right, cool.
[309:30.30] (air horn blaring)
[309:33.66] All right, so that's now.
[309:36.26] I need some cleanup, but.
[309:38.94] (air horn blaring)
[309:41.94] (keyboard clicking)
[309:45.02] (keyboard clicking)
[309:48.02] (keyboard clicking)
[309:51.98] (air horn blaring)
[309:54.98] (keyboard clicking)
[309:57.98] Okay.
[310:23.62] (keyboard clicking)
[310:26.62] Okay, so then what's left here?
[310:33.10] We have to do
[310:34.26] these two.
[310:37.46] We gotta do some cleanup.
[310:38.58] So we would do, for example,
[310:45.82] dash incubator.
[310:51.62] And then, I guess, we might as well for that one as well.
[310:54.46] (keyboard clicking)
[310:58.74] Whoops.
[311:12.82] (keyboard clicking)
[311:15.82] All right.
[311:31.54] This one's gonna become.
[311:40.58] (keyboard clicking)
[311:42.86] This is just gonna become part of dash keys.
[311:45.02] That's where that one's gonna go.
[311:46.70] This one's also gonna go into dash keys.
[311:48.86] This one's gonna stay separate.
[311:51.50] That'll be it.
[311:54.70] We'll bring the crypto stuff back in.
[311:58.86] So now that I've got all the test passing async
[312:01.10] without any of the crypto changes,
[312:02.98] I'm highly confident that I can get it passing
[312:05.62] with the crypto changes,
[312:06.62] 'cause now I actually know it's not
[312:09.66] just all the async stuff.
[312:11.26] Okay.
[312:17.54] But when we do the async await bit,
[312:25.86] I think that's also where
[312:28.82] some node is gonna fail more often now.
[312:33.62] Let's go ahead and just check.
[312:34.78] I just wanna see what happens here.
[312:37.50] Refactor async all the things.
[312:42.50] It's not gonna be here, we're gonna do it there.
[312:48.82] And we're gonna do it on main.
[312:50.42] All right, what else?
[313:01.26] (upbeat music)
[313:03.86] So we got the crypto.
[313:13.14] All right, that's not gonna like that anymore.
[313:20.02] And we got the tweak.
[313:20.86] We got the tweaking medoodle.
[313:23.30] Let me go check on the tweaking medoodle
[313:26.22] while I'm thinking about it.
[313:27.78] Noblesecp256k1.
[313:32.78] There we go.
[313:38.02] And then somebody in the issue
[313:40.34] was mentioning about the tweak.
[313:44.18] (upbeat music)
[313:46.78] (upbeat music)
[313:49.38] (upbeat music)
[313:51.98] Let's see.
[314:17.98] (upbeat music)
[314:20.58] Point add functions.
[314:23.90] (upbeat music)
[314:26.50] Let's see, sometimes I ask a question,
[314:43.58] then I find an answer and I put it in a comment.
[314:47.50] Hmm.
[314:48.34] 'Cause eventually I did find
[314:51.74] whatever it was he was talking about.
[314:55.66] So.
[315:07.86] (upbeat music)
[315:10.46] Okay.
[315:26.10] Secp256k1 tweak.
[315:32.54] Let's see.
[315:36.26] (upbeat music)
[315:38.86] All right, so we're gonna get that somehow.
[315:44.34] All right, async all the things.
[315:56.98] And it fails in node 10,
[316:00.46] which is no surprise.
[316:02.46] And I'm not doing anything with callbacks
[316:05.50] to support node 10.
[316:06.82] So it looks like node 10 just needs to drop off.
[316:09.06] There's so many little things that are kind of annoying.
[316:12.34] We can get all the way up to
[316:16.46] being able to replace the crypto with something else.
[316:21.56] And that's as far as we can go for node 10.
[316:26.70] Okay.
[316:30.78] (upbeat music)
[316:33.36] Let's see.
[316:39.14] I'm guessing it's because it's async is not a keyword.
[316:47.86] Text encoder is not defined, what?
[316:51.26] But I'm not using text encoder.
[316:54.38] Oh, it dash and give error.
[316:56.98] Okay.
[316:57.82] Interesting.
[317:00.18] (upbeat music)
[317:02.26] Okay, so async was available back in node 10.
[317:05.58] I don't believe that.
[317:07.46] Let's see, but text encoder.
[317:10.90] I don't think that I can.
[317:13.26] Let's see, RiveMD.
[317:14.82] Could we do something else for that?
[317:19.62] Could we?
[317:20.46] Nah, it's just not worth it.
[317:21.86] Okay.
[317:25.66] Cool, so basically at this point,
[317:27.48] what do we have left?
[317:29.42] Hold on.
[317:30.42] (upbeat music)
[317:33.00] Okay, so we need to get that over
[317:58.42] and then replace a few more.
[318:00.20] The couple of dependencies is not a big deal.
[318:04.30] So good at all working.
[318:06.46] Okay, so the next time I spend some time on this,
[318:10.20] it will get it working.
[318:11.94] Next time I'm able to spend some time on it,
[318:15.86] which hopefully will be, I don't know, maybe Monday.
[318:21.22] I've got some other stuff
[318:24.78] I need to do Friday and Saturday, I think.
[318:26.82] (upbeat music)
[318:29.40] Okay.
[318:54.22] (upbeat music)
[318:56.80] Update RiveMD 160
[319:03.72] to work in browsers, UN8 array.
[319:13.28] So this one is done.
[319:16.04] (upbeat music)
[319:18.62] Update.
[319:24.86] (upbeat music)
[319:25.98] BS 58, check.
[319:29.06] To work in browsers.
[319:31.96] Work is at dash incubator.
[319:37.52] Base 58, check.
[319:41.12] (upbeat music)
[319:43.70] (keyboard clicking)
[319:46.70] (keyboard clicking)
[319:50.70] (keyboard clicking)
[319:53.70] (keyboard clicking)
[319:58.08] (keyboard clicking)
[320:09.00] (keyboard clicking)
[320:12.00] Okay.
[320:35.96] Well, sorry, this has been a lame stream,
[320:40.32] but can't be all winners all the time.
[320:44.08] And it kind of sucks that it started out with no audio,
[320:46.36] but what do you do?
[320:48.32] Such is life.
[320:50.00] Okay, I'm gonna pause the music.
[320:53.68] I'm gonna do something, I'm gonna stop the this my Bob.
[320:59.56] I'm gonna, I don't know what else I'm gonna do,
[321:01.80] but I'm gonna peace out.
[321:05.40] A little bit more fanfare, maybe.
[321:08.28] ♪ This was a triumph ♪
[321:11.98] ♪ I'm making a note here, huge success ♪
[321:16.98] All right.
[321:18.14] All of the, the only thing that has
[321:25.56] a question mark by it at this point,
[321:27.68] 'cause we know the web crypto stuff
[321:30.92] is pretty highly likely to work.
[321:34.48] And we've already got it done.
[321:35.88] I mean, assuming that the algorithm's the same,
[321:38.96] and we could probably get around that stupid HMAC problem
[321:43.78] just by doing a digest that,
[321:46.02] that hashes the two things together.
[321:51.68] 'Cause I'm pretty sure that's all HMAC is,
[321:53.44] is just when you hash data and then hash the secret
[321:58.44] and then hash the data, you know,
[322:02.16] do an update on the digest.
[322:04.48] So just concatenate those together.
[322:06.20] And I'm, I think that's what an HMAC is anyway.
[322:08.76] So there's that.
[322:11.28] And then there's the, there's the, this one,
[322:14.40] this one, just getting that,
[322:15.72] figuring out where that tweak function is.
[322:18.26] And Dagnabit, I know I found it somewhere.
[322:20.62] Now I don't know where it is.
[322:22.08] Why don't you take one more quick look at that?
[322:26.04] Because, let's see, is there anywhere I am the author?
[322:31.04] No.
[322:31.88] I know there's a few where I'm the author.
[322:37.60] Okay, clarify usage of this compressed pull request.
[322:41.96] Oh wait, what?
[322:51.08] Oh, this looks good.
[322:57.28] (keyboard clicking)
[323:00.28] Nice, that's really nice.
[323:11.54] That's great.
[323:16.92] Look at that.
[323:17.76] Remove features.
[323:20.84] Ooh, ooh.
[323:23.60] How nice.
[323:24.44] (keyboard clicking)
[323:27.44] Ah, well, we'll have to see, because we may need.
[323:36.28] I can take away the snore, that's fine,
[323:50.40] but there's some stuff we need.
[323:53.16] (keyboard clicking)
[323:56.16] Yay.
[324:08.08] All right, cool.
[324:16.70] Yay.
[324:20.84] (keyboard clicking)
[324:23.84] Oh no.
[324:28.92] That's actually, I don't know that we want that.
[324:35.24] I think that having the ASN1 bytes is good.
[324:42.46] (keyboard clicking)
[324:45.46] Okay, recovery bit.
[324:53.78] Okay, it's not called quadrant, it's called recovery bit.
[324:56.62] (keyboard clicking)
[325:00.62] Okay.
[325:10.98] (keyboard clicking)
[325:13.98] That's not, during coding is literally,
[325:24.70] it's, well, it's super simple, so if this is what we get,
[325:30.78] it's literally just having a varint encoding of the length,
[325:40.10] so we can still do that if we do decide to upgrade.
[325:44.34] Verify strict.
[325:47.14] Recover public key.
[325:52.66] Oh, I don't know if I like that, but whatever.
[326:07.22] Okay, probably won't be able to use this
[326:10.90] because the names of things might've been changed.
[326:14.94] Well, let's see, does this still have the tweak?
[326:17.86] Let's see.
[326:18.70] Index.ts, does it still?
[326:24.54] Can we just look at that?
[326:31.30] (keyboard clicking)
[326:34.30] Well, that's great.
[326:38.44] That's so awesome that he's dropping the big int library.
[326:43.44] That's just great.
[326:47.04] Remove craft, remove features.
[326:54.62] Keep it nice and tight.
[326:56.40] Okay, switch to noble curbs.
[327:00.50] (keyboard clicking)
[327:04.06] All right, that's cool.
[327:07.86] Hmm.
[327:18.50] Yeah, that problem.
[327:28.20] (keyboard clicking)
[327:31.20] Add library to important projects.
[327:40.52] Cosmos.
[327:45.82] Nice, okay.
[327:57.34] But what I needed to know,
[327:58.94] let's see if we can still find tweak.
[328:06.30] No, or add.
[328:08.48] Is there an add?
[328:10.62] There is an add.
[328:13.66] Okay, what about, what about, was it in the test?
[328:23.98] Where was it?
[328:26.66] Tweak, tweak utils.
[328:29.54] Here it is, tweak utils.
[328:30.82] Private add.
[328:31.66] This is, this is it.
[328:33.34] This is what we need.
[328:35.02] Private, tweak utils, private add,
[328:38.54] and point add scaler.
[328:42.74] So let me go back here.
[328:46.26] I don't know, I don't think that.
[328:54.06] Okay, so then if I look here,
[328:56.62] where's the tweak?
[328:59.42] Tweak.
[329:02.14] Public key tweak add.
[329:06.26] (keyboard clicking)
[329:09.26] Private key tweak in hex.
[329:31.16] So let's see.
[329:33.34] (keyboard clicking)
[329:36.34] Okay.
[329:37.94] Private key, and that's, this is the tweak,
[329:41.54] is the IL, right?
[329:43.82] Create HMAC, yeah.
[329:45.04] So here's the tweak.
[329:46.14] The tweak is IL, so we can get that in hex.
[329:49.30] So that we can pass that in.
[329:53.86] (keyboard clicking)
[329:58.30] (keyboard clicking)
[330:01.30] And then private key.
[330:09.58] Okay.
[330:17.46] I think, I think this is it, point add scaler.
[330:25.54] I think this is public.
[330:28.22] Let's see, P is hex, tweak is hex, compressed.
[330:31.90] If we look here, key, tweak, and compressed.
[330:36.90] So I'm pretty sure that's public.
[330:41.98] And it's called tweak add, not tweak multiply.
[330:47.30] So I think that's it.
[330:48.62] I think that we can replace it,
[330:53.10] maybe not with, maybe with the latest version,
[330:55.34] maybe, I don't know.
[330:57.34] I'm not sure if we're going to replace it
[331:01.10] with the latest version or not,
[331:02.66] but we should be able to replace it
[331:04.98] with the current version that we had from a month ago.
[331:09.26] And then we can look at using the updated version later.
[331:14.14] All right, now I'm really, really, really,
[331:15.58] really, really, really, really, really out.
[331:17.46] Adios.