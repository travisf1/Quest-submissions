# Quest-submissions
Emerald City Academy- Beginner Cadence Bootcamp (June 2022)

# Chapter 1 Day 1 

1- A blockchain is a distributed database that stores information electronically in digital format. It is structured so that all users contain control rather than a centralized third party. Blockchain differs from a standard database due to the way it compiles information in “blocks” and chains them together so that there is an irreversible timeline of data. For applications of blockchain such as Bitcoin, this means transactions are permanently recorded and can be viewed by anyone. Security within blockchain can be attributed to the decentralized nature, where the information is spread out between multiple network nodes. This means that if the information held within one node is altered, the others can cross reference the information within them and determine the node that has incorrect information. 

2- Smart contracts are computer codes that are built into blockchains in order to facilitate, verify, or negotiate contract agreements. They operate after users agree on terms of an agreement and set of conditions. Once the set of conditions are met the smart contract carries out the terms of the agreement. This helps participants of said agreements to be certain of the outcome without any type of intermediary.

3- The difference between a script and a transaction is that a transaction changes the data on the blockchain, whereas a script is used to view data on the blockchain. Transactions typically cost money to pay for gas fees, execution etc… This can be different amounts based on the blockchain you use. 

# Chapter 1 Day 2  
1- The five cadence programming pillars are: Safety/Security, Clarity, Approachability, Developer Experience, and Resource Oriented Programming

2-These pillars are useful for a multitude of reasons. The clarity, approachability, and developer experience allows new users to be able to learn cadence and develop smart contracts for the flow blockchain. It also helps keep the code easy to read so that is can be verified as safe when audited. Safety/Security is the most important factor because without it, nobody would use the platform.


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




# Chapter 3 Day 1

1-
Resources differ from structs due to the fact that they can only exist in one location, they must be used, and they cannot be copied. This makes them more secure than a struct, and handling them requires much more explicit directions. 

2-
A resource might be better to use than a struct when handling an asset that we do not want to destroy due to a mistake such as a valuable NFT. This is because resources can only be lost through the actual “destroy” keyword. 

3-
The keyword to make a new resource is “create” 

4-
No, resources can only be created within contracts.  

5-
the type is @Jacob

