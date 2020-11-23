These are simple syntax highlighters for the NIL and Neil languages. Both files are merely modified versions of the Lua highlighter (since both languages are merely extensions of Lua, that was the easiest way to go)

Now in order to get this to work you need to do two things. First of all you need to add two files to the "modes" directory of jEdit. Which is in Windows "C:\Program Files\jEdit\modes", I do not know how this is done on other 
platforms, as I simply didn't look that up. These two XML files should then be added to this folder.

It doesn't end there however, these two lines must be added to the file "catalog" which is located in the same folder somewhere between the lines <MODES> and </MODES>

~~~xml
<MODE NAME="NIL" FILE="nil.xml" FILE_NAME_GLOB="*.nil">
<MODE NAME="Neil" FILE="neil.xml" FILE_NAME_GLOB="*.neil">
~~~

Please note that for many languages 2 lines are used and I guess it goes without saying you shouldn't mess those definitions up. If you are really unsure (you shouldn't be coding if you are, I think) just add them as last lines 
before \</MODES>

Now stuff as collapsing and function outlining is not supported this way, but at least you'll have syntax highlighting this way, and that counts for a lot already, eh?



