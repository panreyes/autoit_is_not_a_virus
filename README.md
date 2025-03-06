# Every executable made with AutoIT is considered malware

AutoIT, according to their website, "is a freeware BASIC-like scripting language designed for automating the Windows GUI and general scripting. It uses a combination of simulated keystrokes, mouse movement and window/control manipulation in order to automate tasks in a way not possible or reliable with other languages."

In short: A custom programming language and a compiler.

In my opinion, it's really useful to create small portable programs for a lot of situations. I made a few pieces of software with it, most of them private, and it's really easy and fast.

The only problem that AutoIT has is that many malware creators also consider AutoIT really useful to make their payloads. And... now every antivirus detects EVERY AutoIT program as a virus.

This repository includes an example source code with just a line:
```
MsgBox(0, 0, "Hola mundo!")
```

The signed binary generated with that code is, as of 6 of March of 2025, detected as malware by many AV vendors:
https://www.virustotal.com/gui/file-analysis/MWFiYjQwNjU1NjMxNjFiYTU1NDI2M2RjN2ZmODI5NDk6MTc0MTI2OTE4NA==

Depending on the provider and the day, it will be detected as: Nymeria, Wacatac, MulDrop8, Vindor, TrojanDropper, ...

It can be reproduced following with these steps:
1. Download and install AutoIT from its official website:
https://www.autoitscript.com/site/
2. Open the Scite editor and paste that previous line
3. Press F7 to build an exe.

# My conclusion
I understand that cybersecurity threat attacks are horrible these days, but we need a method to at least validate independent software developers like me that can't afford an EV certificate to avoid being detected as malware every time we create a new build.

Also, if the AV vendors detect many legitimate executables as false positives, the users will lose confidence in their security solutions and will probably end up permitting the execution of an actual malware when the time comes.
