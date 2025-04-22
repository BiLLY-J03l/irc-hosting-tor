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
- edit /etc/tor/torrc config file.
- we're looking to configure hidden services

- ![image](https://github.com/user-attachments/assets/eb7181be-a753-4eef-b035-0fc2b35a4b2a)

- ![image](https://github.com/user-attachments/assets/f360e9d1-4ac0-4cb6-a7d8-f12c2193426c)

- save and exit
  
- connect to tor
- ![image](https://github.com/user-attachments/assets/9231d63a-8fe6-40c3-acdf-ff25730108c1)
- connection successful

- below, we find the hostname of our hidden service public on TOR.
- ![image](https://github.com/user-attachments/assets/a2e783d4-8afd-4971-aa82-82abb78f5b5c)
- lgqucfiywr5kcroqm7ja2xnqykv455wderyhpmg3grryj2xr7xfszwid.onion

- I laucnhed an EC2 instance and configured TOR and install proxychain4 and then I used proxychain4 to start IRSSI and connect to the IRC server on TOR
- ![image](https://github.com/user-attachments/assets/b02cf108-659c-44ce-b3e4-156285cdbc98)
- ![image](https://github.com/user-attachments/assets/2251c415-2a11-4f85-9bb3-4233d8350f34)

- I launched another instance and did the same.

- Then I joined to TEST_CHANNEL to start chatting

        /join TEST_CHANNEL

- and here are JOHN_DOE and THATCHER are having a very innocent chat on the deep web.
- ![image](https://github.com/user-attachments/assets/2afdca9f-c536-4c6a-8721-19525162bd10)
- ![image](https://github.com/user-attachments/assets/d7443b2c-1789-4f01-b3fa-db342ecf5f0b)





