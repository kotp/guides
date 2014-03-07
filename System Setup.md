## System Setup
Basic instructions on setting up a Ubuntu machine and bringing it up.

### Bare Essentials


**step 1:** Insert Boot disk(cd/flash drive)       
**step 2:** Restart your system       
**step 3:** while restarting system select boot menu(f2/delete)       
**step 4:** In Boot menu select Boot disk(cd/flash drive)      
**step 5:** Select “Restore entire Hard disk” option and click on continue          
**step 6:** After restarted choose your Language(English) and click on continue        
**step 7:** Accept Licence agreement and click on continue      
**step 8:** Select Time Zone and click on continue      
**step 9:** Select keyboard (English US) click on continue   
**step 10:** Enter following information 
                          
> your Name              : The Egghead Creative   
computer’s name	        : anyname                                 
User name		: ehc                                        
password		:                            
Confirm password	: 
                                  
and click on continue.

step 11: Enter your password                                            
step 12: select “close window and set up later” button

Now your system is ready to use.

step 13: Open terminal and enter following commands
		sudo apt-get update.
		sudo apt-get upgrade

### Boostrap
**step 1:**  Go to https://github.com/ehc/dotfiles/blob/master/support/system-setup and select Raw tab and copy whole content and past it in local directory file with any name with .sh extension(Ex. setup.sh).OR 
Go to terminal and execute following commands.

i) install curl(sudo apt-get install curl)    
ii) curl -S https://github.com/ehc/dotfiles/blob/master/support/system-setup > setup.sh                
iii) chmod +x setup.sh


**step 2:** Right click on this file and select properties and give execution permission.   
**step 3:** Open Terminal and go to the path where setup.sh file exist   
**step 4:** Run following command. 
  
		./setup.sh 
   
**step 5:** Enter your system’s password

It will take some time to install all required packages………………………  
While or After setting our setup file it will ask for sql password And the password is : “password”.

### Chromium
Goto ->firefox->history->sign in as -> 	username: node@eggheadcreative.com 
 	password: tehc4eva

### SSH Keys

**Copying ssh keys:**
When you copying keys it doesn’t let you do it success ambiguity problem rises: for that 
Goto: http://dtek.net/blog/how-stop-gnome-keyring-clobbering-opensshs-ssh-agent-ubuntu-1204
And copy run **vi /etc/xdg/autostart/gnome-keyring-ssh.desktop**
And Type **sudo !!**  then modify the content  NoDisplay  = change true to false 
Press esc +:wq
Now Goto->settings->startupapplication->sshkey->then remove ssh keys.
Now copy the ssh keys 
scp -r ehc@ipaddress:~/.ssh/ehc*  ~/.ssh/
For checking it just do run :   ssh-add-L 
If not listed out just do :	sarst (It will drop all the keys if existed ).  And again  go the  checking command.

### Shortcuts

Shortcut keys Setting:

**step 1:** press super/window key   
**step 2:** Change lock screen key: Select settings->Keyboard-> shortcut -> system in left side list and change screen Lock shortcut a super+L.

Hide Launcher tab
 
Select settings->Apperance->”ON”(so that Left side bar will not be standby mode).



**Compiz Config** 
Shortcuts for advanced window manager able to set our terminal settings.

Goto->Compiz Config(In case if not available Goto software updater->search for compiz config if not installed install it if not installed runcommand through terminal : 

   **>sudo apt-get install compiz** 

compizconfig-settings-manager 
Then press super/window key and search for 
 compizconfig->Window manager->Grid->Bindings->  And make change for put Left,Put Right and Maximize
Put left: Double click on the <Control><Primary><Alt><Super>Left ->then click on grabkey combination-> and do ctrl+window+alt+leftarrow and the click ok.

Put Right: Double click on the <Control><Primary><Alt><Super>Right ->then click on grabkey combination-> and do ctrl+window+alt+RightArrow and the click ok

Maximize: Double click on the Disabled->then click on grabkey combination-> and do super/window+enter and the click ok.

