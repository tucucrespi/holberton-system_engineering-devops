General

How to create SSH keys
What is the advantage of using #!/usr/bin/env bash over #!/bin/bash
How to use while, until and for loops
How to use if, else, elif and case condition statements
How to use the cut command
What are files and other comparison operators, and how to use them
Requirements

General

Allowed editors: vi, vim, emacs
All your files will be interpreted on Ubuntu 14.04 LTS
All your files should end with a new line
A README.md file, at the root of the folder of the project, is mandatory
All your Bash script files must be executable
You are not allowed to use awk
Your Bash script must pass Shellcheck (version 0.3.3-1~ubuntu14.04.1 via apt-get) without any error
The first line of all your Bash scripts should be exactly #!/usr/bin/env bash
The second line of all your Bash scripts should be a comment explaining what is the script doing
More Info

Shellcheck

Shellcheck is a tool that will help you write proper Bash scripts. It will make recommendations on your syntax and semantics and provide advice on edge cases that you might not have thought about. Shellcheck is your friend! All your Bash scripts must pass Shellcheck without any error or you will not get any points on the task.

Shellcheck is available on the school’s computers. If you want to use it on your own computer, here is how to install it.

Examples:

Not passing Shellcheck:



Passing Shellcheck:



For every feedback, Shellcheck will provide a code that you can use to get more information about the issue, for example for code SC2034, you can browse https://github.com/koalaman/shellcheck/wiki/SC2034.

# Tasks

# 0. Create a SSH RSA key pair mandatory

Read for this task:

Linux and Mac OS users
Windows users
man: ssh-keygen

You will soon have to manage your own servers concept page hosted on remote data centers. We need to set them up with your RSA public key so that you can access them via SSH.

Create a RSA key pair.

Requirements:

Share your public key in your answer file 0-RSA_public_key.pub
Fill the SSH public key field of your intranet profile with the public key you just generated
Keep the private key to yourself in a secure location, you will use it later to connect to your servers using SSH. Some storing ideas are Dropbox, Google Drive, password manager, USB key. Failing to do so will prevent you to access your servers, which will prevent you from doing your projects
If you decide to add a passphrase to your key, make sure to save this passphrase in a secure location, you will not be able to use your keys without the passphrase
SSH and RSA keys will be covered in depth in a later project.

# 1. For Holberton School loop mandatory

Write a Bash script that displays Holberton School 10 times.
Requirement:
* You must use the for loop (while and until are forbidden)
sylvain@ubuntu$ head -n 2 1-for_holberton_school 
#!/usr/bin/env bash
# This script is displaying "Holberton School" 10 times
sylvain@ubuntu$ ./1-for_holberton_school 
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
sylvain@ubuntu$ 
Note that:
* The first line of my Bash script starts with #!/usr/bin/env bash
* The second line of my Bash scripts is a comment explaining what it is doing

# 2. While Holberton School loop mandatory

Write a Bash script that displays Holberton School 10 times.
Requirements:
* You must use the while loop (for and until are forbidden)
sylvain@ubuntu$ ./2-while_holberton_school
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
sylvain@ubuntu$ 

# 3. Until Holberton School loop mandatory

Write a Bash script that displays Holberton School 10 times.
Requirements:
* You must use the until loop (for and while are forbidden)
sylvain@ubuntu$ ./3-until_holberton_school
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
sylvain@ubuntu$ 

# 4. If 9, say Hi! mandatory

Write a Bash script that displays Holberton School 10 times, but for the 9th iteration, displays Holberton School and then Hi on a new line.
Requirements:
* You must use the while loop (for and until are forbidden)
* You must use the if statement
sylvain@ubuntu$ ./4-if_9_say_hi
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Hi
Holberton School
sylvain@ubuntu$ 

# 5. 4 bad luck, 8 is your chance mandatory

Write a Bash script that loops from 1 to 10 and:
* displays bad luck for the 4th loop iteration
* displays good luck for the 8th loop iteration
* displays Holberton School for the other iterations
Requirements:
* You must use the while loop (for and until are forbidden)
* You must use the if, elif and else statements
sylvain@ubuntu$ ./5-4_bad_luck_8_is_your_chance
Holberton School
Holberton School
Holberton School
bad luck
Holberton School
Holberton School
Holberton School
good luck
Holberton School
Holberton School
sylvain@ubuntu$ 
For the most curious:
* 8 in the Chinese culture
* 4 in the Chinese culture

# 6. Superstitious numbers mandatory

Score: 0.00% (Checks completed: 0.00%)
Write a Bash script that displays numbers from 1 to 20 and:
* displays 4 and then bad luck from China for the 4th loop iteration
* displays 9 and then bad luck from Japan for the 9th loop iteration
* displays 17 and then bad luck from Italy for the 17th loop iteration
Requirements:
* You must use the while loop (for and until are forbidden)
* You must use the case statement
sylvain@ubuntu$ ./6-superstitious_numbers
1
2
3
4
bad luck from China
5
6
7
8
9
bad luck from Japan
10
11
12
13
14
15
16
17
bad luck from Italy
18
19
20
sylvain@ubuntu$ 

# 7. Clock mandatory

Write a Bash script that displays the time for 12 hours and 59 minutes:
* display hours from 0 to 12
* display minutes from 1 to 59
Requirements:
* You must use the while loop (for and until are forbidden)
Note that in this example, we only display the first 70 lines using the head command.
sylvain@ubuntu$ ./7-clock | head -n 70
Hour: 0
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
Hour: 1
1
2
3
4
5
6
7
8
9
sylvain@ubuntu$ 

# 8. For ls mandatory


Write a Bash script that displays:
* The content of the current directory
* In a list format
* Where only the part of the name after the first dash is displayed (refer to the example)
Requirements:
* You must use the for loop (while and until are forbidden)
* Do not display hidden files

# 9. To file, or not to file mandatory

Write a Bash script that gives you information about the holbertonschool file.
Requirements:
* You must use if and, else (case is forbidden)
* Your Bash script should check if the file exists and print:
    * if the file exists: holbertonschool file exists
    * if the file does not exist: holbertonschool file does not exist
* If the file exists, print:
    * if the file is empty: holbertonschool file is empty
    * if the file is not empty: holbertonschool file is not empty
    * if the file is a regular file: holbertonschool is a regular file
    * if the file is not a regular file: (nothing)

# 10. FizzBuzz mandatory

Write a Bash script that displays numbers from 1 to 100.
Requirements:
* Displays FizzBuzz when the number is a multiple of 3 and 5
* Displays Fizz when the number is multiple of 3
* Displays Buzz when the number is a multiple of 5
* Otherwise, displays the number
* In a list format