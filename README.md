# Solidity, Blockchain, and Smart Contract Course – Beginner to Expert Python Tutorial
> Notes and code from course from freeCodeCamp.com
Available at this link: https://www.youtube.com/watch?v=M576WGiDBdQ


## Lesson 0: Welcome To Blockchain
Bitcoin was the first blockchain technology to take it mainstream as a some sort of digital gold.
In 1994 Nick Zabo proposed a new technology called smart contract.  

Ethereum takes this blockchain technology one step further because it can create smart contracts.

A **Smart Contract** is a self execution sets of instructions, without 3rd parties involved. A smart contract come to life in a decentralized environment called blockchain.  
Like a regular contract but its totally written in code, the terms of the agreement are written in code.

This revolutionary technology despite many advantages comes with a fatal flaw know as a **The Oracle Problem**.


This blockchain are deterministic systems basically meaning that everything that happens in this system happens in this wall guarded closed box, but if you want it to be this digital superior agreements they need to  interact with the real world and get data from the external world.

**Oracles** are devices that bring data or execute some type of external computation and they do it also in a decentralized manner in order to keep data and off-chain computation also decentralized like the smart contract, because centralized

The on-chain logic will be decentralized in the blockchain, but you also will need off-chain data and external computation decentralized as well in order to avoid single points of failures from centralized oracles. Combining this settlements layers and these off-chain data and external computation builds what's called **hybrid contracts**.


Protocol **Chain Link** is a decentralized modular oracle network that allows you to bring data into you smart contracts and do external computation in order for the smart contracts to do settlements and interact with the real world in some meaningful way. Chain link is the most popular oracle and is Chain agnostic meaning it will work if you are developing contract in ethereum, Polkadot Avalanche or any other platform.

Other tools have adopted ethereum and took it to another direction like Polygon, Avalanche, Polkadot and many more if we learn the core basics of smart contract development on the ethereum platform all these skills translate to these other chains as well.

Blockchain technology has many advantages like:

* Decentralized
* Transparency and Flexibility
* Speed and Efficiency
* Security and Immutability
* Removal of counterparty risk
* Trust minimized agreements (from brand base agreements to math base agreements)

>All these add to the two most important: Freedom and Trust

# Metamask

Install it as web browser extension, create new account, save the Mnemonic, write it down and store it some hidden and safe place.

| Concept | Can Acces | Private or Public|
| ------- |:---------:| -----------------|
| Mnemonic| All your accounts | Keep Private! |
| Private Key | 1 of your accounts | Keep Private! |
| Public Address | Nothing | It's Public |


**Ethereum Mainnet** is the main ethereum networks that works with real money and real values.

**Test Nets Networks** are ethereum networks that resemble the main network ethereum but don't work with real money.

A **faucet** is a wallet that give us fake unlimited ether.

**A block Explorer** is an application that allows us to 'view' transaction that happen on a blockchain.
https://etherscan.io/

**Gas** is the fee payed to a node operator for successfully include a transaction or modification in the blockchain. So gas is measure of computation use.

**Gas Price** How much it costs per unit of gas.

**Gas Limit** is the max amount of gas in a transaction willing to pay. In Metamask you can peek how much gas you want to pay on the upper limit in wei or gas.

**Transaction Fee**: Gas Used x Gas Price

**Wei** is the minimum unit in ether.

1 wei is equivalent to 0.000000000000000001 ether (17 zeros and a 1) and to 0.000000001 Gwei (8 zeros and a 1)

1 ether is equivalent to 1,000,000,000,000,000,000 wei, 1 Quintillion wei (a 1 and 18 zeros)

a **Gwei** is a 1 Billion wei, that is 1,000,000,000 wei (a 1 and 9 zeros) or also 0.000000001 Ether (9 zeros and a 1)


|1 Unit | Ether | Gwei | Wei |
|-------|-------|------ | ------|
| 1 Ether | 1 | 1,000,000,000 | 1,000,000,000,000,000,000|
| 1 Gwei | 0.000,000,001 | 1 | 1,000,000,000 |
| 1 Wei | 0.000,000,000,000,000,001 | 0.000,000,001 | 1 |

