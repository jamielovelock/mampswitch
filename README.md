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
    
Add mampswitch to your bin folder

    ln -s /path/to/mampswitch/mampswitch /path/to/your/bin/mampswitch

Then run it on the command line:

    mampswitch -h
    mampswitch - used to switch cli version of PHP (from MAMP)
    Usage: mampswitch [options] <version>
    -h, --help		Show this message
    -v, --version		Show current version
    -l, --list		List installed versions

    lovelockj@tjmac94:~/bin$ php -v
    PHP 5.3.29 (cli) (built: Jul  6 2015 14:19:43)
    Copyright (c) 1997-2014 The PHP Group
    Zend Engine v2.3.0, Copyright (c) 1998-2014 Zend Technologies
    
    lovelockj@tjmac94:~/bin$ mampswitch -l
    php5.1.6
    php5.2.17
    php5.3.29
    php5.4.42
    php5.5.26
    php5.6.10
    php7.0.0
    
    lovelockj@tjmac94:~/bin$ mampswitch php5.3.29
    Unlinking /Users/lovelockj/bin/phpLinking php5.3.29
    PHP CLI updated to php5.3.29
    
    lovelockj@tjmac94:~/bin$ php -v
    PHP 5.3.29 (cli) (built: Jul  6 2015 14:19:43)
    Copyright (c) 1997-2014 The PHP Group
    Zend Engine v2.3.0, Copyright (c) 1998-2014 Zend Technologies
    
    lovelockj@tjmac94:~/bin$ mampswitch php7.0.0
    Unlinking /Users/lovelockj/bin/phpLinking php7.0.0
    PHP CLI updated to php7.0.0
    
    lovelockj@tjmac94:~/bin$ php -v
    PHP 7.0.0 (cli) (built: Dec  8 2015 16:39:19) ( NTS )
    Copyright (c) 1997-2015 The PHP Group
    Zend Engine v3.0.0, Copyright (c) 1998-2015 Zend Technologies
