# pws
This repository contains a bunch of code that was used for a security demo. This is all meant for eductational purposes only.

The payload.txt, backdoor (in this case called test.exe) and test.bat files should all be in one of the two switch folders on the Bash Bunny.

The Bash Bunny impersonates the keyboard and starts injecting keystrokes. It first disables tamper protection, it then moves test.bat to $env:PUBLIC (C:\Users\Public) and starts test.bat. Then the backdoor is also copied to $env:PUBLIC and executed.


The test.bat file disables windows defender on the target machine and removes all signatures. It keeps running in the background to prevent windows defender from restarting.
