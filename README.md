# Poe server bot quick start

This is the companion repository to the Poe server bot
[quick start](https://developer.poe.com/server-bots/quick-start). Please follow that
guide for instructions on how to use this repository.

#AddedFromPage. Saved you a click. - Cybersooulja

In this quick start guide, we will build a bot server in Python and then integrate it with Poe. Once you have created a Poe bot powered by your server, any Poe user can interact with it. The following diagram might be useful in visualizing how your bot server fits into Poe.
For more information on Poe server bots, check out the .
Deploying your bot
We recommend using  to deploy your bot, but you can also use any cloud provider of your choice; all you need to do is to make the bot server available at a publicly available URL and once you have that, you can skip to . In order to use Modal to deploy your bot, do the following.
Step 1: Install the Modal client
Make sure you have Python installed. Open a terminal and run pip install modal-client
You might have to use pip3 instead of pip depending on your version of Python.
Step 2: Setup your Modal token
This step involves setting up access to modal from your terminal. You only need to do this once for your computer. In the terminal, run modal token new --source poe. If you run into a "command not found" error, try .
If that command runs successfully, you will taken to your web browser where you will be asked to log into modal using your Github account.
After you login, click on "create token". You will be prompted to close the browser window after that.
Step 3: Clone the starter code and deploy to Modal
In your terminal, run:
git clone https://github.com/poe-platform/server-bot-quick-start
cd server-bot-quick-start
pip install -r requirements.txt
modal deploy main.py
Modal will now deploy your app and output two urls: a) the endpoint at which your app is hosted b) an internal page where you can monitor your app. You will be using the former to integrate your bot into Poe.
Integrating with Poe
Once you have a bot running under a publicly accessible URL, it is time to connect it to Poe. You can do that on your desktop by going to the bot creation . You can customize how your bot looks by providing a picture, name and description. After you fill out the server URL and click "create bot", your bot should be ready for use on all Poe clients.
Iterating on your bot
For faster iteration on your bot, we recommend using modal serve main.py. On running that command, Modal will deploy an ephemeral version of your app which live updates in response to any code change. In addition, any print/debug statements will output to your terminal.
Feel free to comment/uncomment any of the other example bots in main.py to try them out or build off of them.
Where to go from here
One of the advantages of building a bot on Poe is the ability to invoke other Poe bots. In order to learn how to do that check out: .
Check out other detailed guides that show you how to enable specific features
​​
​​
Refer to the  to understand the full capabilities offered by Poe server bots.
Check out the  library, which you can use as a base for creating Poe bots.
