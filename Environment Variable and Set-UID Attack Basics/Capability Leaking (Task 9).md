## <h1>**Capability Leaking**</h1>

[Click here to return to the Home Repository](https://github.com/nicohaines/Cybersecurity-Home-Lab/blob/6c40208dbff8b486b290dc279e0788ebb6142c7a/Environment%20Variable%20and%20Set-UID%20Attack%20Basics/README.md)

## **Task 9: Capability Leaking**

In this example, capability leaking is caused because a file descriptor is opened but never closed. Because of this, here is what happens:
* The process is Set-UID and opens /etc/zzz.
* There is no guaranteed close of the file descriptor (or guaranteed drop of privileges) before the program executes /bin/sh.
* Because the file descriptor and privileges persist into the shell, a normal user who runs this program can access the root shell and use the open descriptor to reach privileged resources.

[Click here to return to the Home Repository](https://github.com/nicohaines/Cybersecurity-Home-Lab/blob/6c40208dbff8b486b290dc279e0788ebb6142c7a/Environment%20Variable%20and%20Set-UID%20Attack%20Basics/README.md)