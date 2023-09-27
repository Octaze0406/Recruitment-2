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

To connect to a server using private key use: ssh -i (privatekey) username@host -p 

**BANDIT 14**
---

nc - command used to read and write data on a local network