6-
![image](https://user-images.githubusercontent.com/106039625/172456337-05d9b9b3-9771-48cb-8307-74a1843901a6.png)


# Chapter 3 Day 2


![image](https://user-images.githubusercontent.com/106039625/172717676-3ac1999e-23f8-478e-a432-d5aade96d149.png)


![image](https://user-images.githubusercontent.com/106039625/172717772-186d1c29-7bd0-4dd1-9401-88a082eae640.png)


# Chapter 3 Day 3 

1-
![image](https://user-images.githubusercontent.com/106039625/172887367-a85d5bfc-2eb4-47aa-a3be-a0ae2190473d.png)


2-
![image](https://user-images.githubusercontent.com/106039625/172887437-18c52b10-5966-4c60-9495-34ab05e2e7a4.png)


3-
References can be useful in cadence primarily in order to modify resources without having to move them around.

# Chapter 3 Day 4

1-
Resource interfaces can be used to set requirements for a resource to implement, as well as being used to expose/limit exposure to specific things within a resource by using restricted types.



2-
![image](https://user-images.githubusercontent.com/106039625/173620341-811a6fbe-f613-4dea-b1d4-25a5415d7455.png)

3-
I fixed the first error by defining the “favouriteFruit” variable within the struct, as well as initializing it. The second error was fixed by adding 
```cadence 
pub fun changeGreeting(newGreeting: String): String
``` 
to the struct interface.

![image](https://user-images.githubusercontent.com/106039625/173624952-21de3044-0a35-43c4-a28f-e32f72babed5.png)

# Chapter 3 Day 5

![image](https://user-images.githubusercontent.com/106039625/173666922-c2a8e26a-b726-4836-83ef-7f623b043511.png)


# Chapter 4 Day 1

1-
Contract code and Account storage. Contract code is basically any contracts within the account and account storage is where data is held.

2- 
/storage/ - This is only accessible by the owner of the account by using AuthAccount. This should only be done in transactions.

/public/ - Accessible to anyone, as well as anywhere (contract, scripts, transactions). 

/private/- Available to the owner of the account and those given permission by the owner.

/public/ and /private/ both "look" at /storage/, where the data is actually stored.

3-
.save()- saves the resources to a /storage/ path within account storage
 
.load()-  takes the data out of account storage as an optional.
 
.borrow()- gets a reference to the resource within account storage. Does not move the actual resource.


4-
Scripts can only be used to view data, not modify or move it.

5-
Other people can not save things to your account because doing so requires the account owner to sign the transaction in order to provide their AuthAccount as a paramter within the prepare phase of the transaction. 

6-
Contract
![image](https://user-images.githubusercontent.com/106039625/173869489-679542cf-55ac-46ec-8547-e3eb2797c587.png)


Transaction 1
![image](https://user-images.githubusercontent.com/106039625/173869698-929268b3-76a5-441e-85e6-3beb89f7e2d4.png)


Transaction 2
![image](https://user-images.githubusercontent.com/106039625/173869844-95e6ead4-f518-4331-a676-5b7d50dadfee.png)



# Chapter 4 Day 2

1-

Links a resource to the /public/ or /private/ path by creating a reference to data held in /storage/ 

2- 

Resource interfaces can be used to control what is exposed to the /public/ path because you can create a link to the resource, you can restrict the reference to use the resource interface. Within the resource interface, you can specify which parts of the resource you want to be implemented. Any variables/functions that are present in the resource but not the resource interface will not be accessible within the reference link. 

3-

Contract:

![image](https://user-images.githubusercontent.com/106039625/173991289-ea84e814-5a11-4d2a-aa2f-78ef39563199.png)


Transaction:

![image](https://user-images.githubusercontent.com/106039625/173991362-c4a35cd4-7cdb-4460-ba01-e18f9cfde5da.png)


Scripts:
![image](https://user-images.githubusercontent.com/106039625/173991502-0ac17224-36c4-4a67-a690-6e7c34fc8bd7.png)

![image](https://user-images.githubusercontent.com/106039625/173991643-39b23264-7959-4a55-83fe-7f9279a7a1f8.png)


# Chapter 4 Day 3

1-

So others can deposit NFT’s into our collection without requiring access to our account storage. 


Making it so that we can wrap our NFT’s into the collection and use one storage path instead of having a different storage path for each NFT. 


2-

If you have nested resources you must declare a destroy function


3-


We would want to add a way to either restrict the ability to mint new NFTs or place a cap on the supply. 

No, it would be better to make references to resource interfaces that contain the information you want to be accessible while restricting the data that you want private. 



# Chapter 4 Day 4


```cadence
pub contract CryptoPoops {
  pub var totalSupply: UInt64

  // This is an NFT resource that contains a name,
  // favouriteFood, and luckyNumber
  pub resource NFT {
    pub let id: UInt64

    pub let name: String
    pub let favouriteFood: String
    pub let luckyNumber: Int

    init(_name: String, _favouriteFood: String, _luckyNumber: Int) {    //sets values for NFT resource variables
      self.id = self.uuid

      self.name = _name
      self.favouriteFood = _favouriteFood
      self.luckyNumber = _luckyNumber
    }
  }

  // This is a resource interface that implements the Collection resource and allows us to reference chosen variables and functions while ...(cont) 
// restricting the data within the resource that we do not want exposed such as the withdraw function
  pub resource interface CollectionPublic {
    pub fun deposit(token: @NFT)          // this will allow other to deposit NFTs into our collection
    pub fun getIDs(): [UInt64]                // this will allow the public to see our NFT ID within our public collection reference
    pub fun borrowNFT(id: UInt64): &NFT       // this will allow the public to get a reference to a resource we hold within our storage and read  ...(cont)
    //our NFT without having to withdraw it.
  }

  pub resource Collection: CollectionPublic { //this is a resource referenced by the CollectionPublic interface. the collection wraps our NFT's so...(cont)
      //...we can save them under one storage path. 
    pub var ownedNFTs: @{UInt64: NFT}

    pub fun deposit(token: @NFT) {                    //explained above in resource interface
      self.ownedNFTs[token.id] <-! token
    }

    pub fun withdraw(withdrawID: UInt64): @NFT {            //this allows us to withdraw NFT's from our collection
      let nft <- self.ownedNFTs.remove(key: withdrawID) 
              ?? panic("This NFT does not exist in this Collection.")
      return <- nft
    }

    pub fun getIDs(): [UInt64] {                        //explained above in resource interface
      return self.ownedNFTs.keys
    }

    pub fun borrowNFT(id: UInt64): &NFT {             //explained above in resource interface
      return (&self.ownedNFTs[id] as &NFT?)!
    }

    init() {                        
      self.ownedNFTs <- {}
    }

    destroy() {                               //destroys the nested resource 
      destroy self.ownedNFTs
    }
  }

  pub fun createEmptyCollection(): @Collection {         //this creates our collection that we wrap our NFT resources in   
    return <- create Collection()
  }

  pub resource Minter {  //this resource is what holds the function that allows the NFT to be minted and should be owned by whoever deployed the contract.        

    pub fun createNFT(name: String, favouriteFood: String, luckyNumber: Int): @NFT { //this function creates the 
      return <- create NFT(_name: name, _favouriteFood: favouriteFood, _luckyNumber: luckyNumber)
    }

    pub fun createMinter(): @Minter {  //This function creates the Minter resource so that it can be saved to the contract deployers account. 
      return <- create Minter()
    }

  }

  init() {
    self.totalSupply = 0
    self.account.save(<- create Minter(), to: /storage/Minter) //saves Minter resource to account of contract deployer
  }
}
```

# Chapter 5 Day 1


1-
Events are basically a way to announce that something happened. This could be useful to add transparency within a program, or to mark milestones such as “1,000,000th nft mint”.

2 & 3- (Correction, flip > and < signs)

![image](https://user-images.githubusercontent.com/106039625/174162283-5f68d316-8575-4f6f-a33d-1ae0f041f8cf.png)


4-
numberOne:
Yes, this function will log the name.

numberTwo:
Yes, the function will return the value. 

numberThree:
No, it will have an error due to the post condition. 
Self.number is initialized at 0 then set to increment by 1 and return self.number. However, because 1 does not == (result + 1), the post condition will  fail and it will be an error.

# Chapter 5 Day 2

1- Having NFT contract standards makes it easier for clients such as DApps to interact with multiple NFT contracts without having to implement different functionality for each one. 

2- Pizza or Cereal


3-

Contract Interface-
![image](https://user-images.githubusercontent.com/106039625/174187416-3f69a0d8-7082-4985-9262-c95cf39c3502.png)

Implementing Contract- (CORRECTION- updateNumber function should set self.number to newNumber)
![image](https://user-images.githubusercontent.com/106039625/174187485-d33410cf-7d5d-48f4-a819-3493782b7d3c.png)


# Chapter 5 Day 3

1-

Force casting with as! Downcasts a generic resource type to be a more specific type or panics if it does not work.. This is useful to have in our collection for when others try to deposit NFT’s into our account. Using as! We can downcast it to a more specific NFT type to make sure not just any generic NFT type can be deposited.

2-

Auth gives you an authorized reference. We must use this when we need to downcast a reference. 

3-
### Contract
```cadence
import NonFungibleToken from 0x02
pub contract CryptoPoops: NonFungibleToken {
  pub var totalSupply: UInt64

  pub event ContractInitialized()
  pub event Withdraw(id: UInt64, from: Address?)
  pub event Deposit(id: UInt64, to: Address?)

  pub resource NFT: NonFungibleToken.INFT {
    pub let id: UInt64

    pub let name: String
    pub let favouriteFood: String
    pub let luckyNumber: Int

    init(_name: String, _favouriteFood: String, _luckyNumber: Int) {
      self.id = self.uuid

      self.name = _name
      self.favouriteFood = _favouriteFood
      self.luckyNumber = _luckyNumber
    }
  }

  pub resource interface MyCollectionPublic {
        pub fun deposit(token: @NonFungibleToken.NFT)
        pub fun getIDs(): [UInt64]
        pub fun borrowNFT(id: UInt64): &NonFungibleToken.NFT
        pub fun borrowAuthNFT(id: UInt64): &NFT
  }
 
  pub resource Collection: NonFungibleToken.Provider, NonFungibleToken.Receiver, NonFungibleToken.CollectionPublic, MyCollectionPublic {
    pub var ownedNFTs: @{UInt64: NonFungibleToken.NFT}

    pub fun withdraw(withdrawID: UInt64): @NonFungibleToken.NFT {
      let nft <- self.ownedNFTs.remove(key: withdrawID) 
            ?? panic("This NFT does not exist in this Collection.")
      emit Withdraw(id: nft.id, from: self.owner?.address)
      return <- nft
    }

    pub fun deposit(token: @NonFungibleToken.NFT) {
      let nft <- token as! @NFT
      emit Deposit(id: nft.id, to: self.owner?.address)
      self.ownedNFTs[nft.id] <-! nft
    }

    pub fun getIDs(): [UInt64] {
      return self.ownedNFTs.keys
    }

    pub fun borrowNFT(id: UInt64): &NonFungibleToken.NFT {
      return (&self.ownedNFTs[id] as &NonFungibleToken.NFT?)!
      }

    pub fun borrowAuthNFT(id: UInt64): &NFT {
      let ref = (&self.ownedNFTs[id] as auth &NonFungibleToken.NFT?)!
      return ref as! &NFT
      }

    init() {
      self.ownedNFTs <- {}
    }

    destroy() {
      destroy self.ownedNFTs
    }
  }

  pub fun createEmptyCollection(): @NonFungibleToken.Collection {
    return <- create Collection()
  }

  pub resource Minter {

    pub fun createNFT(name: String, favouriteFood: String, luckyNumber: Int): @NFT {
      return <- create NFT(_name: name, _favouriteFood: favouriteFood, _luckyNumber: luckyNumber)
    }

    pub fun createMinter(): @Minter {
      return <- create Minter()
    }

  }

  init() {
    self.totalSupply = 0
    emit ContractInitialized()
    self.account.save(<- create Minter(), to: /storage/Minter)
  }
}
```

### NonFungibleToken Standard Contract Interface

```cadence
/**
## The Flow Non-Fungible Token standard
*/

// The main NFT contract interface. Other NFT contracts will
// import and implement this interface
//
pub contract interface NonFungibleToken {

    pub var totalSupply: UInt64

    pub event ContractInitialized()

    pub event Withdraw(id: UInt64, from: Address?)

    pub event Deposit(id: UInt64, to: Address?)

    pub resource interface INFT {
        // The unique ID that each NFT has
        pub let id: UInt64
    }

    pub resource NFT: INFT {
        pub let id: UInt64
    }

    pub resource interface Provider {
        pub fun withdraw(withdrawID: UInt64): @NFT {
            post {
                result.id == withdrawID: "The ID of the withdrawn token must be the same as the requested ID"
            }
        }
    }

    pub resource interface Receiver {
        pub fun deposit(token: @NFT)
    }

    pub resource interface CollectionPublic {
        pub fun deposit(token: @NFT)
        pub fun getIDs(): [UInt64]
        pub fun borrowNFT(id: UInt64): &NFT
    }

    pub resource Collection: Provider, Receiver, CollectionPublic {

        // Dictionary to hold the NFTs in the Collection
        pub var ownedNFTs: @{UInt64: NFT}

        // withdraw removes an NFT from the collection and moves it to the caller
        pub fun withdraw(withdrawID: UInt64): @NFT

        // deposit takes a NFT and adds it to the collections dictionary
        // and adds the ID to the id array
        pub fun deposit(token: @NFT)

        // getIDs returns an array of the IDs that are in the collection
        pub fun getIDs(): [UInt64]

        // Returns a borrowed reference to an NFT in the collection
        // so that the caller can read data and call methods from it
        pub fun borrowNFT(id: UInt64): &NFT {
            pre {
                self.ownedNFTs[id] != nil: "NFT does not exist in the collection!"
            }
        }
    }

    pub fun createEmptyCollection(): @Collection {
        post {
            result.getIDs().length == 0: "The created collection must be empty!"
        }
    }
}
```
### Create Collection Transaction 

```cadence
import CryptoPoops from 0x01
import NonFungibleToken from 0x02

transaction {

  prepare(acct: AuthAccount) {
  acct.save(<- CryptoPoops.createEmptyCollection(), to: /storage/Collection)
  acct.link<&CryptoPoops.Collection{NonFungibleToken.CollectionPublic, CryptoPoops.MyCollectionPublic}>(/public/Collection, target: /storage/Collection)
  }

  execute {
    log("stored a collection for cryptopoops")
  }
}
```

### Deposit/Mint Transaction
```cadence
import CryptoPoops from 0x01
import NonFungibleToken from 0x02

transaction(recipient: Address) {

    prepare(acct: AuthAccount) {
        let nftMinter = acct.borrow<&CryptoPoops.Minter>(from: /storage/Minter)!

        let publicReference = getAccount(recipient).getCapability(/public/Collection)
                    .borrow<&CryptoPoops.Collection{NonFungibleToken.CollectionPublic}>()
                    ?? panic("This account does not have a collection")
    
        publicReference.deposit(token: <- nftMinter.createNFT(name: "Travis", favouriteFood: "Pizza", luckyNumber: 44))
    }


    execute {
    log("store new NFT into collection")
    }
}
```

### Script for ID
```cadence
import CryptoPoops from 0x01
import NonFungibleToken from 0x02

pub fun main(account: Address): [UInt64] {
let publicReference = getAccount(account).getCapability(/public/Collection)
                .borrow<&CryptoPoops.Collection{NonFungibleToken.CollectionPublic}>()
                                      ?? panic("This account does not have a collection")
return publicReference.getIDs()

}
```



### Final Script-
```cadence
import CryptoPoops from 0x01
import NonFungibleToken from 0x02

pub fun main(account: Address, id: UInt64): String {
let publicReference = getAccount(account).getCapability(/public/Collection)
                .borrow<&CryptoPoops.Collection{CryptoPoops.MyCollectionPublic}>()
                                      ?? panic("This account does not have a collection")

log(publicReference.borrowAuthNFT(id: id).favouriteFood)
log(publicReference.borrowAuthNFT(id: id).luckyNumber)
log(publicReference.borrowAuthNFT(id: id).name)
return "Am I done?"

}
```

Result-
![image](https://user-images.githubusercontent.com/106039625/174389251-e2120433-f33c-486a-9837-242ab65af197.png)


