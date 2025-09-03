# Instructions

## FOR GEMINI code asistant gemini-cli 

copy content of file memory-bank.md

### 1. LOCAL PROJECT

 init code asistant gemini its create a GEMINI.md FILE
 copy content of memory-bank.md and paste in first of all content
 or you can add a line "Read first memory-bank.md and follow steps"

### 2. LOCAL WITH COMANDS

in your local project folder create or open a .gemini\commands folder 
copy memory-bank.md and done you can rename file like load-memory.md 
you need edit the file and add at first line the command config 
```
---
name: load-memory
description: initialize the memory-bank for this project
---
```

and type in your code asist /load-memory and its create a local memory-bank folder with all data
about yout project
Like optional **You can create a global command follow the same step but in the global user folder 
like bellow 


### 3. GLOBAL for ALL Projects 

go to yout folders user
windows: c:\users\USUARIO\.gemini
linux / mac : ~/.gemini 

open or create GEMINI.md and paste content of file memory-bank.md inside
and DONE!
each time run gemini cli code asistant its READ GEMINI.md on main folder
