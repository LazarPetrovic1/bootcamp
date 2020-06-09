# Securing TCP/IP

### Making TPC/IP secure

**The CIA of security**:
1. *Confidentiality* - nobody can see the data being sent except for the recipient and the sender
1. *Integrity* - was data received in the same format it was sent; is it good in a way it should be good
1. *Availability* - can I gain access to my data if I really need it

***The core problems are balancing out the confidentiality and integrity, while making the application easy to use and contents thereof available.***

Additional things added to the CIA:
+ *Authentication* - giving someone the right to access something (username & pass/smart card/SSH key)
+ *Authorization* - permissions given to a person after authentication has been completed

*Non-repudiation* - concept tied to integrity: **if someone hands me something, I have no doubt that that's the person who handed it to me**

### Symmetric encryption

There are different methods of encryption and securing data, ranging from simple ciphers to full-fledged algorithms specifically designed for the purpose

The most popular is the Caesar's Cipher - increment (or decrement) a letter by a certain number (e.g increment by 1 means that A becomes B, B becomes C, C becomes D, etc)

Using Caesar's Cipher and incrementing the values by 3, the message *I love you* becomes *l oryh brx*

Vigenère cipher - Caesar's Cipher with a key. If the key is shorter, it will repeat until it completely covers the plaintext

Using Vigenère's Cipher with a key of 123:

I love you
1231231231
__________
J opxh arv

**Symmetric encryption** works like Vigenère cipher: using a key a value is encrypted: a cyphertext is returned as a value. The same key is used for decrypting the cyphertext.

Common in wereless networks - RC4 or AES
