# Sonaric

> After installing the node, our sonaric points will come instantly.

> They said they are still working on an incentive program.

> There is no such thing as our points will be rewards - we are just inside as RC.

> We do not have a server cost, we will use an existing server.

#

# Hardware.

> We need Ubuntu 22 and above.

> I used one of the devices where I installed an active node.

> If you are still going to buy a new server, 2 vCPU and 2 RAM are enough.

#

# Installation

```console
# server update
sudo apt-get update && sudo apt-get upgrade -y

# Let's install nodejs using nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
nvm install 20
nvm use 20
npm install -g npm@latest

# sonaric installation
sh -c "$(curl -fsSL https://raw.githubusercontent.com/monk-io/sonaric-install/main/linux-install-sonaric.sh)"
````

> If we get node information output with the `sonaric node-info` command, it's ok.

![1](https://github.com/user-attachments/assets/1b39381e-b74f-4931-8cdb-c65ce109f456)



#

```console
# update
sudo apt update
sudo apt upgrade sonaric
sonaric node-info
```

```console
# let's edit the end of the command.
ssh -L 127.0.0.1:44003:127.0.0.1:44003 -L 127.0.0.1:44004:127.0.0.1:44004 -L 127.0.0.1:44005:127.0.0.1:44005 -L 127.0.0.1:44006:127.0.0.1:44006 user@your-vps-ip
# If you are using root as user, let's write root.
```

> To understand that the above command works: `curl http://localhost:44004`

![2](https://github.com/user-attachments/assets/81c89d88-d807-418d-9018-22b83e3c2e35)


```console
sonaric identity-export -o node-name.identity
# Let's delete the node-name part and specify a name.
# Let's enter our password.
````

> You can download the backup file on our server with SFTP (File) connection applications or via Termius (Mac - Windows - Phone), Mobaxterm.

If Termius, you entered SFTP - You selected your server, you dragged the xxxx.identy file on your server and copied it to the desired file on your computer - you downloaded it.

![3](https://github.com/user-attachments/assets/230fa6e3-edab-472a-9309-016cc2d8da57)


> For Backup (Pub ID - Priv Key - Key - Key PW while setting up on the site)

We will open a tunnel between the node and our pc.

```console
ssh -L 127.0.0.1:44003:127.0.0.1:44003 -L 127.0.0.1:44004:127.0.0.1:44004 -L 127.0.0.1:44005:127.0.0.1:44005 -L 127.0.0.1:44006:127.0.0.1:44006 user@your-vps-ip
```

User - And set the IP Address according to your server and paste it into CMD and enter your server. The tunnel will be active as long as CMD is open.

From your browser: Go to http://localhost:44004/ - You will see your node's score - ranking.

There will be a settings button in the upper right middle Click - Click the Export Button - Set your password and confirm it will now give you your keys. Save then click the save to json file file and save the json version to your computer.



