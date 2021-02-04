# Blockchain_week_18
This weeks homework, we are creating a test network through blockchain for ZBank. As a class we will all submit our custom testnet blockchain, send a test transaction, create a reporitory and write instructions on how to use the chain for the rest of your team. 

1. To start this assignment off I installed the mac verison of Go Ethereum tools. Once this was complete I changed the name and saved the folder under my documents file. Below is a screenshot of my geth folder. I know the files are not in alphabetical order, I apologize in advance. 
<img width="563" alt="Screen Shot 2021-02-03 at 5 42 46 PM" src="https://user-images.githubusercontent.com/70147930/106819953-8f224b80-6648-11eb-9dbc-a63ca3d41346.png">

2. After creating the folder for your geth, go to your terminal and open the geth folder. Once you are in the correct folder in your terminal type "./geth --datadir node1 account new". Hit enter. Once this is complete you will be instructed to create a password. Once your password is complete you will receive a public address to the key and a path of the secret key file.  Now repeat this step but instead type "./geth --datadir node2 account new" to create your second node and be sure to write down the public address to the key as well as your path of the secret key file. I will not be adding a screenshot of this because my private key is displayed.

3. Now that we have successful created both test accounts and taken notes on our public access to the key as well as our path of the secret key, we are ready to setup our genesis block. The genesis block will allow us to run our network. Please insert the command "./puppeth" into your terminal. After you have inserted this command press enter. Now you will choose the Clique Proof of Authority by selecting the following steps. "Configure New Genesis" or 2, press enter, "Create New Genesis From Scratch" or 1, press enter, "Clique-Proof-Of-Authority" or 2, press enter. 
<img width="647" alt="Screen Shot 2021-02-03 at 10 16 27 PM" src="https://user-images.githubusercontent.com/70147930/106840140-8abc5980-666d-11eb-8e20-7e1419256be6.png">

4. Wahoo! You're doing great! Now that you have choosen a Clique Proof of Authority you will need to designate an amount of time for the blocks. The question will appear as "How many seconds should blocks take?". The default for this question is 15 seconds and can remain at 15 seconds. Remember those public keys I told you to write down? They are about to come in handy! After selecting 15 seconds for the time for the blocks you will be prompted to list the public keys. Notice how your public key and the command already has "0x" listed. TAKE NOTE - these do not need to be listed twice, please either remove the 0x from your public or the command line. When prompted to pre-fund the pre-compiled accounts please say no. See below for details. 
<img width="627" alt="Screen Shot 2021-02-03 at 10 24 26 PM" src="https://user-images.githubusercontent.com/70147930/106840674-a1af7b80-666e-11eb-82f9-27d3c926c1e6.png">

5. Great job! Now there is a written in question for you to create a chain or network ID. Please be sure to remember this combination. I am doing 1998 because that was the year I was born. You will be directed to answer two more questions and answer them as follows: "Manage Existing Genesis" or 2, press enter, "Export Genesis Configuration" or 2, press enter, press enter once more to save genesis to the current directory. Be sure to remember your network name! Mine is puppernet2.json 
<img width="653" alt="Screen Shot 2021-02-03 at 10 28 43 PM" src="https://user-images.githubusercontent.com/70147930/106840996-3a45fb80-666f-11eb-8057-9d574a13c643.png">

Now we get to the good stuff! We are now going to link the nodes to the new network (remember when I told you to remember your network name). My code will look as follows: ./geth --datadir node1 init puppernet2.json and ./geth --datadir node2 init puppernet2.json. I used both commands in separate tabs in the terminal and ran into no trouble. My page is very long for both of these and will not be adding a screenshot.

Here we goooo!! Time to start mining some blocks through the nodes you just created! For node1, run the command "./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --minerthreads 1 --rpc --allow-insecure-unlock". For SEALER_ONE_ADDRESS put your 1st public key minus the 0x. 





