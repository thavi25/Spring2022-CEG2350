## Lab 01

- Name: Thavindu Gimsara Wijesena
- Email: wijesena.2@wright.edu

## Part 1 Answers

1. mkdir DirA  
2. mkdir “Dir B”
3. cd “Dir B”
4. DirA. It is better to avoid spaces. For example, if you type mkdir Dir B, it will create two individual directories called “Dir” and “B” instead of a singular directory named “Dir B”

5. cd /home/thavi

   mv "Dir B" DirB

## Part 2 Answers

1. cd DirA

   touch test.txt

   vim test.txt
   
   i

   ***file content here***
 
    Escape (esc)
  
     :wq

  
2. File contents:

```
Hello World!
Pizza time!
Error404
Don’t break ur laptop
```

## Part 3 Answers

1. cd DirA
   
   cp test.txt .hiddentext.txt
   
2. ls -a

## Part 4 Answers

1. sudo adduser bob
2. /home/bob/
3. Cannot. It is because I do not have the permission to add or edit files from my user to bob. In order to create a file, I have to switch to bob.
4. su bob 
5. cd ~ 
6. Yes. It is because the user now is bob. This user can add files to their own home directory without any permission required.
7. su thavi (note: also could use ‘exit’ instead)
8. cd ~

## Part 5 Answers

1. sudo addgroup crew
2. sudo usermod -a -G crew thavi  
   
   sudo usermod -a -G crew bob    

3. chmod 770 DirA   (note: before using this command, I used the command 'sudo chgrp crew DirA' but it did not give me permission to create any files in 'DirA' even though it gave me access to DirA)

4. su bob
5. cd /home/thavi/DirA
   
   touch newfile.txt
   
6. This is because we gave Read, Write and execute permission to the group 'crew' for DirA using the command 'chmod 770 DirA'.

## Part 6 Answers

1. su thavi
  
   cd
   
   sudo touch sudouser.txt
   
2. This file is only a readonly for user 
3. sudo vim sudouser.txt

   i

   ***file content here***
  
   
   
    esc
   
   :wq
   
   
   
   File Content: 
   ```
   this is a sudo file
   ```

## Extra Credit

1. su thavi
  
   cd ~
   
   sudo adduser sally
   
   sudo usermod -a -G crew sally
   
   cd DirB
   
   touch mydiary.txt
   
   chmod 600 mydiary.txt
   
   sudo chgrp crew mydiary.txt
   
   sudo chown sally mydiary.txt

2. step 1:
   cd /home/thavi/DirB
   
   step 2:
   sudo vim mdiary.txt

   step 3:
   i

   step 4:
   *add my text:*
   this diary is empty

   step 5:
   esc

   step 6:
   :wq
   
   
3. step 1:
   cd ~

   step 2:
   sudo usermod -a -G sudo bob
 
   step 3:
   su bob

   step 4:
   cd /home/thavi/DirB

   step 5:
   sudo vim myDiary.txt

   step 6:
   i

   step 7:
   *add bob's text:* Sally this is 2022. Nobody uses written diaries anymore. That is why we have the internet and the cloud. -not bob-

   step 8:
   esc

   step 9:
   :wq
 
