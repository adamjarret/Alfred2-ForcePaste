Force Paste 
=============

**Force Paste** is an **[Alfred 2](http://www.alfredapp.com/) Workflow** that can be used to 
"paste" text into stubborn password prompts by sending a keypress event for each character
in the contents of the clipboard. 

Installation
-------------
Double click the **Force Paste.alfredworkflow** file and follow the prompts in
[Alfred 2](http://www.alfredapp.com/) to import the workflow.

The Script
-------------
The workflow is set to pass the contents of the clipboard to the AppleScript function.

    on alfred_script(q)
      delay 0.1
      repeat with n in (characters of q)
	      tell application "System Events" to keystroke n
	      delay 0.1
      end repeat
    end alfred_script