```
Transaction Fee Example:

 21,000 gas @ 1 GWEI per gas = 21,000 Gwei
```

In this transaction we will pay 21,000 transaction fee per this transaction.

Why we would want to pay more?? why we eve have the option to pay more??

Because node can only process a limit of transaction at a time. So a node has to decide why it need  to include my transaction into the block, and if there are many people the nodes are going to need an incentive  to prioritize those who are willing to pay more.

So gas price is based off the demand of the blockchain. The more people want to make transactions, the higher the gas price, and therefore the higher the transaction fees.

At https://ethgasstation.info/ you can se an estimate of how much time will take your transaction depending on how much are you willing ti pay.

---

## Understanding how a blockchain works

First is important to understand what a Hash is:

**Hash** is a unique fixed length string, meant to identify a piece of data. They are creating by placing said data into a "hash function".
To see an example of a hash function  go to: https://emn178.github.io/online-tools/keccak_256.html
or to
https://andersbrownworth.com/blockchain/hash


For example if you write "dog" when it is "hashed" using the *SHA256* algorithm it outputs the following Hash:

> cd6357efdd966de8c0cb2f876cc89ec74ce35f0968e11743987084bd42fb8944

but if we put now "dog and a cat" it hashes to:

> 2d18833fcfd98e3ce3bebef0faf6f936c974814854528ae56a30926b17acc2de

The important thing to understand is that data, combined with a Nonce, a Block Number and with a previous hash is combined to form a new Hash

To see how a Hash is combined to form a Blockchain see the next explanation video at https://andersbrownworth.com/blockchain/

**Genesis Block** is the first block in a Blockchain

**Mining** is the process if finding the solution to the blockchain problem, the problem is to find a hash that starts with a given number of zeros.

**Block** is a list of transaction mined together

**Nonce** is a number used once to find the solution to the blockchain problem. It is also used to define the transaction number for an account/address.

**Node** a single instance of the many validators running the blockchain.

---

## Private Key and Public Key Cryptography

**Private Key** Only known to the key holder, it is used to sing a transaction or a message, (kind like a password, remember to keep it secret).

For example, this is private Key using RSA Algorithm:
> -----BEGIN RSA PRIVATE KEY-----
MIICfdssdfKBgQC1uHHsPSPXMwVzIVfuhimmvVsdfdsKzLPngscZ90vN07h8NjRC0u
i52xhnMrLfdssfdKNs+Ci1jn/8vfU+T3gaoWvvbdsdffhx3P9Urq5o9vNmtJJXWyQ8L
Sypmh6R8yWD/7etka+qRzwYq/nreF7nzVbqJXs953+FkEkJmAlv/S5BzQwIDAQAB
AoGBAI9Dvu0UtrDulJlT7FMsiqHeHXX5c4E42t2PJruOOoy4WB5mnYhYohZXfWzK
+y5WR6L9uxasdP77EQFgec03nubZg2cC+QNQ8Y/aBR7WbdudCtexziAZrB/RQY
Gd9IlW2yauHKWIPmhLIQnQXHs4YEqhUvFbg+mRzYhjmpEBRBAkEA9cG/7EsLrv/9
KtblrTe1oYGI2OwSNZvmy7fAQTHLpdr0SHMZl/JQkrnwYuw2zgk0hmargt29k5s
4sNgI78qqwJBAL1La8eQdgNnAxwAHzP4zyAj6Oex3/zt5zDB9QKEMMLfdsezGZG
TQSsQS0/Tm7LNNEyAakev+fh13aBpA3n2ckCQGjNUzdFWZoreJ9IPXH9C+vv/Zfk
NG/AKFA/8DDdN2dnVD2BOCzgHRQ1Txogec6rhka6fATdsiafkzew8dLMtzkCQB6U
/Mi1EhvinKH9cw678AbzRkBp8pZNSyvaUIhjgdsZp0I0CUF3pOOsMj6nVVRByt1
BMep7B8uYX0H3NVSS+ECQQDaP+8Zn4rEAT2rCoRQ/cfkVn8YGqKlJJfdseekEbB+5
egFcEK+lasdMjNvC9l2Wm+URc4qkjddffrXK/11tSzDD
-----END RSA PRIVATE KEY-----

