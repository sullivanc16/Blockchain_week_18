# Blockchain_week_18
This weeks homework, we are creating a test network through blockchain for ZBank. As a class we will all submit our custom testnet blockchain, send a test transaction, create a reporitory and write instructions on how to use the chain for the rest of your team. 

1. To start this assignment off I installed the mac verison of Go Ethereum tools. Once this was complete I changed the name and saved the folder under my documents file. Below is a screenshot of my geth folder. I know the files are not in alphabetical order, I apologize in advance. 
<img width="563" alt="Screen Shot 2021-02-03 at 5 42 46 PM" src="https://user-images.githubusercontent.com/70147930/106819953-8f224b80-6648-11eb-9dbc-a63ca3d41346.png">

2. After creating the folder for your geth, go to your terminal and open the geth folder. Once you are in the correct folder in your terminal type "./geth --datadir node1 account new". Hit enter. Once this is complete you will be instructed to create a password. Once your password is complete you will receive a public address to the key and a path of the secret key file.  Now repeat this step but instead type "./geth --datadir node2 account new" to create your second node and be sure to write down the public address to the key as well as your path of the secret key file. I will not be adding a screenshot of this because my private key is displayed.

3. Now that we have successful created both test accounts and taken notes on our public access to the key as well as our path of the secret key, we are ready to setup our genesis block. The genesis block will allow us to run our network. Please insert the command "./puppeth" into your terminal. After you have inserted this command press enter. Now you will choose the Clique Proof of Authority by selecting the following steps. "Configure New Genesis" or 2, press enter, "Create New Genesis From Scratch" or 1, press enter, "Clique-Proof-Of-Authority" or 2, press enter. 
<img width="647" alt="Screen Shot 2021-02-03 at 10 16 27 PM" src="https://user-images.githubusercontent.com/70147930/106840140-8abc5980-666d-11eb-8e20-7e1419256be6.png">

