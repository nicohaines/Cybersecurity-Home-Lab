## **Set-UID**

**Task 5:**

When exporting environment variables as a normal user for a Set-UID program, the new environment variables will be reflected during that session. However, once the session ends and is reopened, those environment variables are no longer present.

**Task 6:**

You can get system("ls") to run properly while using the PATH environment (instead of specifically using ls in /bin/sh). Because of this vulnerability, the system() call in this example allows me, as a normal user, to run ls using a relative path instead of the absolute path. This means I could create malicious code that can identify the exact directory of this program.