**Public Key** a genereted string trhough a one way algorithm using the private key as a seed. Usually the algorithm is called Elliptic Curve Digital Signature Algorithm

See axample: https://andersbrownworth.com/blockchain/public-private-keys/keys

The Private key is also used to create a signature attached to the message that can be verified with the public key. In the case of blockchain instead of a message there are transactions.


Private Key ||| > Public Key > Address

**Node** a single instance in a decentralized network.

If one acts malicious (like faking a transaction) all other nodes will ignore that corrupt node.


**Consensus** is the mechanism used to agree on the sate of a blockchain.
Consensus protocol can be split in two main parts:
1 Chain Selection algorithm
2 Sybil resistance (proof of work for bitcoin)

**Sybil Resistance Mechanism** a way to define who is the block author to defend against user creating a large number of pseudo anonymous identities to gain a disproportional advantages influence over the set system.

**Prof of work** (or PoW) a node has to go trough a very difficult computation problem, in simple terms is finding a NONCE (A nonce is an abbreviation for "number only used once") that generates a SHA with the given number of zeros.
Some blockchain make this problem harder or easy in order to change the **block time** is how long it takes to block to publish.

**Chain Selection** bitcoin and ethereum use **Nakamoto Consensus** a combination of prof of work and longest chain role. Whichever node who has the longest chain is going to be the chain that they use.

**Transaction Fee** is the reward given to the node who finds solves riddle. Node are competing against each other to be the first one to solve it so they can get the transaction fee and a block reward.

**Block Rewards** are currency of the same blockchain separated exclusively for the miners to incentivize mining and currency liquidity. So in bitcoin blockchain miner get bitcoin and ETH for Ethereum.

**Prof of Stake** (Pos) the one that uses Eth 2.0 a different mechanism that uses a collateral (stake). Nodes (validators) put up ETH as guarantee that they will act honestly in the network if they misbehave they are gone to be punish by removing their stake. Nodes are randomly chosen to propose the new block and the rest of the nodes will validate if the chosen one has proposed the block honestly.
The fee is paid to validators (not called miners)

Pros: great sybil resistance Mechanism
uses less energy

Cons: slight less decentralized mechanism due to the costs it takes to participate.


## Atacks

**Sybil Attack** a user creates a large amount of pseudo anonymous accounts to influence a network.

**51% attack** because of blockchain agree on the longest blockchain as long as they match 51% of the network. This would mean you could do a fork in the network and alter the values in the blockchain.

Both of these attacks are very difficult to do in proof of work and proof of stake.

## Scalability Problem
The more nodes want to participate in transactions and in validating the more it costs to make a transaction (gas fee rises).

ETH 2 will solve this with Sharding.

**Sharding** is a blockchain of blockchains increases the number of transactions in under layers of the main blockchain.

**Layer 1** Base layer blockchain implementation like Bitcoin Ethereum, Avalanche.

**Layer 2** Any application built on top of a layer 1. Examples: Chain link, Arbitrom and Optimisms.

**Rollups** are like layer 2  sidechains but their security relies on Layer 1, side chains implement their own security features.
https://ethereum.org/en/developers/docs/scaling/layer-2-rollups/

---
## Lesson 1: REMIX IDE & intro to SOLIDITY
>Video minute 1:30:40

The default go to IDE to start programming smart contract.
Is an online code editor for Solidity. Solidity is the name of the language in which the smart contracts are coded in Ethereum Network.

> IDE Integrated Development Environment

### Variables
These are the types of variables you can have in Solidity:

- integers
- booleans
- strings
- unsigned integers
- address
- bytes object 32 bytes

Its declaration would be as follows:

