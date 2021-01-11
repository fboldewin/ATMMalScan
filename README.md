<img src="https://github.com/fboldewin/ATMMalScan/blob/main/graphics/ATMMalScan-Logo.PNG" height="300" width="300">

# Introduction
ATMMalScan is a commandline tool for Windows operating systems version 7 and higher, which helps to search for traces of malware on an ATM during the DFIR process. This tool scans the running processes of a system to be examined, as well as the hard disk, depending on the specified file path. To scan a system, a user with standard rights is sufficient. However, ATMMalScan provides the best results with administrator privileges.

# Known issues:
Currently ATMMalScan does not support codepages that require Unicode, this means Windows operating systems that are set to e.g. Cyrillic or Chinese characters, no representative result can be guaranteed.

# Usage (Example)

Step1 => Scan process memory and disk. ===> Check if Admin privileges are available on the device for best results!
<img src="https://github.com/fboldewin/ATMMalScan/blob/main/graphics/1-Scan-Mem-Disk.PNG" height="300" width="840">


Step2 => ATMMalScan detect a Malware called XFS_DIRECT in a process, gives details about the thread and its rules matches.
Further a full processmemory dump has been saved to disk, to catch the malicious process, its modules, as well as its stack and heap pages.
<img src="https://github.com/fboldewin/ATMMalScan/blob/main/graphics/2-Scan-Malware-Detected.PNG" height="600" width="600">


Step3 =>  Dump can be found here => <Directory where ATMMalScan64.exe has been started>\Dump  
<img src="https://github.com/fboldewin/ATMMalScan/blob/main/graphics/3-Scan-Malware-Dump.PNG" height="200" width="500">


Step4 =>  Open dumpfile with Windbg and extract the ATM malware to disk using ".writemem"
<img src="https://github.com/fboldewin/ATMMalScan/blob/main/graphics/4-Windbg-Malware-Extraction.PNG" height="500" width="900">


Step5 => Repair the dumped PE with one of your favorite PE-Fixers and start analysing the malware in detail. 
<img src="https://github.com/fboldewin/ATMMalScan/blob/main/graphics/5-PEDumpFixer%2BIDA.PNG" height="500" width="700">
