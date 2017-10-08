---
Title: System and Cyber Security
Date: 27-01-2017 to 15-4-17
Members: Kamlesh K Biloniya, Divya chauhan, Chaman Agrawal, Kushagra Rajput
Mentors: Siddarth Krishnamoorthy & Soumye Singhal
---

* **Abstract:**  this  project was about learning, exploring and exploiting various security vulnerability in a program.  Project was mostly based on system vulnerabilities under “old-style” Linux system.

     Contents:
     * **Basic linux command**
     * **ssh login**
     * **Assembly Language**
     * **Buffer overflow attack**
     * **Format string attack** <br />
     
* **Linux Basics**
         **Read, Write & Execute Permissions** <br />
         Permissions are the basic "rights" to act on a file or directory. The basic rights are read, write and execute.
         * Read - a readable permission allows the contents of the file to be viewed
         * Write - a write permission on a file allows you to modify the contents of that file.
         * Execute - for a file, the executable permission allows to run the file and execute a program.
         * We can view permissions for file for directory by ls –l command.
         
![](https://github.com/kamleshhello/Ethical-Hacking/blob/master/git1.png)<br />
*Some example of basic commands*
![](https://github.com/kamleshhello/Ethical-Hacking/blob/master/git2.png)<br />
* **SSH (the Secure Shell)**
    * Using SSH requires a client on the local computer and a server on the remote one.<br />
    * It establishes an encrypted connection to a remote computer, executes a command there and redirects its input and output across the connection. 
![](https://github.com/kamleshhello/Ethical-Hacking/blob/master/git3.png)
* **Assembly Language**
    * Assembly language is a low-level programming language.
    * Assembly language is converted into executable machine code by an assembler.
    * Computer basically consist of two things: CPU and memory.
    * And there is some internal memory (registers) only accessible to CPU.
![](https://github.com/kamleshhello/Ethical-Hacking/blob/master/git4.png)
* **Some Assembly Instructions**
    * mov eax, ebx — copy the value in ebx into eax
    * push eax — push eax on the stack
    * lea eax, [var] — the value in var is placed in EAX.
    * jmp begin — Jump to the instruction labeled begin
![](https://github.com/kamleshhello/Ethical-Hacking/blob/master/git5.png)
![](https://github.com/kamleshhello/Ethical-Hacking/blob/master/git6.png)
![](https://github.com/kamleshhello/Ethical-Hacking/blob/master/git7.png)
* **Buffer overflow**
    * **Buffer:** A  Temporary space in memory used for hold data.
    * **Buffer overflow:** Happens when data written to the buffer is larger then size of buffer and due to insufficient bound checking it overflows and overwrites adjacent memory location.<br />
    * **Simple Vulnerable Function:**<br />
        GetInput{ <br />
                  Char buffer[8];<br />
                  gets(buffer);<br />
                  puts(buffer);<br />
}
   <br />
            **Gets() does not check if input size is greater than size  of buffer**
* **Format String Attack:**
    * The Format String exploit occurs when the submitted data of an input string is evaluated as a command by the application. Using format String vulnerability we can read the stack , execute  code .
    * Format string vulnerable function:- gets(),scanf(), printf() ,Strcpy() , strcat() ….etc(they don't check size of input or output)
    * Format parameters :-
    * %n  Write an integer to the location in the process memory  
    * %x    Read data from stack
    * %s  Read character string from process memory
    
         **Continue..........
         With summer project**
* **Pwntools**
    * Written in python
    * CTF framework
    * Makes exploitation easy
    * >>> from pwn import *   # it imports a lot of functionality into global namespace
    * >>> p=process('/bin/sh') # starts process 
    * >>>p.sendline('input')     # sends input
    * >>>p.recvline(timeout=5) # receives output 
* **Canaries:**
    * Canaries are stack guard
    * Used to check stack buffer overflow
    * But there are many techniques to bypass canaries
* **Shellcode injection and ROP**
    * Exploiting to execute your own code with Root permission 
           Three step Procedure :
           * Crafting shellcode
           * Injecting shellcode
           * Modify Execution flow –Run the shellcode 
![](https://github.com/kamleshhello/Ethical-Hacking/blob/master/git8.png)
* **Web Based  Attack**
    * CSRF (Cross-site request forgery)
    * XSS  (Cross site scripting ) Attack
         1. reflected xss attack
         2. stored xss attack
         3. DOM-based xss attack
![](https://github.com/kamleshhello/Ethical-Hacking/blob/master/git9.png)


