## The hack

Hi. Recently, my friend's Steam account was hacked. I looked into the issue and checked his system logs and found a malicious DLL file that didn't match up with the DLL files I had. Somehow, a hacker injected this DLL into Steam. I fixed the issue and reloaded Steam to check that the file didn't automatically install itself, but the file had reappeared. I ran the debugger and it seems that the DLL gets injected by hooking on to system drivers. My friend hadn't downloaded any suspicious files, so I can only assume there must be a vulnerability within Steam itself. I reported the problem to Valve but haven't gotten a response yet, so I created a fix since the attacker seems to be starting to access the compromised accounts.

## How to fix

I wrote a simple script to remove the DLL and scan the drivers. Just run the EXE and grant it administrator privileges (this is necessary for the driver scan). If you don't want to run the executable, you can build the fix yourself from the source code (Python 2.x required).
