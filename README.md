# GlobalReplace
A bash script that can perform a global text replace on multiple files

If arguments are specified:

rep will globally replace a pattern with another string for the files specified on the command line.
For example:

   rep sorce source myFile1.txt
   rep sorce source myFile1.txt myFile2.txt myFile3.txt
   rep sorce source myFile*
   rep sorce source ../../*/files/myFile*

will change every occurance of "sorce" to "source" in every file specified.

   rep "'fred' 'bert'" "'fred' 'ernie'" myFile1.txt

This replaces: 'fred' 'bert'
with:          'fred' 'ernie'


If no arguments are specified:

rep enters interactive mode and will prompt the user to enter a filename path. Here there is the advantage that wild cards may be used, so the script can work on several directories, or files with a common suffix, rather than a common prefix. rep then presents the user with options to view the lines within the files which will be affected. It is then possible to abort the pattern replacement operation should an unforseen undesireable operation take place.

rep is _case_sensitive_!

WARNING: rep will overwrite the original files!
