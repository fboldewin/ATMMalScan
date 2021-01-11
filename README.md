<img src="https://github.com/fboldewin/ATMMalScan/blob/main/graphics/ATMMalScan-Logo.PNG" height="300" width="300">

# Introduction
ATMMalScan is a commandline tool for Windows operating systems version 7 and higher, which helps to search for traces of malware on an ATM during the DFIR process. This tool scans the running processes of a system to be examined, as well as the hard disk, depending on the specified file path. To scan a system, a user with standard rights is sufficient. However, ATMMalScan provides the best results with administrator privileges.

# Known issues:
Currently ATMMalScan does not support codepages that require Unicode, this means Windows operating systems that are set to e.g. Cyrillic or Chinese characters, no representative result can be guaranteed.