```solidity
pragma solidity ^0.6.6;

### Variables types and declaration

contract myFirstContract {

  unint256 favoritNumber = 5; //unsigned integer
  bool favoriteBool = true;
  string favoriteString = "string";
  int256 favoriteInt = -5;
  address favoriteAdress = 0x75455s5545fb...
  bytes32 favoriteBytes = "cat"
}
```

> "contract" is a reserved keyword in solidity.

Lets create our first contract:

```
pragma solidity ^0.6.0;

contract simpleStorage {

  //this will get initialized to 0
  unit256 public favoriteNumber;

  function store(uint256 _favoriteNumber) public{
    favoriteNumber = _favoriteNumber;
  }

}

```

> "//" is the way of creating comments in solidity

### Visibility
is the scope in which functions can be called or accessed. Is declared after the variable type.

>See more at https://docs.soliditylang.org/en/v0.7.3/contracts.html#visibility-and-getters

If we don't explicitly give a visibility keyword it will automatically will be set to  internal.

**Public** can be called by anybody including variables.

**External** can be only called by other contract.

**Internal** can only be called by other functions inside the contract or his derived contract.

**Private** the most restrictive only visible for the contract they are defined at.

If not set will automatically will be set to **Internal**

### Functions

> Note: "state-changing" functions calls are also called **transactions**.

There are two special keywords that define the type of function in which you don't have to make a transaction: view and pure

**View** keyword means you are reading some state of the blockchain. Public variables also have view function.

**Pure** are those who only do some type of math. Does not change the state of the blockchain



```
pragma solidity ^0.6.0;

contract simpleStorage { //global

  //this will get initialized to 0
  unit256  favoriteNumber;
  bool favoriteBool;

  function store(uint256 _favoriteNumber) public{
    favoriteNumber = _favoriteNumber;
  }

  function retrieve() public view returns(uint256){
    return favoriteNumber
  }

  function addNumber(uint256 _favoriteNumber) public pure returns(uint256){
  return _favoriteNumber + _favoriteNumber;
  }
}

```
### Scope
Global are defined in the outer most layer of the contract.
Function defined variables are only know to that function context.

### Structs

Are ways to define new types in solidity

Example of a struct:
```
pragma solidity ^0.6.0;

contract simpleStorage {

  unit256  favoriteNumber;
  bool favoriteBool;

  struct People {
    uint favoriteNumber;
    string name;
  }

  People[] public people;

  //to initialize inside of contract we would do:
  //People public person = People({favoriteNumber:2, name: "Patric"})

  function store(uint256 _favoriteNumber) public{
    favoriteNumber = _favoriteNumber;
  }

  function retrieve() public view returns(uint256){
    return favoriteNumber
  }

  function addNumber(uint256 _favoriteNumber) public pure returns(uint256){
  return _favoriteNumber + _favoriteNumber;
  }
}

```

### Arrays
A way of storing a list of an object or type, it is initialized with 'name' + square brackets
```
People[] public people;
```

Means an array of people object public visibility called people, in this case is a **Dynamic** array because it can change size.

People[1] public people;  
Would be an array with a maximum of 1 people

We are going to add a new function to our contract to add a new person to our people Array

```
function addPerson(string memory _name, uint256 _favoriteNumber) public {
  people.push(People({favoriteNumber: _favoriteNumber, name: _name}))
}
```
So the finished contract looks like this:
```
pragma solidity ^0.6.0;

contract simpleStorage {

  uint256  favoriteNumber;

  struct People {
    uint favoriteNumber;
    string name;
  }

  People[] public people;

  //to initialize inside of contract we would do:
  //People public person = People({favoriteNumber:2, name: "Patric"})

  function store(uint256 _favoriteNumber) public{
    favoriteNumber = _favoriteNumber;
  }

  function retrieve() public view returns(uint256){
    return favoriteNumber;
  }

  function addNumber(uint256 _favoriteNumber) public pure returns(uint256){
  return _favoriteNumber + _favoriteNumber;
  }


  function addPerson(string memory _name, uint256 _favoriteNumber) public {
    people.push(People(_favoriteNumber, _name));
    }

}

```

