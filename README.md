# LinuxCLI
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    In this exercise, you will learn and practice several common commands for the BASH shell on a Linux system.
On the Linux desktop, right-click anywhere and select Open Terminal Here from the context menu to open a Terminal window.
</head>
<body>
    
  <img src="https://i.imgur.com/P3AlRkT.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
  In the new terminal window, take note of the prompt: cybrary@linux:~/Desktop$. A lot of information is being conveyed here. First, you are the cybrary user on a host named linux. The ~ means "home," which, for the cybrary user, is /home/cybrary. The /Desktop means your current location in the file system is the Desktop directory under /home/cybrary. The $ means you are a non-root user.
  
  <img src="https://i.imgur.com/8qQscvU.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
  Note: Not every Linux terminal you use will have a prompt to tell you who and where you are.
In the next steps, you will learn some commands to validate the information provided by the prompt.
At the prompt, type whoami and press Enter to display the name of the current user.
  
  <img src="https://i.imgur.com/BZW6DH2.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
  At the prompt, type hostname and press Enter to display the name of the machine.
  
  <img src="https://i.imgur.com/OL5NJpE.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
   At the prompt, type pwd and press and enter to display the current directory.
  
  <img src="https://i.imgur.com/VqvazP1.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
  The pwd command stands for print working directory. Remember that ~ is short for "home" and "home" for the cybrary user is /home/cybrary. Thus ~/Desktop = /home/cybrary/Desktop.
      At the prompt, type id and press Enter to display the user and group ID's for your account.
  
  <img src="https://i.imgur.com/mrOF2eR.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
A standard user account in Linux starts at id 1000. The cybrary user is id 1001, which means it is a standard user account. Every user will also belong to a group named after the user.
Now that we have confirmed who we are and where we are, let's explore the Linux file system.
At the prompt, type cd .. (note the space between cd and ..) and press Enter.
The cd command stands for change directory, and .. means up one directory. By executing this command, we are moving from /home/cybrary/Desktop to /home/cybrary. You can use the pwd command to confirm this.
 <img src="https://i.imgur.com/bD0FriO.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
 At the prompt, type ls and press Enter to display a list of all files and directories in the current directory (/home/cybrary).
  
 <img src="https://i.imgur.com/cpqJQ24.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
 At the prompt, type ls -l and press Enter to display a long directory listing.
  
  <img src="https://i.imgur.com/rl6FsvV.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
  Notice that with the -l option, you can see important information about the directories and files in /home/cybrary.
In the output, the "d" means that the object is a directory. Next are three sets of permissions. Permissions are read (r), write (w), and execute (x). A dash (-) means that a given permission is not set. For example, r-x grants read and execute permission but not write. The first set of three applies to a file or folder owner, the next set applies to the group, and the last set applies to everyone else. Thus, for the /home/cybrary/Desktop directory, user cybrary has permission to read, write and execute, group cybrary has permission to read and execute, and everyone else has permission to read and execute.
At the prompt, type ls -la and press Enter.
<img src="https://i.imgur.com/yRcEpT4.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
The -a option shows all files, including hidden files. Notice the files that start with a dot (.)  These are hidden files. Typically these files are used to manage terminal settings, collect command history, and other shell-related settings. They are hidden to prevent users from making accidental changes to these important files and to keep the directory listing clean.
At the prompt, type cd ../..   and press Enter to go up two directories.
  
<img src="https://i.imgur.com/EgiLXkU.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
Notice the prompt changes to cybrary@linux:/$. The "/" means root directory. This is the top (root) of the Linux file system. Everything in Linux lives under the root directory. You can type cd ../../../../.. and press Enter, but you cannot go any higher than the root of the file system.
At the prompt, type ls and press Enter to see the typical file structure for Linux.
  
<img src="https://i.imgur.com/dHvdZMc.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
At the prompt, type cd ~ and press Enter to return home (/home/cybrary).
  
<img src="https://i.imgur.com/ZfZVE3Y.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
Alternatively, you can type cd /home/cybrary and press Enter.
At the prompt, type mkdir labwork and press Enter to create a new directory called labwork within the cybrary home directory.
The mkdir command stands for make directory. You can confirm the directory was created with ls.
  
<img src="https://i.imgur.com/wZN5ptm.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
At the prompt, use the cd command to navigate to the labwork directory.
At the prompt, type touch file1.txt file2.txt file3.txt and press Enter to create three empty files in the labwork directory. Use the ls command to confirm.
  
<img src="https://i.imgur.com/hxpfmCF.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">
  
At the prompt, type echo "This is file 1" >> file1.txt and press Enter to append the quoted text into the file1.txt file.
  
<img src="https://i.imgur.com/XR9qpHv.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

The “>>” output redirector tells Linux to append the echoed text to the file.
At the prompt, type cat file1.txt and press Enter to print the contents of file1.txt to the screen. 

<img src="https://i.imgur.com/WPAYdOG.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

The cat command stands for con cat enate.
At the prompt, type file file1.txt and press Enter to confirm that file1.txt is an ASCII text file. 

<img src="https://i.imgur.com/G2JXFuZ.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

The file command displays a file's type, even if a file has no extension or is intentionally mislabeled (e.g., file1.exe).

Note: Linux does not require the .txt extension on text files. Adding .txt is a courtesy to other users on the system.
At the prompt, use the echo command to append This is file 2 to file2.txt and This is file 3 to file3.txt, then use the cat command to confirm.
At the prompt, use the mkdir command to create three new directories in the labworks directory: red, blue, and green. It is possible to make all three directories at once. Use ls to confirm your work.

In the next steps, you will practice the commands to copy and move files.
At the prompt, type cp file1.txt blue/ and press Enter to copy file1.txt to the blue directory.

