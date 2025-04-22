# irc-hosting-tor
This repo showcases how to deploy and configure an IRC server on the deep web

## Update the instance

    sudo su
    apt update
    apt full-upgrade -y
    apt autoremove -y

## Install inspircd tor irssi

  - ![image](https://github.com/user-attachments/assets/3dfe2604-1888-4aec-82f7-81f2420760c7)

## Configuration

- Backup the config file.
  
      cp /etc/inspircd/inspircd.conf /etc/inspircd/inspircd.conf.bak

- check the docs -> https://docs.inspircd.org/4/configuration/
- the most important tag at the moment is <oper> tag as it has the Server Admin password
- There are other tags as well to consider.
    - <admin>
    - <bind>
    - <server>
    - <files>

## Starting the service

- start the service

        systemctl start inspircd

    - ![image](https://github.com/user-attachments/assets/12de861e-5280-441a-b61f-a7a2706f17bd)
 
## Connecting locally

- use irssi client to connect to the IRC server.
  
- ![image](https://github.com/user-attachments/assets/31cda724-0015-49e3-ad90-0c43add75dee)

- The connection was successful

# Connecting to TOR

- next step is connecting our IRC server to TOR network





