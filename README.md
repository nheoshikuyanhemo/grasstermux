# GrasTermux

register Grass https://app.getgrass.io/register/?referralCode=zaS_ajz8z7OExq-
#
original source from  https://github.com/ymmmmmmmm
#
Grass connection in mises browser to termux 
#
Below I will tell you step by step in details how to run your GetGrass extension on Termux.
#
Disclaimer ON! ⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️

If you do anything to your GetGrass account, you do it at your own risk! 

## command:

1. update and upgrade repository termux

       pkg update && pkg upgrade 

2. required install:

       pkg install python
   #
       pip install loguru
   #
       pip install websockets
   #
       pkg install git
   #
       pkg install openssh

4. Login SSH
create ssh password:

       passwd

##### clone bot folder from github: 

    git clone https://github.com/nheoshikuyanhemo/grasstermux.git

    cd grasstermux

run SSH:

    sshd

check your device userID:

    whoami

Check your IP, select (UP, RUNNING):

    ifconfig

run your ssh
(ssh YourUserID@YourIP -p port)
###### example: 

    ssh u0_a308@102.168.1.8 -p 8022

then submit your password to agree to login to SSH , you will automatically return to the initial folder, then go to the getgrass_bot folder:

    cd grasstermux

4. Get user id

//go to your getgrass dashboard on mises browser,

//launch Devtool,

//refresh dashboard getgrass,

//open Devtool page,

//open page network, Search for "user" in devtools search.

//click {!}RetrieveUser

//Go to response tab.

//copy user id

# back to termux 
edit file no_proxy.py:

    nano no_proxy.py

##### Look for the line that contains:
#
async def main():

 #TODO Modify user_id
 
  _user_id = ''
  
  await connect_to_wss(_user_id)
    
#
fill in the _user_d = 'with your userid'

Save 

Click the CTRL button, then X, then Y, then Enter. 
#
5. run python

       python no_proxy.py
