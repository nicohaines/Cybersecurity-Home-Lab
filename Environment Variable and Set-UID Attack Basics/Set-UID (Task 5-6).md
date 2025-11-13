## <h1>**Set-UID**</h1>

[Click here to return to the Home Repository](README.md)

## **Task 5: Environment Variable and Set-UID Programs**

When exporting environment variables as a normal user for a Set-UID program, the new environment variables will be reflected during that session. However, once the session ends and is reopened, those environment variables are no longer present.

    Program "foo.c":

![](Screenshots/14.png)

    Compiling, changing the owner to root, and establishing "foo.c" as a Set-UID program:

![](Screenshots/15.png)

    Now after setting up this program, when attempting to create a new Environment Variable (for example ANYNAME=Nico), the new ENV is reflected when running the newly compiled ./foo command.

![](Screenshots/16.png)

## **Task 6: The PATH Environment Variable and Set-UID Programs**

You can get system(“ls”) to run properly while using the path env as opposed to just using "ls" in the /bin/sh directory. Because of this vulnerability, the system() command allows a normal user to run the ls command using a relative path instead of the absolute path. This means that a user could create a malicious code that can identify the exact directory of this program.

    For example, here is a program titled "systemls.c":

![](Screenshots/17.png)



[Click here to return to the Home Repository](README.md)