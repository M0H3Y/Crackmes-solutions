# Challenge Link

[Secret CrackMe](https://crackmes.one/crackme/5e18007c33c5d419aa013585)

# Level 
2

# Description

>Either you can get the secret(which might be challenging though), and the flag will be provided, or you can just manipulate the program to get the flag directly :).
Enjoy!

# Solution 
First, Let's open this executable in IDA and see how it works. 

![](images/Secret_CrackMe_1.PNG)

As we can see, there is some comparison made with my input, and if the result of this comparison is false, it will print `Secret is not valid. Try again.` otherwise, it will make a bunch of other comparisons. 

If we take a look at the function `sub_40177f`....it seems that it's the function that prints our flag but after making a lot of operatios on it.


So, we can bypass all those comparisons to get the function `sub_40177f` called and see what it prints.

So let’s open up ollydbg and play around with the program to make it call that function at 40177f. 

![](images/Secret_CrackMe_2.PNG)

# FLAG

FLAG-{Dr0wn1ngDuck}
