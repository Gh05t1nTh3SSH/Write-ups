# Steganography

## 🐱‍👤 Samurai 🐱‍👤

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/samurai_title.png)

Once downloaded the image "samurai.png", looks like this:

![Screenshot](https://github.com/Gh05t1nTh3SSH/Write-ups/blob/master/CTF/H-c0n%202020/Images/Samurai/samu.png)

One of the first steps that I always do with stego challenges, is check the file properties and metadata:

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/filesamu.png)

With command **file** I didn't see anything out of the expected, so I continue with **exiftool**

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/exiftool.png)

The first impresion was something weird with the name of the author, however, I keep digging with **binwalk**

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/binwalk.png)

Here I found something useful, a zip compressed inside the png. Binwalk has an option to extract the compressed files

![Screenshot](https://github.com/Gh05t1nTh3SSH/Write-ups/blob/master/CTF/H-c0n%202020/Images/Samurai/listextract.png)

Nice! We found a **wav** file. After checking the metadata and properties, I've opened the file with an [Spectrogram].

There is a GUI tool called [Sonic Visualizer]. With the option (P), we can open the Spectrogram and see the word **SHINOBI**

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/spectro.png)

After try to use **SHINOBI** as a password with different stego programs, finally I tried with [stegpy] and it worked:

![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/stegpy.png)

## Flag



![Screenshot](https://raw.githubusercontent.com/Gh05t1nTh3SSH/Write-ups/master/CTF/H-c0n%202020/Images/Samurai/complete.png)