### Memory and Storage

In solidity you will often see these keywords on functions, those are ways to store with information.

**Memory** means do not store, only use it this time. After the execution is delete it forever.

**Storage** means that it stored on chain.


A string is actually an object, so we have to decide where we want it to store it. So whenever using a parameter to define a function we need to call string memory.


### Mappings
A data structure like dictionary type, that takes in some type of key a returns data associated with it.


```
mapping(string => uint256) public nameTOFavorteNumber
```

and add the corresponding part to the addPerson function:
```
  nameToFavoriteNumber[_name] = _favoriteNumber;
```

Also we will add License Identifier at the top.

So all the Contract will be:



```
// SPDX-License-Identifier: MIT

pragma solidity ^0.6.0;

contract simpleStorage {

  uint256  favoriteNumber;

  struct People {
    uint favoriteNumber;
    string name;
  }

  People[] public people;
  mapping(string => uint256) public nameToFavoriteNumber;

  //to initialize inside of contract we would do:
  //People public person = People({favoriteNumber:2, name: "Patric"})

  function store(uint256 _favoriteNumber) public{
    favoriteNumber = _favoriteNumber;
  }

  function retrieve() public view returns(uint256){
    return favoriteNumber;
  }

  function addNumber(uint256 _favoriteNumber) public pure returns(uint256){
  return _favoriteNumber + _favoriteNumber;
  }


  function addPerson(string memory _name, uint256 _favoriteNumber) public {
    people.push(People(_favoriteNumber, _name));
    nameToFavoriteNumber[_name] = _favoriteNumber;
    }

}
```

### EVM

Ethereum Virtual Machine is refereed to the overall ecosystem in which all the interactions are done in the Ethereum Network. A lot of Blockchains are **EVM compatible.**

###

## Lesson 2: Factory Pattern
> Video time 2:09:00

The idea of the factory pattern is to have a contract (the factory) that will carry the mission of creating other contracts.

What if I want have a lot of these contract deployed to give people the power to save their favorite number.

Here is where the Factory Pattern comes handy.  **Factory Pattern** is a design pattern that allows a contract to create new contracts.

So lets create our storage factory contract

```
// SPDX-License-Identifier: MIT

pragma solidity ^0.6.0;

import "./SimpleStorage.sol";


contract StorageFactory {
    SimpleStorage[] public simpleStorageArray;

    function createSimpleStorage() public {
        SimpleStorage simpleStorage = new SimpleStorage();
        simpleStorageArray.push(simpleStorage);
    }

    //store factory store
    function sfStore(uint256 _simpleStorageIndex, uint256 _simpleStorageNumber) public {
        SimpleStorage simpleStorage = SimpleStorage(address(simpleStorageArray[_simpleStorageIndex]));
        simpleStorage.store(_simpleStorageNumber);
    }
}

```
Code explanation:

First we import our previous contract to interact with it.

```
import "./SimpleStorage.sol";
```
We need a way to keep track of those contract that we deploy so lets put them in a new list inside our new contract StorageFactory:

```
contract StorageFactory {
    SimpleStorage[] public simpleStorageArray;
    (...)
}
```

If we want our contract to deploy a new contract we need function to do that.

```
function createSimpleStorage() public {
    SimpleStorage simpleStorage = new SimpleStorage();
    simpleStorageArray.push(simpleStorage);
}
```

In the previous lines we create a new variable type of "SimpleStorage"  contract named "simpleStorage" that is equal to an initialize "SimpleStorage()" with no input parameters.

Every time we deploy a new contract we will add it to our newly  created array simpleStorageArray with this previous line of code "simpleStorageArray.push(simpleStorage);"

And with this we successfully deployed a new contract from another contract.

And now in order to interact with our original SimpleStorage contract we created the function "sfStore" and passed two parameters, and index and a number to store.  

Every time you want to interact with a contract we need an **Adress** and a **ABI** (Application Binary Interface).

