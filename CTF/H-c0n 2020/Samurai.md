# Steganography

## 🐱‍👤 Samurai 🐱‍👤

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/samurai_title.png)

Once downloaded the image "samurai.png" we opened and it look like this:

![Screenshot](https://github.com/Gh05t1nTh3SSH/Write-ups/blob/master/CTF/H-c0n%202020/Images/Samurai/samu.png)

One of the first steps that I always do with stego challenges, is check the file properties and metadata:

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/filesamu.png)

With **file** command I didn't see anything out of the expected, so I keep digging with **exiftool**

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/exiftool.png)

The first impresion was the name of the autor, however, I keep with my checklist with **binwalk**

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/binwalk.png)

Here I found something useful, a zip compressed inside the png. Binwalk has an option to extract the compressed files

![Screenshot](https://github.com/Gh05t1nTh3SSH/Write-ups/blob/master/CTF/H-c0n%202020/Images/Samurai/listextract.png)


![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/spectro.png)
![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/stegpy.png)
![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/complete.png)
