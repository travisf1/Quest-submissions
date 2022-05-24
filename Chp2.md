Chapter 2 Day 1

1-
![image](https://user-images.githubusercontent.com/106039625/169721017-d84d22a5-459f-464a-a0cc-2440eb682b6e.png)

Chapter 2 Day 2

1- The reason we would not call changeGreeting in a script is because a script is only used to view the information, it can not be used to actually change the data. 

2- In the prepare phase, Authaccount means that the user approves of the transaction. This is what actually allows the transaction to access the data within your account, which can only be done in the prepare phase.

3- The difference between the prepare and execute phase is that the information in your account can only be accessed in the prepare phase. The execute phase can call functions but is mainly utilized to separate the logic from the prepare phase in order to clear up the code.

4-
![image](https://user-images.githubusercontent.com/106039625/169858736-016d5ee0-ed6f-49aa-b813-4371346b61cb.png)

![image](https://user-images.githubusercontent.com/106039625/169858914-343f15cd-085e-4476-8865-3c70c28fc376.png)

![image](https://user-images.githubusercontent.com/106039625/169858991-f5de0241-55e4-4ed3-9b12-eeda6051389c.png)

![image](https://user-images.githubusercontent.com/106039625/169859049-3801694b-47a6-4630-8a07-a25dc995fae3.png)




Chapter 2 Day 3

1-
![image](https://user-images.githubusercontent.com/106039625/170078960-83e6b048-6523-4d08-b6c4-1c6d9133da0d.png)

2-
![image](https://user-images.githubusercontent.com/106039625/170079071-1bf9e569-9849-4afe-89c4-9dd93f4b4f4a.png)

3- 

The Force-Unwrap operator !, gets rid of optional types unless the “thing” it attempts to unwrap is nil, which causes it to abort.

For example:  

var name1: String? = "Travis"
var unwrappedName1: String = name1!

Since the name “Travis” is not nil, the optional was unwrapped to String, instead of the optional type, “String?”. 


4-
The error message means that it expected a String type, but got a String optional (String?)

This is occurring because the return subject they used was an address type, not a string type. 

In order to fix this, a force-unwrap operator ! needs to be placed at the end of the return thing[0x03]. This returns it to the actual type, string, since there is no nil.

![image](https://user-images.githubusercontent.com/106039625/170079419-c2716f05-e303-4e04-8445-0017ad5d8194.png)







