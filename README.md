# 8 Numbers Wordlist for WIFI hash bruteforce

 Wordlist contains all possible combinations of eight-digit numbers. Most suitable for bruteforcing the hash of captured wifi handshakes

 First of all, I would like to say that you will find it easier to create such a password yourself using the Crunch Utility.

https://www.kali.org/tools/crunch/

_crunch 8 8  0123456789 -o 8numbersWordlist.txt_

 The first two numbers are responsible for the length of the password: a minimum of 8 characters and a maximum of 8 characters. Next we list all the characters we want to use to generate the password: this can be numbers, letters or any other character. The -o flag will put the result of the generation into a file with the name "8numbersWordlist.txt".


 The vast majority of popular ISPs provide their customers with routers. The password is 8 randomly generated digits. In addition, many public wireless networks, such as coffee shops, choose the simplest password, such as 12345678, to make it easier for customers to connect. 

 All of this makes life much easier for a hacker trying to gain unauthorised access to the network. Once a WPA handshake is intercepted, it is only a matter of time before a hacker can find a password for such a network.

 When Wired Equivalent Privacy (WEP) technology was first introduced, it was proved ineffective and easy to hack. WEP was replaced by a new privacy algorithm called WPA (Wi-Fi Protected Assets).  This made hacking more difficult, but not impossible.
From 2006, the WPA2 protocol was introduced. It uses the AES encryption algorithm, which is very difficult to crack. The disadvantage of WPA2 is that the encrypted password is transmitted when users connect during the so-called 4-way handshake. If we intercept the handshake, we know the encrypted password, and all we have to do is decrypt it. Here we will not look at how to intercept this WPA handshake: youtube is full of tutorials on this topic. In my opinion, the easiest way to get the handshake is to use the wifite2 utility.

https://github.com/derv82/wifite2

To crack a password, we can use tool called aircrack-ng

_aircrack HANDSHAKE.cap -w WORDLIST.txt_


![](https://i.imgur.com/cvpYrx3.png)
