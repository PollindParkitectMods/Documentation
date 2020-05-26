---
id: logging
title: Logging
sidebar_label: Logging
---

## UnityEngine.Debug.Log
The Unity way of logging is via [`UnityEngine.Debug.Log(...)`](https://docs.unity3d.com/ScriptReference/Debug.Log.html) and its [variants](https://docs.unity3d.com/ScriptReference/Debug.html). The log file is `Parkitect\Parkitect_Data\output_log.txt`. Uncatched exceptions are logged to that file too (with their StackTrace).
The log file's created new every time Parkitect starts. New messages are added at the end of the file when they are logged. That means you must reload the file in your text editor to see new logs. Some text editors can auto-refresh a file when it changed (e.g. Notepad++ with a "Document monitor" plugin).  


Besides opening the log file in a text editor, a debug console with the log messages and exceptions can be brought up in Parkitect by hitting `Ctrl+Alt+D`. However that window only displays messages that are logged while it's open.  
![Debug Console](https://raw.githubusercontent.com/Craxy/Parkitect-DebugMods/master/docs/wiki/img/DebugConsole.png)