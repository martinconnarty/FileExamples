# Title

ZIP Files

# Extension

ZIP

## Description

**From Wikipedia**

ZIP is an archive file format that supports lossless data compression. A ZIP file may contain one or more files or directories that may have been compressed. 

**Security Concerns**

ZIP files allow one or multiple malicious files to be easily combined and delivered to a victim. This may often be through Phishing where they are sent directly or a URL which leads to a ZIP.

As ZIP file use is built in to many Operating Systems, as well as it's ability to password protect + compress, it is often used by a Threat Actor when exfiltrating data that they may have stolen.

The Password Protecting of a ZIP can be used as a way to prevent security tools such as inbound email scanners, from being able to scan the contents. Victims may receive the password in the body of the email or seperately. Importantly to note, Password Protected ZIPs do **not** hide the file name of the contents by default even if the files themselves cannot be read without the password.

## File Header Signature (Magic Bytes)

- 50 4B 03 04 (PK)
- 50 4B 05 06 (empty archive) (PK)
- 50 4B 07 08 (spanned archive) (PK)
 


## MimeType

application/zip
## Example

[Example](../../../FileExamples/raw/main/ExampleFiles//example.zip)

[Example Password Protected - password=testtest](../../../FileExamples/raw/main/ExampleFiles//example_password_testtest.zip)

## References

https://en.wikipedia.org/wiki/ZIP_(file_format)

https://www.crowdstrike.com/blog/how-to-prevent-zip-file-exploitation/

https://attack.mitre.org/techniques/T1560/
