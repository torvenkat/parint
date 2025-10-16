---
date: 2025-10-15
title: Speed up old Mx MacOS machines under Tahoe
tags:
  - macos
---
New iteration of MacOS (Tahoe) significantly slows down older macs.  I have an M1 Air and it is now very slow. 

The fix is to disable Glass. In a terminal: 

`defaults write -g com.apple.SwiftUI.DisableSolarium -bool YES`

This gets rid of the slow animations, inconsistent window cornering, and other annoyances.

Then  do this so that menus aren't transparent and unreadable: 

`System Settings > Accessibility > Display > Reduce Transparency`

If for some reason you ever want to sacrifice performance and get the glass desktop back, you change the YES to NO in the Terminal command. 