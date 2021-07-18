# Operating Systems Assignment 2 - Generations
This exercise involves printing out the generations of a series of processes created using fork().

You will create a program that accepts a single command line argument indicating the number of generations that should be created. For each generation, your program will fork a child process until you have created a series of children of the right length. Each process should print its own generation, in reverse order.

When the generations are printed, each process should print its own process ID, as well as the process ID of its parent process.

## Example Output
Here are some sample runs:

### No argument
If no argument is provided, the program should print a message and exit

```
$ ./generations
Usage: ./generations num_generations
```
### Invalid argument
If the argument is less than 0, the program should print a message and exit
```
$ ./generations
Usage: ./generations num_generations
```
### Correct Argument
```
$ ./generations 5
Great Great Great Grandchild. pid: 5732 ppid: 5731
Great Great Grandchild. pid: 5731 ppid: 5730
Great Grandchild. pid: 5730 ppid: 5729
Grandchild. pid: 5729 ppid: 5728
Child. pid: 5728 ppid: 5727
Parent. pid: 5727 ppid: 3329
```
## Completing the Assignment
Follow these steps to complete the assignment:
### Accept the Assignment
Accept the assignment in Github Classroom by Clicking on [this link](https://classroom.github.com/a/EO3Kl9gF). This will create your own repository containing the template files.

*Note:* In addition to creating your repository, accepting the assignment will also create a "Feedback" pull request. Please _do not_ close or delete this pull request. It will be used for me to communicate comments about your assignment to you. 
### Clone Your Repository
Clone your new repository to a Linux machine (either WSL or erdos), as follows:
```
$ git clone git@github.com:skamens-fordham-org/os-h22-<your_username>.git
```
### Implement the Code
The template contains a C++ sourcefile `generations.cpp`. In this file are detailed instructions on how to implement the assignment.
### Compile and Test
You can compile your program using `make` (there is a simple Makefile in your template repository). If you are using another development environment, you can simply compile using g++.

Test your program to ensure that it provides the output as described above.

*Note:* It is not unusual when testing programs that use fork() to end up with an infinite loop. If this happens when you are testing, use Control-C to stop the execution and figure out what is causing the loop.
### Commit Your Changes to Git
Use the folloowing command to commit your changes
```
$ git commit
skamens@LAPTOP-V3GF0EG5:~/fordham/fall2021/os-hw1-template$ git commit
[main e9aeec7] Add initial template files
 2 files changed, 68 insertions(+)
 create mode 100644 Makefile
 create mode 100644 generations.cpp
```
### Push Your Changes to Github
Upload your changes to Github as follows:
```
skamens@Sam:~/test-assignment-skamens-fordham$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 279 bytes | 279.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/skamens-fordham-org/test-assignment-skamens-fordham
   1a6667e..460b567  main -> main
```
### Submit Your Assignment to Blackboard
In order to match your assignment to the grading system, each assignment must be "submitted" in Blackboard. This indicates to me that you consider your assignment ready to be graded. In addition, you will be able to see the detailed rubric for each assignment after grading is complete.

#### Fill in the submission file
Fill in the information in the file submit.txt. The contents of the file are as follows:
```
Operating Systems, Fall 2021
Assignment 2

Please fill in the information below and submit this file to Blackboard to turn in your assignment.

Your Name:
Email Address:
Link to your Github Repository: 
Upload the file to Blackboard
```
#### Click on the Assignment Link

#### Click "Browse Local Files"
Select and upload your submit.txt file, and click Submit (at the bottom of the screen)

Note: You could also click Write Submission and simply enter the contents of submit.txt in the text box before clicking Submit



