# Title

Windows Shortcut Files

# Extension

LNK

## Description

LNK files are usually seen by users as shortcuts, and used in places like the Desktop and Start Menu.

Windows shortcut files (.LNK) include many metadata fields, including an icon location field (also known as the IconEnvironmentDataBlock) designed to specify the path to an icon file that is to be displayed for the LNK file within a host directory.



**Security Concerns**

LNK Files can be given custom icons, as well as contain code such as a command like Powershell or Command Prompt might execute. Combined with double file-extension issues, they frequently will decieve users into clicking on them.

A linux tool like `lnkinfo` can be used to display details of the file, and will give more details than the default properties button in Windows which might only show the target application and not the malicious argument to it.

## File Header Signature (Magic Bytes)

4C 00 00 00 01 14 02 00

## MimeType

Application/x-ms-shortcut

## Example

[Example](../../../FileExamples/raw/main/ExampleFiles//example.lnk)

## References

https://attack.mitre.org/techniques/T1027/012/

https://www.trendmicro.com/en_us/research/17/e/rising-trend-attackers-using-lnk-files-download-malware.html
