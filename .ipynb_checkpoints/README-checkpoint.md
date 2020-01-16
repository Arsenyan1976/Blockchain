# Blockchain

## Proof of Work Development Chain

In this activity, I will create my `Genesis` block using `Puppeth` tool bundled with the `Go Ethereum`.
The genesis block is the first step towards creating oa new blockchain!

### Creating Genesis

* In GitBash we call `./puppeth.exe` command
* after that we select network name (in our case it will be `armen2012`)
* then we select `configure new genesis` (option 2)

![1](Images/1.png)

* for the question What would you like to do? We select option 1, `create new genesis from scratch`
* Then we slect the comsensus: `Etash - Proof-of-Work`
* In next step we import couple of accounts from `MyCrypto` wallet.
* following question is by defalt `yes`
* then we specify our chain ID: `1976`

![2](Images/2.png)
 
* for the next step we export genesis configurations by selecting 2. This will create 4 `.json` files.
 
### Creating Noes 

![3](Images/3.png)

* Then we exit `puppeth` by using the `Ctrl+C` keys combination.
* with the help of `geth` command we Create the first node's data directory 

![4](Images/4.png)
* then with the smae command we create the second node 

![5](Images/5.png)

* we initialize and tell the nodes to use your genesis block by this command : `./geth init armen2012.json --datadir node1` and `./geth init armen2012.json --datadir node2`

![6](Images/6.png)

### Starting a Chain

* Now it is time to start our blockchain network
* `Node1` will be full mining node initiated by following command: `./geth --datadir node1 --mine --minerthreads 1`  

![7](Images/7.png)

* `Node2` will be a full node that exposes an RPC port, allowing  to talk to it with other apps like MyCrypto. 
* In order to launch `node2` we need to copy the enode address from `node1` and incorporate into the command line ov `node2` as follows:
>`./geth --datadir node2 --port 30304 --rpc --bootnodes "enode://d5321f6146a4273b7ed2b3382e2aa74e304d5f4750e76f15533dc3f652a3404181b10713bb7ecfc6741b55aef06d2683bf0cf7f99c0afba57a189869056a34a0@127.0.0.1:30303" --ipcdisable`


![8](Images/8.png)

### Processing thansaction using MyCrypto wallet

* We open MyCrypto app and navigate into `change Network`

![9](Images/9.png)

* at `Change Network` we select `Kovan` and select `Mnemonic Phrase`

![10](Images/10.png)

* After inserting `Mneomonic Phrase` we unlock the accounts and we can find the accounts that we had already registered during Genesis creation. 
![11](Images/11.png)

* Here we select first account and hit `Unlock`

![12](Images/12.png)

* In this step we select from dropdown menue `View Wallet info` and we copy the `Private key` 

![13](Images/13.png)

* in next step we set up custom node.

![14](Images/14.png)

* We Register Node name, Network name and Node ID and of caurs the URL address.

![15](Images/15.png)

* After that we select `Private Key`

![16](Images/16.png)

* with the help of previously copied `Private key` we unlock the wallet

![17](Images/17.png)

* from drop down menue we select `Sent Ether and tokens`

![18](Images/18.png)

* Then we copy the address and past under recepient address window, choose tha amount to send and hit the `send`.

![19](Images/19.png)

*After that we confirm the transaction and send

![20](Images/20.png)

* we receive the confirmation that the stransaction was `successful`

![21](Images/21.png)



# P.S.

> I Initially started the process for `Proof-of-Authority` . However I was having all the time error message and was not able to connect 2 nodes to work together.  After receiving approval from instructional team I started to do Proof-of-Work developement



![Problem](Images/Problem.png)