To return the specific contract in the array we need to call our simple storage with his address like this: SimpleStorage(address("adress_value")), so in our case that will be
```
SimpleStorage(address(0xd840735F4B6a0d1AF8Fa48EcE560f4778c007397));
```

so in our contract this line calls for an index in our array/list and calls for his address and stores it in a variable of type SimpleStorage named simpleStorage (with lower "s")

```
        SimpleStorage simpleStorage = SimpleStorage(address(simpleStorageArray[_simpleStorageIndex]));

```
and then we call the store function with the given number parameter to store.

```
      simpleStorage.store(_simpleStorageNumber);
```

Now our contract is almost complete, we need a way to get our saved number so we add a new function to our StoreFactory contract:

```
 function sfGet(uint256 _simpleStorageIndex) public view returns (uint256){
   SimpleStorage simpleStorage = SimpleStorage(address(simpleStorageArray[_simpleStorageIndex]))
   return simpleStorage.retrieve();
 }
```
So the finall code looks like this:

```
// SPDX-License-Identifier: MIT

pragma solidity ^0.6.0;


contract StorageFactory {
    SimpleStorage[] public simpleStorageArray;

    function createSimpleStorage() public {
        SimpleStorage simpleStorage = new SimpleStorage();
        simpleStorageArray.push(simpleStorage);
    }

    function sfStore(uint256 _simpleStorageIndex, uint256 _simpleStorageNumber) public {
      SimpleStorage simpleStorage = SimpleSrotage(address(simpleStorageArray[_simpleStorageIndex]));
      simpleStorage.store(_simpleStorageNumber)
    }

    function sfGet(uint256 _simpleStorageIndex) public view returns (uint256){
      SimpleStorage simpleStorage = SimpleStorage(address(simpleStorageArray[_simpleStorageIndex]))
      return simpleStorage.retrieve();
    }

```


Finally we could refactor our contract to avoid saving into a variable and do the push to array and store our value like this:

```
// SPDX-License-Identifier: MIT

pragma solidity ^0.6.0;

import "./SimpleStorage.sol";


contract StorageFactory {
    SimpleStorage[] public simpleStorageArray;

    function createSimpleStorage() public {
        SimpleStorage simpleStorage = new SimpleStorage();
        simpleStorageArray.push(simpleStorage);
    }

    function sfStore(uint256 _simpleStorageIndex, uint256 _simpleStorageNumber) public {
      SimpleStorage(address(simpleStorageArray[_simpleStorageIndex])).store(_simpleStorageNumber);
    }

    function sfGet(uint256 _simpleStorageIndex) public view returns (uint256){
      return SimpleStorage(address(simpleStorageArray[_simpleStorageIndex])).retrieve();

    }
}
```

### Inheritace

Since our original contract has many cool features, what if we wanted our StorageFactory to be a simple storage on itself, that is when inheritance becomes handy.

In order to StoreFactory to have all properties and functions we need to created with the "is" key word like this:

```
contract StorageFactory is SimpleStorage {
  //  everything else ...
}
```
https://betterprogramming.pub/learn-solidity-the-factory-pattern-75d11c3e7d29

## Lesson 3: Fund Me
> Video time 2:26:23

Now lets create a function that accepts some type of payment. A new keyword is **payable** which means a function can accept funds.

Every time you call a function  has an associated value to it, you can always append a "value" of the number of wei or gwei or finney or eth will be sent to the function if it is a payable function.

```
// SPDX-License-Identifier: MIT

pragma solidity >=0.6.0 <0.9.0;

contract FundMe{
  function fund() public payable{

  }
}
```
To keep track of who is sending funds to our contract lets create a contract with a mapping of addresses and value like this:

```
// SPDX-License-Identifier: MIT

pragma solidity >=0.6.0 <0.9.0;

contract FundMe{

  mapping(address => uint256) public addressToAmountFunded

  function fund() public payable{
    addressToAmountFunded[msg.sender] += msg.value;
  }
}
```
**msg.sender** and **msg.value** are keyword in every contract and transaction that specify the amount sent and the sender.

