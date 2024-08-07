# Title

Lnk - LnkStomped files

# Extension

Lnk

## Description

**From https://www.elastic.co/security-labs/dismantling-smart-app-control**

> "When a user downloads a file, the browser will create an associated “Zone.Identifier” file in an alternate data stream known as the Mark of the Web (MotW). This lets other software (including AV and EDR) on the system know that the file is more risky. SmartScreen only scans files with the Mark of the Web. SAC completely blocks certain file types if they have it. This makes MotW bypasses an interesting research target, as it can usually lead to bypassing these security systems. Financially motivated threat groups have discovered and leveraged multiple vulnerabilities to bypass MotW checks. These techniques involved appending crafted and invalid code signing signatures to javascript or MSI files.

> During our research, we stumbled upon another MotW bypass that is trivial to exploit. It involves crafting LNK files that have non-standard target paths or internal structures. When clicked, these LNK files are modified by explorer.exe with the canonical formatting. This modification leads to removal of the MotW label before security checks are performed. The function that overwrites the LNK files is _SaveAsLink() as shown in the following call stack:"

I have generated a LNK File as per [Elastic's Tool](https://github.com/joe-desimone/rep-research/blob/8e22c587e727ce2e3ea1ccab973941b7dd2244fc/lnk_stomping/lnk_stomping.py) - lnkinfo shows:

![image](https://github.com/user-attachments/assets/8bb5267f-b318-4b3a-85eb-1282f6d6316f)


**Security Concerns**

As described above LNK Stomping is a regularly used method that can be used to bypass MoTW Smart Screen restrictions on LNKFiles. 

## File Header Signature (Magic Bytes)

- 4C 00 00 00 01 14 02 00


## MimeType

Application/x-ms-shortcut

## Example

[Example](../../../FileExamples/raw/main/ExampleFiles/lnk_stomp.lnk)

## References

[https://en.wikipedia.org/wiki/7z](https://www.elastic.co/security-labs/dismantling-smart-app-control)

https://github.com/martinconnarty/FileExamples/blob/main/Lnk.md

https://attack.mitre.org/techniques/T1560/



