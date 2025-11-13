## **Securely Invoke External Programs**
**Task 8**

In this task, I compare the uses of execve() and system().

1. If I run the program with system(), I am able to access a root shell when there is an error or when input contains shell metacharacters. For example:

        ./catall aa;/bin/sh

    system() opens a shell, and because the program is Set-UID, a normal user can cause the shell to run with elevated privileges, which may allow access to a root shell if the program does not properly handle input or drop privileges.

2. When using execve() instead, the vulnerability from system() should not occur because execve() does not invoke the shell in the same way. However, in my demonstration execve() also opened a root shell. I suspect there is still a way the code ends up invoking /bin/sh or otherwise allowing the shell to be executed, so I will research this further to identify the exact issue. Technically, execve() should be safer.