But what if we wanted to send funds in USD insetead of ETH??
we would need to know the convertion rate from ETH to USD

How and where are we are getting this data from??

## Decentralized Oracle Network Chainlink

Since blockchain can reach consensus on deterministic matters but can't on non-deterministic we need a way to get some information that is also decentralized as the blockchain.

For example an api call, getting a random number or the price of a certain token or cryptocurrency.

Centralized oracles are single point of failures so we need a decentralized oracles to provide a more robust infrastructure to our contracts.

Data feeds from **ChainLink** can be found at data.chain.link

> data.chain.link

They already are been used by top protocols like AAVE, SushiSwap, Synthetix, Set Protocol.

> https://docs.chain.link/docs/get-the-latest-price/

We can find an example to open in Remix:

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.7;

import "@chainlink/contracts/src/v0.8/interfaces/AggregatorV3Interface.sol";

contract PriceConsumerV3 {

    AggregatorV3Interface internal priceFeed;

    /**
     * Network: Kovan
     * Aggregator: ETH/USD
     * Address: 0x9326BFA02ADD2366b30bacB125260Af641031331
     */
    constructor() {
        priceFeed = AggregatorV3Interface(0x9326BFA02ADD2366b30bacB125260Af641031331);
    }

    /**
     * Returns the latest price
     */
    function getLatestPrice() public view returns (int) {
        (
            /*uint80 roundID*/,
            int price,
            /*uint startedAt*/,
            /*uint timeStamp*/,
            /*uint80 answeredInRound*/
        ) = priceFeed.latestRoundData();
        return price;
    }
}
```

To add price data feed we need to import to our contract:
```
import "@chainlink/contracts/src/v.06/interfaces/AggregatorV3Interface"
```

### Interfaces

> source: https://github.com/smartcontractkit/chainlink/blob/develop/contracts/src/v0.6/interfaces/AggregatorV3Interface.sol

Interfaces don't have full function implementations.
In solidity contracts don't natively understand how to interact with another contract we have to tell solidity what function can be called in another contract and this is where interfaces come into play.

Interfaces compile down to an ABI (Application Binary Interface)

The **ABI** tells solidity and other programming languages how it can interact with another contract.

Anytime you want to interact with an already deployed smart contract you will need an ABI



importing is the same as pasting the whole code so for simplicity we will paste all code so our contract will look like this:

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.6.0;

interface AggregatorV3Interface {

  function decimals()
    external
    view
    returns (
      uint8
    );

  function description()
    external
    view
    returns (
      string memory
    );

  function version()
    external
    view
    returns (
      uint256
    );

  // getRoundData and latestRoundData should both raise "No data present"
  // if they do not have data to report, instead of returning unset values
  // which could be misinterpreted as actual reported values.
  function getRoundData(
    uint80 _roundId
  )
    external
    view
    returns (
      uint80 roundId,
      int256 answer,
      uint256 startedAt,
      uint256 updatedAt,
      uint80 answeredInRound
    );

  function latestRoundData()
    external
    view
    returns (
      uint80 roundId,
      int256 answer,
      uint256 startedAt,
      uint256 updatedAt,
      uint80 answeredInRound
    );

}

contract FundMe{

  mapping(address => uint256) public addressToAmountFunded;

  function fund() public payable{
    addressToAmountFunded[msg.sender] += msg.value;
  }

  function getVersion() public view returns (uint256){
    AggregatorV3Interface priceFeed = AggregatorV3Interface(0x9326BFA02ADD2366b30bacB125260Af641031331);
    return priceFeed.version();
  }

  function getPrice() public view returns(uint256){
    AggregatorV3Interface priceFeed = AggregatorV3Interface(0x9326BFA02ADD2366b30bacB125260Af641031331);
    (uint80 roundId,
      int256 answer,
      uint256 startedAt,
      uint256 updatedAt,
      uint80 answeredInRound)
      = priceFeed.latestRoundData();
      return uint256(answer);
  }

}
```

A **Tuple** is alist of objects of potentially different types whose number is a constant at compile-time.

2:50:00
