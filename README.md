# Steganography-CS101-Project
Steganography is storing and hiding information to be conveyed within another object such that the presence of that information is not visible to human inspection. In this system we store the message inside the image by changing its pixel values according to the binary code of the message.This produces just a minor change in the pixels which is not visible directly thus making it safe to transfer across the network to a particular user. The encryption is made using the Diffie Hellman Key Exchange Concept that involves the use of public and private keys. This algorithm generates a unique communication key between the users. The image after encryption is sent to the receiver, who using that communication key can decrypt the message from the image pixels. Even if the other users in the network get hold of that encrypted image none would be able to decrypt the message unless they get to know the communication key between the sender and the receiver, thus making a secure way of transmitting information without any leakage.


Technical-Details
Let’s look at the journey of our encryption process
1) The individuals using the system first input their username into the database and a private key is generated randomly for them.
2) With the help of the private key a public key is calculated for each user and stored in a google sheet accessible to all
3) For message transference,  a communication key is generated using public key of receiver and private key of sender.
4) After all this, the sender chooses an image to encrypt his/her message in it.
5) The message is then converted to its ASCII value  and then to binary and stored in the image.
6) Using the algorithm, the message in its binary form is encrypted into the image and the user then sends it to the receiver.

Now let’s look at the journey of our decryption process
1) To decrypt the image the user enters the name of the sender and his private key. With the help of the  google sheet, public key of the sender is found..
2) From the private key of the receiver and the public key of sender, the communication key is generated which is used to find the offset and the gap.
3) This communication key is the same as that calculated for the sender, the proof of which is given ahead
4) With offset and gap, Least Significant bits of pixels are extracted and paired in group of 7 and then the binary digits are converted to alphabets to get the message.  

Implementation
Python is used for the implementation of all the codes used in our project. This was primarily due to the amount of in built functions and libraries present in it already which helped us write the code efficiently. Also file handling was easier to manage in python compared to other programming languages. To maintain the database of usernames and public keys we are simply using an excel sheet.
LIBRARIES USED AND SYSTEM REQUIREMENTS :-
I) Python Imaging Library
II) Google Client Library

Potential Applications
1)   The biggest application of the system is the end to end encrypted exchange of confidential data between a user and a receiver.
2)   This interface can also be used to encrypt a watermark into an image. The party owning the image can simply embed their name or some data into the image and to prove their claim, they can simply decrypt the image.

Team Members:
1)Ojas Jain 
2)Samarth Singhal 
3)Sanat Gupta 
4)Siddharth Verma 
