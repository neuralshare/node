# node

the node is a simple program that listens to the transactions on account `GAU3XW7Z5OYR7BFANSB7HGVGJRZJ5NSJ3ERWJ5HRVZRCHFSRTQ32YPEM` and sends the corresponding GPT-3 response to the sender account.
The first time you start node, a configuration file called "config.json" will automatically be created in the same folder. Before restarting the node again, now that your configuration file exists, you will need to put your openai api key inside the file, inside "openai_apikey". Then simply replace `"openai_apikey":null` with `"openai_apikey":"sk-xxxx"` . Then you can start the node which will send the response as soon as it sees a new transaction. Before sending it, it will make sure that it has not already been sent by another node.
In the configuration file you will also see a Stellar secret key which is automatically created together with the file. The account connected to it is already funded by FriendBot on FUTURENET and it is the account that will send the responses. If you wish, you can modify that secret key bearing in mind that for correct functioning the account should have XLMs available to be able to carry out transactions on Futurenet. however, it is advisable not to modify it and leave what you find.

## Install and run

 To install the node, create a new Python virtual environment, then install the node with pip: `pip install neuralshare-node`
 Them, to run the node simply execute: `python3 -m neuralshare-node.node`


