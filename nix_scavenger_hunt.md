# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox.
*Paste the output of the `pwd` command here:*
/home/cabox/workspace  

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*
LICENSE          nix_scavenger_hunt.md                 
README.md        nix_scavenger_hunt_stretch.md         
challenge_files  

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*
total 36K                                              
drwxrwxr-x 4 cabox cabox 4.0K Jan 12 11:32 .           
drwxr-xr-x 9 cabox cabox 4.0K Jan 12 11:32 ..          
drwxrwxr-x 8 cabox cabox 4.0K Jan 12 11:32 .git        
-rw-rw-r-- 1 cabox cabox 1.1K Jan 12 11:32 LICENSE     
-rw-rw-r-- 1 cabox cabox 1.4K Jan 12 11:32 README.md   
drwxrwxr-x 7 cabox cabox 4.0K Jan 12 11:32 challenge_fi
les                                                    
-rw-rw-r-- 1 cabox cabox 5.6K Jan 12 11:38 nix_scavenge
r_hunt.md                                              
-rw-rw-r-- 1 cabox cabox  317 Jan 12 11:32 nix_scavenge
r_hunt_stretch.md  
It shows more information about each file in long list format,rather than just listing out the names of each. 

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/)Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*
-a, --all
       do not ignore entries starting with .
-l     use a long listing format
-h, --human-readable
       with -l, print sizes in human readable format (e.g., 1K 234M 2G)
	   
* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*
bin   etc       lib    mnt   root  srv  usr            
boot  fastboot  lib64  opt   run   sys  var            
dev   home      media  proc  sbin  tmp  

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*
/home/cabox  

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*
/home/cabox 

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*
Two .demo files:
cloaked-wookie.demo                            
scooter-double-mamba.demo

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
/home/cabox/workspace     

* Press the up arrow on your keyboard. *What just happened?*
reenters the last command you put in

* Press the up arrow a few more times. *What do you see?*
it goes through all the previous commands you entered chronologically 

* Run the `history` command. *What do you see?*
A summary of all the commands I have done in this session. 
   1  ls                                                               
    2  pwd                                                              
    3  cd challenge_files                                               
    4  ls                                                                                                                      
    6  ls                                                               
    7  pwd                                                              
    8  ls                                                                                                                            
   10  cd ..                                                            
   11  pwd                                                              
   12  history 

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
cadbox

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
no, it says:
cabox    pts/0        Jan 13 15:15 (54.69.152.243)

* How long has your system been running? Use `uptime` to see, and *paste the result here:*
 15:23:07 up 9 min,  1 user,  load average: 0.00, 0.00, 0.00
 
* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
It is a list of the active processes running. It reminds me of the task manager for windows showing all of the processes and how heavily they are taxing the system. 

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*
It provides the current and ongoing look at processor activity including cpu and memory usage. 

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*
2 files:
credit_cards.txt                                                                           
credit_cards2.txt

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
Last Updated: January 15 2015

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
./tmp/modi_laboriosam.txt    

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
Two Files: 
/home/cabox/workspace/challenge_files/Britt-Erdman.user:O'Harachester, WA
 37261                                                                   
/home/cabox/workspace/challenge_files/Lissie-Strosin.user:Jewessfurt, WA 
00816-7241  

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*
/home/cabox/workspace/challenge_files/serial-numbers/eaque_molestiae.txt:
Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut 
est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel
 esse blanditiis dolorem culpa non quia. 

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
it shows a list of options:
Options:                                                                              
  -d        display help instead of ring bell                                         
  -f        count logical, rather than screen lines                                   
  -l        suppress pause after form feed                                            
  -p        suppress scroll, clean screen and disblay text                            
  -c        suppress scroll, display text and clean line ends                         
  -u        suppress underlining                                                      
  -s        squeeze multiple blank lines into one                                     
  -NUM      specify the number of lines per screenful                                 
  +NUM      display file beginning from line number NUM                               
  +/STRING  display file beginning from search string match                           
  -V        output version information and exit 
  
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
it shows a list of the files all on one page, with the date and size, here is the top:
total 460K                                                                            
drwxrwxr-x 7 cabox cabox 4.0K Jan 14 11:42 .                                          
drwxrwxr-x 4 cabox cabox 4.0K Jan 12 11:32 ..                                         
drwxrwxr-x 2 cabox cabox 4.0K Jan 12 11:32 01                                         
-rw-rw-r-- 1 cabox cabox    0 Jan 12 11:32 2015_special_stuff.demo                    
-rw-rw-r-- 1 cabox cabox   93 Jan 12 11:32 Afton-Jast.user                            
                      
  
* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*
root       544  0.0  0.6  63876  3344 ?        Ss   11:39   0:00 sshd: ca
box [priv]                                                               
cabox      546  0.0  0.2  64012  1496 ?        S    11:39   0:00 sshd: ca
box@notty                                                                
cabox      547  0.0  0.1  12920   892 ?        Ss   11:39   0:00 /usr/lib
/openssh/sftp-server                                                     
root       562  0.0  0.6  63876  3344 ?        Ss   11:46   0:00 sshd: ca
box [priv]                                                               
cabox      564  0.0  0.2  64012  1500 ?        S    11:46   0:00 sshd: ca
box@notty                                                                
cabox      565  0.0  0.1  13048   972 ?        Ss   11:46   0:00 /usr/lib
/openssh/sftp-server                                                     
root       568  0.0  0.6  63876  3492 ?        Ss   11:49   0:00 sshd: ca
box [priv]                                                               
cabox      570  0.0  0.2  63876  1472 ?        S    11:49   0:00 sshd: ca
box@pts/0                                                                
cabox      571  0.0  0.3  18124  2016 pts/0    Ss   11:49   0:00 -bash   
cabox      581  0.0  0.2  15520  1144 pts/0    R+   11:50   0:00 ps aux  
cabox      582  0.0  0.1   8816   764 pts/0    S+   11:50   0:00 grep --c
olor=auto cabox
