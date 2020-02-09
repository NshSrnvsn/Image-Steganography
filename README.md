## Image-Steganography

# What is Steganography?
  
  Steganography is “an art of secret writing”. Its goal is to conceal the fact of communication. Steganography includes the concealment of information within computer files. In digital steganography, electronic communications may include steganographic coding inside of a transport layer, such as a document file, image file, program or protocol. Media files are ideal for steganographic transmission because of their large size. For example, a sender might start with an innocuous image file and adjust the color of every hundredth pixel to correspond to a letter in the alphabet. The change is so subtle that someone who is not specifically looking for it is unlikely to notice the change.
In the digital age, steganography is increasingly being used by hackers and criminals to covertly communicate sensitive information. It is even being used as a means of bypassing network defenses to communicate with malware.



# Steganography Vs Cryptography

  The advantage of steganography over cryptography alone is that the intended secret message does not attract attention to itself as an object of scrutiny. Plainly visible encrypted messages, no matter how unbreakable they are, arouse interest and may in themselves be incriminating in countries in which encryption is illegal.
Whereas cryptography is the practice of protecting the contents of a message alone, steganography is concerned both with concealing the fact that a secret message is being sent and its contents.



# Terminology

  In steganography the payload is the data covertly communicated and the carrier is the signal, stream, or data file that hides the payload.


# Pixel concept and color models

  Pixels are the smallest individual element of an image. So, each pixel is a sample of an original image. It means, more samples provide more accurate representations of the original. The intensity of each pixel is variable. In color imaging systems, a color is typically represented by three or four component intensities such as red, green, and blue, or cyan, magenta, yellow, and black.
Here, we will work with the RGB color model. As you can imagine, the RGB color model has 3 channels, red, green and blue.
The RGB color model is an additive color model in which red, green and blue light are added together in various ways to reproduce a broad array of colors. The name of the model comes from the initials of the three additive primary colors, red, green, and blue. The main purpose of the RGB color model is for the sensing, representation and display of images in electronic systems, such as televisions and computers, though it has also been used in conventional photography.

So, each pixel from the image is composed of 3 values (red, green, blue) which are 8-bit values (the range is 0–255).
As we can see in the image above, for each pixel we have three values, which can be represented in binary code (the computer language).
When working with binary codes, we have more significant bits and less significant bits, as you can see in the image below.

The leftmost bit is the most significant bit. If we change the leftmost bit it will have a large impact on the final value. For example, if we change the leftmost bit from 1 to 0 (11111111 to 01111111) it will change the decimal value from 255 to 127.
On the other hand, the rightmost bit is the less significant bit. If we change the rightmost bit it will have less impact on the final value. For example, if we change the leftmost bit from 1 to 0 (11111111 to 11111110) it will change the decimal value from 255 to 254. Note that the rightmost bit will change only 1 in a range of 256 (it represents less than 1%).

# Image Types
  
  When it comes to digital images, specifically in regards to steganography, there are three primary classes. There file types are those with lossy-compression, those with lossless-compression, and raw file types. We are working with lossless-compression file types. Lossless and lossy compressed files types are most common in the world today because of their compact size.
Of these, raw files are typically the easiest to work with. However they tend to be very large files, are not commonly used by most consumers, and often require special software used professional photographers or enthusiasts in order to view and edit. Some examples of raw image file formats are RAW and DNG.

Lossless-compression means that the files are stored in a compressed format, but that this compression does not result in the actual data being modified when the file is opened, transported, or decompressed. For lossless files steganography is often accomplished by manipulating the least-significant bits (LSB) of the carrier file. Some examples of lossless-compression image file formats are PNG, TIFF, an BMP.

Lossy-compression is the opposite of lossless-compression. When lossy compression is used there is no guarantee that the file will not be modified slightly when subjected to storage, transmission, or decompression. In nearly all cases this modification will be imperceptible to the end user, otherwise it wouldn’t be very popular. However, since LSB steganography will modify these “unimportant” bits that can be lost during compression doing steganography on files with lossy-compression is more complex. This means we can’t risk using lossy compression that may not preserve our modifications. Some examples of lossy-compression image file formats are JPEG and BPG.


### Code

The Code included here includes 2 kinds. 
            

            1. User interface code- [GUI.py]
                This works for BMP format.
                
            2. Terminal code - [steg.py]
               This works for loseless image format (.png, .jpeg)


## Learn More

[Image Steganography in Cryptography]-https://www.geeksforgeeks.org/image-steganography-in-cryptography/

[Simple Image Steganography in Python]-https://hackernoon.com/simple-image-steganography-in-python-18c7b534854f
