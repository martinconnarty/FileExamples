# Title

7z files

# Extension

7z

## Description

**From https://www.elastic.co/security-labs/dismantling-smart-app-control**

> "When a user downloads a file, the browser will create an associated “Zone.Identifier” file in an alternate data stream known as the Mark of the Web (MotW). This lets other software (including AV and EDR) on the system know that the file is more risky. SmartScreen only scans files with the Mark of the Web. SAC completely blocks certain file types if they have it. This makes MotW bypasses an interesting research target, as it can usually lead to bypassing these security systems. Financially motivated threat groups have discovered and leveraged multiple vulnerabilities to bypass MotW checks. These techniques involved appending crafted and invalid code signing signatures to javascript or MSI files.

> During our research, we stumbled upon another MotW bypass that is trivial to exploit. It involves crafting LNK files that have non-standard target paths or internal structures. When clicked, these LNK files are modified by explorer.exe with the canonical formatting. This modification leads to removal of the MotW label before security checks are performed. The function that overwrites the LNK files is _SaveAsLink() as shown in the following call stack:"

**Security Concerns**

As described above LNK Stomping is a regularly used method that can be used to bypass MoTW Smart Screen restrictions on LNKFiles. 

## File Header Signature (Magic Bytes)

- 37 7A BC AF 27 1C	 (7z)
 

## MimeType

application/x-7z-compressed

## Example

[Example](../../../FileExamples/raw/main/ExampleFiles/example.7z)

## References

https://en.wikipedia.org/wiki/7z

http://fileformats.archiveteam.org/wiki/7z

https://attack.mitre.org/techniques/T1560/


![image](https://github.com/user-attachments/assets/8bb5267f-b318-4b3a-85eb-1282f6d6316f)
