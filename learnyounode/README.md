# javascripting

from [nodeschool](https://nodeschool.io/index.html)

# LEARN YOU THE NODE.JS FOR MUCH WIN!  

## HELLO WORLD (Exercise 1 of 13)  

Write a program that prints the text "HELLO WORLD" to the console  
(stdout).  

─────────────────────────────────────────────────────────────────────────────  

## HINTS  

To make a Node.js program, create a new file with a .js extension and  
start writing JavaScript! Execute your program by running it with the node  
command. e.g.:  

  `$ node program.js`  

You can write to the console in the same way as in the browser:  

  `console.log("text")`

When you are done, you must run:  

  `$ learnyounode verify program.js`  

to proceed. Your program will be tested, a report will be generated, and  
the lesson will be marked 'completed' if you are successful.  


## BABY STEPS (Exercise 2 of 13)  

 Write a program that accepts one or more numbers as command-line arguments  
 and prints the sum of those numbers to the console (stdout).  

─────────────────────────────────────────────────────────────────────────────  

## HINTS  

 You can access command-line arguments via the global process object. The  
 process object has an argv property which is an array containing the  
 complete command-line. i.e. process.argv.  

 To get started, write a program that simply contains:  

    `console.log(process.argv)`

 Run it with node program.js and some numbers as arguments. e.g:  

    `$ node program.js 1 2 3 `

 In which case the output would be an array looking something like:  

    `[ 'node', '/path/to/your/program.js', '1', '2', '3' ]`  

 You'll need to think about how to loop through the number arguments so  
 you can output just their sum. The first element of the process.argv array  
 is always 'node', and the second element is always the path to your  
 program.js file, so you need to start at the 3rd element (index 2), adding  
 each item to the total until you reach the end of the array.  

 Also be aware that all elements of process.argv are strings and you may  
 need to coerce them into numbers. You can do this by prefixing the  
 property with + or passing it to Number(). e.g. +process.argv[2] or  
 Number(process.argv[2]).  

 learnyounode will be supplying arguments to your program when you run  
 learnyounode verify program.js so you don't need to supply them yourself.  
 To test your program without verifying it, you can invoke it with  
 learnyounode run program.js. When you use run, you are invoking the test  
 environment that learnyounode sets up for each exercise.  


## MY FIRST I/O! (Exercise 3 of 13)  

  Write a program that uses a single synchronous filesystem operation to  
  read a file and print the number of newlines (\n) it contains to the  
  console (stdout), similar to running cat file | wc -l.  

  The full path to the file to read will be provided as the first  
  command-line argument (i.e., process.argv[2]). You do not need to make  
  your own test file.  

 ─────────────────────────────────────────────────────────────────────────────  

## HINTS  

  To perform a filesystem operation you are going to need the fs module from  
  the Node core library. To load this kind of module, or any other "global"  
  module, use the following incantation:  

     var fs = require('fs')  

  Now you have the full fs module available in a variable named fs.  

  All synchronous (or blocking) filesystem methods in the fs module end with  
  'Sync'. To read a file, you'll need to use  
  fs.readFileSync('/path/to/file'). This method will return a Buffer object  
  containing the complete contents of the file.  

  Documentation on the fs module can be found by pointing your browser here:  
  file:///usr/lib64/node_modules/learnyounode/node_apidoc/fs.html  

  Buffer objects are Node's way of efficiently representing arbitrary arrays  
  of data, whether it be ascii, binary or some other format. Buffer objects  
  can be converted to strings by simply calling the toString() method on  
  them. e.g. var str = buf.toString().  

  Documentation on Buffers can be found by pointing your browser here:  
  file:///usr/lib64/node_modules/learnyounode/node_apidoc/buffer.html  

  If you're looking for an easy way to count the number of newlines in a  
  string, recall that a JavaScript String can be .split() into an array of  
  substrings and that '\n' can be used as a delimiter. Note that the test  
  file does not have a newline character ('\n') at the end of the last line,  
  so using this method you'll end up with an array that has one more element  
  than the number of newlines.  
## MY FIRST I/O! (Exercise 3 of 13)  

   Write a program that uses a single synchronous filesystem operation to  
   read a file and print the number of newlines (\n) it contains to the  
   console (stdout), similar to running cat file | wc -l.  

   The full path to the file to read will be provided as the first  
   command-line argument (i.e., process.argv[2]). You do not need to make  
   your own test file.  

  ─────────────────────────────────────────────────────────────────────────────  

## HINTS  

   To perform a filesystem operation you are going to need the fs module from  
   the Node core library. To load this kind of module, or any other "global"  
   module, use the following incantation:  

      var fs = require('fs')  

   Now you have the full fs module available in a variable named fs.  

   All synchronous (or blocking) filesystem methods in the fs module end with  
   'Sync'. To read a file, you'll need to use  
   fs.readFileSync('/path/to/file'). This method will return a Buffer object  
   containing the complete contents of the file.  

   Documentation on the fs module can be found by pointing your browser here:  
   file:///usr/lib64/node_modules/learnyounode/node_apidoc/fs.html  

   Buffer objects are Node's way of efficiently representing arbitrary arrays  
   of data, whether it be ascii, binary or some other format. Buffer objects  
   can be converted to strings by simply calling the toString() method on  
   them. e.g. var str = buf.toString().  

   Documentation on Buffers can be found by pointing your browser here:  
   file:///usr/lib64/node_modules/learnyounode/node_apidoc/buffer.html  

   If you're looking for an easy way to count the number of newlines in a  
   string, recall that a JavaScript String can be .split() into an array of  
   substrings and that '\n' can be used as a delimiter. Note that the test  
   file does not have a newline character ('\n') at the end of the last line,  
   so using this method you'll end up with an array that has one more element  
   than the number of newlines.  