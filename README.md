# mimikatz
windows 10 password hash cracker.


For SAM file retriever toll mimikatz
=======================================================
Format of the SAM and/or SYSTEM files has changed since Windows 10 update, thus tools like chntpw, bkhive, pwdump, samdump2 print hash of the empty passwords (I verified it on my Windows 10). Since this update, Windows uses AES128 to encrypt password's MD4 hash. Because of that, nearly all tools regarding Windows password recovery became outdated.

Fortunately there is a tool called mimikatz  (Windows-only, but can be ran on Linux by using Wine) created by Benjamin Delpy, that can read passwords' hashes saved in Windows' new format. Note that Windows Defender and Symantec antivirus treats it as a 'Hack Tool' and removes it, so you need to disable them before running mimikatz (run as an administrator).

mimikatz consists of many modules, but you should explore lsadump module, particularly lsadump::sam function. 

You can download mimikatz tool
https://github.com/gentilkiwi/mimikatz.git
