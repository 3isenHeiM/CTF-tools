# Cheatsheet

## Webapps

* Check for headers

Strings manipulation :
* base64 encoded ?
  `echo $STRING | base64 --decode`
  
Scan all files in a website : 
  `dirb http://$WEBSITE$ (-p $PROXY)`
  
  
 Get the list of words to build a dictionnary : 
  ``cewl http://$WEBSITE`
  
 Try a dictionnary on a password :
  Set brup as INTRUDER, and set the pOST request and then the payload as a list of words
  
  
 Brute force a wp-login
  * Create the dictionnary
  * wpscan -u $SITE --proxy $PROXY --username=*USERNAME --wordlist=$DICTIONNARY
  
  
  Fidn a directory where the current user has write access : 
  `find / -writable -type d 2>/dev/null`
  
  
  In a program, always chec that the commands are mentionned from the base name : /bin/bash/CAT and not simply cat.
  Otherwise, write a file containig only "/bin/sh" and add it in first to the PATH : 
   export PATH=FILE:$OLD_PATH
   
   `strings` will display printable string of a file (useful when executables)

