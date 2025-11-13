## <h1>**Dynamic Loader/Leaker**</h1>

[Click here to return to the Home Repository](https://github.com/nicohaines/Cybersecurity-Home-Lab/blob/6c40208dbff8b486b290dc279e0788ebb6142c7a/Environment%20Variable%20and%20Set-UID%20Attack%20Basics/README.md)

## **Task 7: The LD PRELOAD Environment Variable and Set-UID Programs**

This task demonstrates potential vulnerabilities when using shared libraries or dynamic linking. The four examples below show how a dynamically linked program can behave under different conditions:
1. Running the program as a normal user (program with regular permissions) outputs the default/original environment variable value: "I am not sleeping".
2. When the program is Set-UID, the linking is successful and a normal user is able to run the linked program; this executes sleep().
3. When running as the root account while the program is Set-UID and re-exporting the LD_PRELOAD environment variable, the sleep() call is again successful.
4. In the last condition, the owner of myprog is Sally. As a normal user while the program is Set-UID, I am still able to run sleep().

Altogether, these outcomes imply that if the program is Set-UID and dynamically linked, any user may be able to influence or trigger the dynamically linked behavior.

[Click here to return to the Home Repository](https://github.com/nicohaines/Cybersecurity-Home-Lab/blob/6c40208dbff8b486b290dc279e0788ebb6142c7a/Environment%20Variable%20and%20Set-UID%20Attack%20Basics/README.md)