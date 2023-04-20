# Lab Report 2

## Part I 


## Part II

I choose the `averageWithoutLowest` as the bug I will be explaing. 

Here is failure induced input I applied to the test:
![image](failure_induced.png)

Here is the input that does not induce an error:
![image](no_failure.png)

Here are the symptoms:
![image](symptoms.png)

This is the before:
![image](before_bugfix.png)

This is the after bug fix:
![image](fixed.png)

Before fixing the bug, the method fitlered out all the lowest values when there is more than one duplicates of the lowest value in the input array. We fix the bug by summing up all the values from the array and only took out one of the lowest value. As you can see from the symptoms from the failure-induced input, the expected value is larger than the actual value. 


## Part III
From week 2 lab I learned how to workign with server remotely and open up a server using the `-curl` command. This is especially helpful, because this allows the programmer to access the server without working browser. From week 3, I learned how to wrtie a JUnit test and create failure-inducing inputs. I did not know the importance of inducing the failure from your test, since I'va always thought the code is good enough as long as I got the program to work form a few commands.
