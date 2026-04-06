

## Source 
On the link below you can find source code of passThrough minifilter
https://github.com/microsoft/Windows-driver-samples/tree/main/filesys/miniFilter/passThrough

## Description
This project adds some payload to the original code.
How it works:
1. You have to create file C:\Windows\conf.txt
2. In conf.txt you should add description in the form:  
\<rights (rwx)\> \<object path to file\> \<process\>
ex: "r-x \Device\HarddiskVolume3\Users\hola\Desktop\test_dir\secret.txt test.exe"  
<process> - means process, which will be able to use given rights
3. Install and load driver

 As a result, you have only one process that is allowed to manipulate chosen file.
