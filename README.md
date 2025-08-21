# How-to-do-steganography
Steganography is the practice of hiding a secret message inside another medium, e.g., image, audio, video, etc., so that the very existence of the message is concealed. Unlike encryption, which scrambles data to make it unreadable, steganography disguises the data so that outsiders don’t even suspect it exists.


Steganography

Download three .jpg images; e.g., images from pexels.com (it is royalty-free)
Create your three Text files; e.g., 1.txt, 2.txt, 3.txt
Download steghide https://steghide.sourceforge.net/download.php ( or get any other steganography tool of your choice)


Block1:- Key phrase to embed and extract file on steghide- StartHere
Why_W0rri? - encoded to Base64 string: V2h5X1cwcnJpPw== (I used: https://gchq.github.io/CyberChef/)
Save: V2h5X1cwcnJpPw== into your 1.txt file.
Then embed the 1.txt file into the 1.jpg (image) file with steghide (command line). 
To confirm: Try to extract your 1.txt file from the 1.jpg (image) file with steghide (command line) before you proceed to Block2.



Block2:- Key phrase to embed and extract on steghide - decode the Base64 string from Block1: V2h5X1cwcnJpPw==  (Use:- Why_W0rri?)
Create: 2.txt file, and save with the following message inside: 
Generate a SHA3-256 hash of the key phrase, S3Kur1ti. This will be used as the Symmetric Key for Block 3. This Key phrase is also the Key phrase for Block 3.
Embed the 2.txt file into the 2.jpg (image) file with steghide (command line). 
To confirm: You may try to extract your 2.txt file from the 2.jpg (image) file with steghide (command line) before you proceed to Block3.



Block3:- Key phrase to embed and extract file on steghide - S3Kur1ti
Create: 3.txt file (empty for now)
Use the Cyberchef (https://gchq.github.io/CyberChef/) to create some cyphertext:
	Generate a SHA3-256 hash of the key phrase, S3Kur1ti.
	Use the output to decrypt the cyphertext. 
	Encrypt FINAL SECRET MESSAGE (Trust Nothing, and Verify Everything.) with AES Encryption, use 31 zeros (0) as the Initialization Vector (IV), and your cyphertext as the Key.
	Copy the output and save it as your 3.txt file.
Embed the 3.txt file into the 3.jpg (image) file with steghide (command line). 

To confirm: You may try to extract your 3.txt file from the 3.jpg (image) file with steghide (command line).

