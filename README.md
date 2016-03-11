# mampswitch
Simple PHP script for switching PHP CLI version when using MAMP on a mac.

**Usage**
Make sure you add your local bin to your global PATH. (Put it before $PATH so the system wide php bin won't be used)

Edit ~/.bash_profile and add

    export PATH=/Users/lovelockj/bin/php/bin:$PATH

Also make sure mampswitch is executable.

    chmod +x mampswitch

Edit the source and set your USER_BIN folder path

   	define('USER_BIN', '<<<PATH TO YOU PERSONAL BIN FOLDER>>>');
    