<img src="https://i.imgur.com/ESlCrUr.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

At the prompt, type ls -R and press Enter to display all files and folders under the labwork directory.

<img src="https://i.imgur.com/s4NbNbH.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

Notice that file1.txt exists in both labwork and blue (because it was copied, rather than moved).
At the prompt, type rm -i file1.txt and press Enter to remove file1.txt.

When prompted, type y and press Enter to confirm.

<img src="https://i.imgur.com/BP01vBe.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

Note: Without the -i option, rm would have removed the file without confirmation. This is very dangerous as the Linux CLI does not have a recycle bin like Windows. The rm command does not honor the GUI recycle bin even if you use a Linux GUI desktop. If you delete a file by accident, you will need to restore that file from a backup.
At the prompt, type ls -R and press Enter to confirm that file1.txt is now removed from the labworks folder.
At the prompt, type mv file2.txt green and press Enter to move the file2.txt file to the green directory. Execute ls -R to confirm that file2.txt has been moved.

<img src="https://i.imgur.com/mZN7qQf.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

Unlike the cp command, the mv command does not leave a copy of the file behind.

The mv command is also used the rename files.
At the prompt, type mv file3.txt happypumpkin.moo and press Enter to rename file3.txt.

Execute ls -R to confirm that file3.txt is gone, and in its place is happypumpkin.moo.
At the prompt, use the cat command to prove that the contents of happypumpkin.moo are the same as file3.txt.

Note: Again, Linux does not care what file you name or what file extension you use.
At the prompt, type mv happypumpkin.moo red/file3.txt and press Enter to move and rename the happypumpkin.moo file. Execute ls -R to confirm.

<img src="https://i.imgur.com/QP9e760.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

When you use the cat command to output the file's output to the terminal, the entire file content gets printed all at once, which is not always ideal. Linux provides two tools for reading large files: more and less. The more command is the original reading tool. The more command allows you to page through a file, one page at a time. The less command is a play on words as less is a newer tool, and less allows you to scroll up and down. In essence, "less" is "more".
At the prompt, type base64 /dev/urandom | head -c 1M > abigfile.txt and press Enter to create a large file.

This command generates 1MB of random text that is base 64 encoded. Execute ls -la to confirm the creation of abifile.txt.

<img src="https://i.imgur.com/b1PCCb7.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

At the prompt, type more abigfile.txt and press Enter to open abigfile.txt in more.

<img src="https://i.imgur.com/jhRGyrG.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

You can use the space bar to page through the file, but because this file is massive, it would take a long time to page through all of abigfile.txt. Instead, press q to quit more.
At the prompt, type less abigfile.txt and press Enter to open abigfile.txt in less.

Use the space bar to page down, b to page up, the down arrow to go down one line at a time, and the up arrow to go up one line at a time. When done moving around in less, press q to quit less.

Knowing how to locate files is essential when using Linux.  As luck would have it, Linux provides the find command just for this purpose.
At the prompt, type find / -name "more" 2>/dev/null and press Enter to look for all directories and files called "more" starting at the root directory (/).

<img src="https://i.imgur.com/0XBoZuS.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

Note: The 2>/dev/null command line argument tells Linux to redirect (>) any errors (2) to a black hole (/dev/null). This command suppresses error messages and makes the output more useful. Feel free to try the find command without error suppression to see what that looks like.
At the prompt, type find . -name "*.txt" and press Enter to find all files with a .txt extension in the current directory and all subdirectories.

<img src="https://i.imgur.com/gFMsoGT.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

Sometimes we need to find files that contain a particular word or phrase. The Linux grep tool is designed for precisely that.
At the prompt, type grep -r "This" and press Enter to find all files containing the text "This”.
The grep tool will show the location of the files and output the line where the text is found.

<img src="https://i.imgur.com/zp3x818.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

Finally, let's look at some basic file-parsing techniques. In the /cybrary/home directory, there is an unsorted file. We will look at ways to sort and count the contents of this file. We will also see how to combine simple Linux commands to generate the desired outcome.
At the prompt, execute the command to return to the /home/cybrary directory.
At the prompt, type cat unsorted and press Enter to view the contents of the "unsorted" file.

You will see a list of words in no particular order. You may notice that some of the words repeat.

<img src="https://i.imgur.com/m9bZxLZ.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

At the prompt, type cat unsorted | sort and press Enter to print an alphabetically sorted list of words in the "unsorted" file to the screen.

<img src="https://i.imgur.com/cTkTaHW.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

The | character is called a pipe. It tells Linux to take the output of cat and make it the input for the sort command.
At the prompt, type cat unsorted | sort | uniq and press Enter to sort the list and remove duplicates.

<img src="https://i.imgur.com/HG6ScS1.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

In this example, the cat command's output is piped into sort, and then that output is piped into uniq.

Note: The uniq command must be used with the sort command, as shown.
At the prompt, type cat unsorted | wc to count the file's words, lines, and characters.

<img src="https://i.imgur.com/JZNnkbV.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

The wc command stands for word count. The output tells us there are 17 words, 17 lines of text, and a total character count of 123.
At the prompt, type cat unsorted | wc -w commands to see the number of words only.

<img src="https://i.imgur.com/L2kORnr.png" alt="Lab Screenshot" style="max-width: 100%; height: auto;">

At the prompt, type cat unsorted | sort | uniq | wc -w and press Enter to count the unique words in the "unsorted" file.
At the prompt, type cd Desktop and press Enter to navigate to the desktop.
At the prompt, type ./flag.sh and press Enter to run a script that will check your work.
You will need 8 points to reveal the flag required to answer the last question on the Tasks tab.
Now you learned how to navigate the Linux file system and find files and folders. You learned how to create files and directories and append text to files. You also learned some basic file parsing.
