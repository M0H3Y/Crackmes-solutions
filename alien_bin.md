# Challenge Link

[alien_bin](https://crackmes.one/crackme/5d78168833c5d46f00e2c428)

# Level 
2

# Description

>In the ruins of an ancient alien civilization a micro sd card was found with this binary inside. It's asking us to feed it a password, but we don't know where to get it from! We've tried all of our birthdays right way and backwards here at the lab, but nothing seems to work :( Maybe we missed something.



# Solution 

We are given a 64-bit ELF. when executing it, it asks for the password. 

![](images/alien_bin_1.png)

we can use `ltrace` which intercepts the dynamic library calls so we can see if there is a call to strcmp and what arguments are passed to it.

![](images/alien_bin_2.png)

Here we can see there is a call to strcmp with 2 parameters `mo` which is my input and `bd23cf3f56baa86bc` which is the right password.

![](images/alien_bin_3.png)

