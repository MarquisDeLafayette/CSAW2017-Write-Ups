# CSAW CTF 2017 Quals: Best Router

**Category:** Forensics
**Points:** 200
**Solves:** 240
**Description:**

Best Router

http://forensics.chal.csaw.io:3287

NOTE: This will expand to ~16GB!

19:00 Eastern: updated. Old flags have been removed.

## Write-up

So the challenge send you to a login page and using the developer tools you find pretty quickly that the website was written in perl which is the first clue/hint you'll find.

So now you decompress and mount the image that you are given. 

You now can search for the login.pl file with grep.

grep -r login.pl /path/to/mounted/image/*

Which shows you the various places where you can find a file called login.pl. In this case it so happens that you find in the same folder several files that are of interest. You see flag.txt which is empty, password.txt, and username.txt.

username.txt = admin
password.txt = iforgotaboutthemathtest

So if you go back to the login page and input the credentials you'll find the flag. Honestly it was a pretty easy forensics challenge and shouldn't have been valued as high as it was. 

### Flag

`flag{but_I_f0rgot_my_my_math_test_and_pants}`
