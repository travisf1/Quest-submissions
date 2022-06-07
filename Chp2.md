# Chapter 2 Day 1

1- (Question) 

Deploy a contract to account 0x03 called "JacobTucker". Inside that contract, declare a constant variable named is, and make it have type String. Initialize it to "the best" when your contract gets deployed.

Check that your variable is actually equals "the best" by executing a script to read that variable. Include a screenshot of the output.



(Answer)

![image](https://user-images.githubusercontent.com/106039625/170081588-0f5731ad-33d0-4811-9f0d-635d92154c35.png)



![image](https://user-images.githubusercontent.com/106039625/169721017-d84d22a5-459f-464a-a0cc-2440eb682b6e.png)




# Chapter 2 Day 2

1- The reason we would not call changeGreeting in a script is because a script is only used to view the information, it can not be used to actually change the data. 

2- In the prepare phase, Authaccount means that the user approves of the transaction. This is what actually allows the transaction to access the data within your account, which can only be done in the prepare phase.

3- The difference between the prepare and execute phase is that the information in your account can only be accessed in the prepare phase. The execute phase can call functions but is mainly utilized to separate the logic from the prepare phase in order to clear up the code.

4- (Question)
Add two new things inside your contract:

A variable named myNumber that has type Int (set it to 0 when the contract is deployed)
A function named updateMyNumber that takes in a new number named newNumber as a parameter that has type Int and updates myNumber to be newNumber
Add a script that reads myNumber from the contract

Add a transaction that takes in a parameter named myNewNumber and passes it into the updateMyNumber function. Verify that your number changed by running the script again.



(Answers)

![image](https://user-images.githubusercontent.com/106039625/169858736-016d5ee0-ed6f-49aa-b813-4371346b61cb.png)


![image](https://user-images.githubusercontent.com/106039625/169858914-343f15cd-085e-4476-8865-3c70c28fc376.png)


![image](https://user-images.githubusercontent.com/106039625/169858991-f5de0241-55e4-4ed3-9b12-eeda6051389c.png)


![image](https://user-images.githubusercontent.com/106039625/169859049-3801694b-47a6-4630-8a07-a25dc995fae3.png)




# Chapter 2 Day 3

1- (Question)
In a script, initialize an array (that has length == 3) of your favourite people, represented as Strings, and log it.

(Answer)

![image](https://user-images.githubusercontent.com/106039625/170078960-83e6b048-6523-4d08-b6c4-1c6d9133da0d.png)

2- (Question) 
In a script, initialize a dictionary that maps the Strings Facebook, Instagram, Twitter, YouTube, Reddit, and LinkedIn to a UInt64 that represents the order in which you use them from most to least. For example, YouTube --> 1, Reddit --> 2, etc. If you've never used one before, map it to 0!


(Answer)

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


# Chapter 2 day 4

![image](https://user-images.githubusercontent.com/106039625/172391821-11617915-1f60-4140-b311-b9b6ed5bb975.png)

![image](https://user-images.githubusercontent.com/106039625/172391973-ccf49083-7e6e-49f4-8d5e-45c03e970fc7.png)

![image](https://user-images.githubusercontent.com/106039625/172392196-27e5cbb6-4b37-4c40-af92-c666a1534454.png)


pub contract Authentication {

    pub var contacts: {Address: Contact}
    
    pub struct Contact {
        pub let firstName: String
        pub let discord: String
        pub let twitter: String
        pub let account: Address

        // You have to pass in 4 arguments when creating this Struct.
        init(_firstName: String, _discord: String, _twitter: String, _account: Address) {
            self.firstName = _firstName
            self.discord = _discord
            self.twitter = _twitter
            self.account = _account
        }
    }

    pub fun addProfile(firstName: String, discord: String, twitter: String, account: Address) {
        let newProfile = Contact(_firstName: firstName, _discord: discord, _twitter: twitter, _account: account)
        self.contacts[account] = newProfile
    }

    init() {
        self.contacts = {}
    }

}

pub contract Authentication {

    pub var contacts: {Address: Contact}
    
    pub struct Contact {
        pub let firstName: String
        pub let discord: String
        pub let twitter: String
        pub let account: Address

        // You have to pass in 4 arguments when creating this Struct.
        init(_firstName: String, _discord: String, _twitter: String, _account: Address) {
            self.firstName = _firstName
            self.discord = _discord
            self.twitter = _twitter
            self.account = _account
        }
    }

    pub fun addContact(firstName: String, discord: String, twitter: String, account: Address) {
        let newContact = Contact(_firstName: firstName, _discord: discord, _twitter: twitter, _account: account)
        self.contacts[account] = newContact
    }

    init() {
        self.contacts = {}
    }

}
import Authentication from 0x01

transaction(firstName: String, discord: String, twitter: String, account: Address) {

    prepare(signer: AuthAccount) {}

    execute {
    Authentication.addContact(firstName: firstName, discord: discord, twitter: twitter, account: account)
        log("We're done.")
    }
}

