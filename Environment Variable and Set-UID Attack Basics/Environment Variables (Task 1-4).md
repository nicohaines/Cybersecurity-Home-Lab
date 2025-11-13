## **Environment Variables**

**Task 1:**

Demonstrates the usage of the printenv and env commands, and how to set and unset environment variables.

**Task 2:**

When using fork() to duplicate a process, the child inherits all of the parent’s environment variables. In the example below I use diff to compare the environment variables of the original process (parent) and the duplicate (child). As you can see, there is no difference because the child inherited all of the parent’s variables.

**Task 3:**

This task shows two examples of process environment variable lists. In the first, the third argument to execve() is NULL. When the third argument of execve() is NULL, the new process has no environment variables. When the third argument is the previously identified environ reference, the program lists all of its related environment variables.

**Task 4:**

This task demonstrates a flaw of system() compared to execve(): system() invokes /bin/sh, and environment variables (for example PATH) are passed to that shell process, which can cause unexpected behavior or make execution dependent on the environment.
