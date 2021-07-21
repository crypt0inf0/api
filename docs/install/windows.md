# Setup Avalon Node On Windows

Download [git](https://git-scm.com/downloads) and a few other required software's.

#### Required software's
* [MongoDB](https://mongodb.com)
* [NodeJS](https://nodejs.org/en/download/) **v10/12/14** (LTS)

## Install and run Avalon node on Windows
Open `Command Prompt` by  `Windows Key + R` & type `CMD` Run the following command,
```
git clone https://github.com/dtube/avalon.git
cd avalon
```
Let's install nodejs dependencies,
```
npm install
```
Once its complete, Lets install & run our avalon node.
```
setx HTTP_PORT "3001"
setx P2P_PORT "6001"
setx DB_NAME "avalon"
setx DB_URL "mongodb://localhost:27017"
setx PEERS "ws://34.65.228.228:6001,ws://dseed.techcoderx.com:6001"
setx MAX_PEERS "20"
node --stack-size=65500 main
```
By default your node will be observer node.

Check out how to become a leadernode & produce blocks [here](#leader)


To run Avalon node in background, You need to install npm package,
```
npm install forever -g
```
Run Avalon node in backgroung using `forever`
```
forever start node --stack-size=65500 main
```

Peer list:
```
ws://34.65.228.228:6001
ws://dseed.techcoderx.com:6001
```




