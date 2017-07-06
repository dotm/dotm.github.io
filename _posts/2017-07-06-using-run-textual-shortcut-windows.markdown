---
layout: post
title: "[Technical Tips] Using run as textual shortcut for Windows software and file"
---

Do you know you can open shortcut files (.lnk files) with Run?

I used to think that the most efficient way to open software is using the custom Windows keyboard shortcut. It IS fast. But there’s only so much keys that you can use. Plus, sometimes, somehow, the keyboard shortcut will be reset automatically to None, and then you’ll have to set the shortcut again.

And then I realize that I can use the Run command (Windows+R) in Windows to launch software.

1. Create a folder in your desktop (I personally named it “Links”)
2. Add that folder to Windows PATH
3. Put shortcuts in that folder and rename the shortcuts to make it shorter (e.g. rename “chrome” to “c”)
4. Then you can use the Run command to run all the things inside that folder (e.g. to run chrome, I press Windows+R, type “c”, hit Enter)

If you don’t have the Windows key, you can just set the keyboard shortcut for the Run command. (I personally set it to Ctrl+Alt+Left)

This way you can open all software you want with just a few keystrokes. The benefits against the alternatives:

- vs. keyboard shortcut: no need to reset the keyboard shortcut and you can use more than one character (I use “n” for Sticky Notes and “np” for Notepad++)
- vs. Desktop shortcut: your desktop will be clean (the only thing you should put in your Desktop is one folder, the “Links” folder)
- vs. Windows Search: marginally quicker and can reach unindexed folders
- Aside from running software (.exe, .lnk) You can use it to run scripts (.bat, .reg), use the default run command (ncpa.cpl, regedit, cmd, powershell), open files (even if those files are not located in drive C), etc.
