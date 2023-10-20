**BANDIT 0**
---
 Simply need to connect to the network using ssh(SECURE SHELL )- ssh username@host -p port

**BANDIT 1**
---

Next level introcued a dashed file(-). To open it use cat <-

**BANDIT 2**
--- 

To open file with spaces in between either use
   1.cat "____"
   2.cat "spaces\ in\ between" 

**BANDIT 3**
---

To read files that are hidden we cant simply use ls beacuse it only shows non-hidden files. To expose the hiiden ones use (ls -a)

**BANDIT4**
---

To identify which file is human readable aka(ASCII) , we can use file command.If multiples files ina directory need to be searched use file ./* .
   1. file -shows the type of file.
   2. ./ showing current directory
   3. (*) for the command to apply to all files.

**BANDIT5**
---

To look at the size of file we use : du -b -a 

   1.du -to reveal size
   2.b - to reveal the size of files or directories in bytes
   3.a -to simply include all files and directory

**BANDIT6**
---

to find something stored in a server we use (find) and to characterise what we are looking for we add to the format file / -option expression 

   1. -user to specify a user
   2. -group to specify a group
   3. -size to specify size criteria and add c at the end to measure in bytes.
   4. 2>/dev/null - 2> is to redirect specifically standard error files and dev/null is used to discard any data sent to it.Main advantage of using it is to clean up all the waste denied messages

**BANDIT7**
---

Open a file and search the password next to a word- use | grep (word) .

**BANDIT8**
---
To pint point a line amongst many ,we use sort and uniq .

sort (file) -arranges all the lines in alphabetical order
|uniq -u  it serches for lines which only repeats only once.

**BANDIT9**
---

Since using file command revealed what the file contained was (data) and we need human readable text: strings (filename) - strings command is used to extract human readable strings from binary files.

**BANDIT10**
---

To convert base64 to ASCII - (base64 -d <<< "_____") 

OR simply use: echo __________base64encoded___ |base64 -d : echo basically prints what comes after it as text to terminal and | takes it out and gives it to next command ie base64 and -d decodes and it.

**BANDIT11**
---

since we have to rotate the alphates by 13 positons, we have to use ROT13 :cat filename | tr 'A-Za-z' 'N-ZA-Mn-za-m'

**BANDIT12**
---

first as per description ,create directory to store the data temporarily : mkdir /tmp/name
then copy the file from home directory to current - cp ~/filename (~/ :represent homedirectory to current directory

then to understand what kind of file: file (name)

  1.if it came as gzip; change the file to gzip format by :mv filename filename.gz

  then decompress it using: gzip -d filename.gz

  2.if came as bzip2 : mv filename filename.bz2

  then decompress using: bzip2 -d filenmae.bz2

  3. if came as POSIX tar archive (GNU) : mv filename filename.tr

     decompress using :tar -xf filename.tr

which revealed flag as ASCII at end

**BANDIT 13**
---
login password:wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw 

To connect to a server using private key use: ssh -i (privatekey) username@host -p 

After entering , you can open the file given in the task to reveal the password for level 14

bandit14 pass:fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq


**BANDIT 14**
---

nc - hostname port {command used to read and write data on a local network}

bandit15 pass :jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt


**BANDIT 15**
---

TO connect to aserver connecting to a local host- openss s_client -connect (hostname):port - (where s_client: is used to work with ssl tasks and interact with it)

bandit16 pass:JQttfApK4SeyHwDlI9SXGR50qclOAil1


**BANDIT 16**
---

nmap [Scan Type(s)] [Options] 3{target specification}  . where sV is used to probe open for info.

to scan whihc has the ssl we use nmap with sV-which tells it to do a detection scan : nmap sV (hostname) -p range

* if everything showns unknown use : nmap -A localhost -p range

* after connect to it using openssl s_client _connect localhost:port

* then save it into a new file

WHAT IS SSL- The SSL protocol, which stands for Secure Sockets Layer, is a cryptographic protocol designed to provide secure communication over a computer network.

* after saving ,open bandit 17 using : ssh -i (the savedfile) bandit17........-p 2220

**BANDIT17**
---

 Next to find out the line which is diiferent between two directories we use diff command: diff previous new |uniq -u

* The differed text will come as :< p6ggwdNHncnmCNxuAt0KtKVq185ZU7AW
-- hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg.

*  hence the new password.

 **BANDIT18**
 ---

 * bandit18 pass:hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg.

 * //When you connect to an SSH server, the server's default behavior is to start a login shell for the specified user. If the login shell exits immediately, it can result in being logged out immediately after connecting.
* to solve: Try specifying a different shell explicitly when connecting. For example, you can use: ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/bash
-  [ This command explicitly specifies /bin/bash as the shell to be used on the remote server.] - more user friendly option
  
*  since we cant directly connect using ssh, we can create a remote shell to do the task using: -t /bin/sh  {-t ;This will start a new bash shell on the server.}
-   [This command uses the -t option, which forces pseudo-tty allocation, and specifies /bin/sh as the shell.]

* this will open up a new file readme and on using cat will give the pass: awhqfNnAbc1naukrpqDYcF95h7HoMTrC


 **BANDIT19**
 ---
 setuid: a bit that makes an executable run with the privileges of the owner of the file.
-  The primary purpose of setuid is to allow users to execute specific programs with elevated privileges without needing to escalate their own privileges.

-  Linux File Permissions:

   * Each file in Linux has an owner, a group that owns the file, and permissions set for the user (owner), group, and others.
   * Permissions include read (r), write (w), and execute (x) for each category (user, group, others).
   * Permissions are represented in the format rwxrwxrwx, where the first three letters represent user permissions, the next three represent group permissions, and the      last three represent others' permissions.

Setuid (s) Permission:

    The setuid (s) permission is a special permission that replaces the x (execute) permission in the user's permission set.
    When a program with setuid is executed, it runs with the effective user ID (UID) of the owner of the program, not the UID of the user who launched it.

Setting Setuid Permission:

    To give a binary setuid permissions, use the chmod u+s <filename> command.
* first on trying to open the password,i was denied permission as a user. to get the same level of preveilages as a user we use setud.
* going to home directory to check the additional details on each file,(rwxrwxrwx)
* cd ~ , ls -l , and on going to the directory of the file...it said run the command as another user.
* so going back as a bandit user and putting in :./bandit20-do cat /etc/bandit_pass/bandit20

  bandit20 pass:VxCazJaVykI6W36BkBU0mJTCM8rR95XT

  **BANDIT20**
  ---
* after going to directory and typing ls -l : i got suconnect and used it to listen on any port number say:12000 by : ./suconnect 12000
* for listening we need to send something ,and here we need to send the bandit20 password:e0ho -n "bandit20pass" | nc -l  -p 12000

Open two terminal:
- one to send the bandit 20 password: echo -n 'pass' | nc -l -p 12000
- one to receive using : ./suconnect 12000
  bandit21 pass:NvEJF7oVjkddltPSrdKEFOllh9V1IBcq

  







