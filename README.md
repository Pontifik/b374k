# b374k shell 3.2
This PHP Shell is a useful tool for system or web administrator to do remote management without using cpanel, connecting using ssh, ftp etc. All actions take place within a web browser

##Features : 
* File manager (view, edit, rename, delete, upload, download, archiver, etc)
* Search file, file content, folder (also using regex)
* Command execution
* Script execution (php, perl, python, ruby, java, node.js, c)
* Give you shell via bind/reverse shell connect
* Simple packet crafter
* Connect to DBMS (mysql, mssql, oracle, sqlite, postgresql, and many more using ODBC or PDO)
* SQL Explorer
* Process list/Task manager
* Send mail with attachment (you can attach local file on server)
* String conversion
* All of that only in 1 file, no installation needed
* Support PHP > 4.3.3 and PHP 5

## Requirements :
* PHP version > 4.3.3 and PHP 5
* As it using zepto.js v1.1.2, you need modern browser to use b374k shell. See browser support on zepto.js website http://zeptojs.com/
* Responsibility of what you do with this shell

## Installation :
Download b374k.php (default password : b374k), edit and change password and upload b374k.php to your server, password is in sha1(md5()) format. Or reate your own b374k.php, explained below:
  
  git clone https://github.com/phith0n/b374k.git
  cd b374k
  php -f index.php -- --help

## Customize :
After finished doing editing with files, upload index.php, base, module, theme and all files inside it to a server
Using Web Browser :

Open index.php in your browser, quick run will only run the shell. Use packer to pack all files into single PHP file. Set all the options available and the output file will be in the same directory as index.php
Using Console :

-o filename save as filename
-p password protect with password
-t theme theme to use
-m modules modules to pack separated by comma
-s strip comments and whitespaces
-b encode with base64
-z [no|gzdeflate|gzencode|gzcompress] compression (use only with b)
-c [0 9] level of compression
-l list available modules
-k list available themes

example :

$ php -f index.php o myShell.php p myPassword s b z gzcompress c 9

Don't forget to delete index.php, base, module, theme and all files inside it after you finished. Because it is not protected with password so it can be a security threat to your server

## Upgrade
20160216 / Convert SQL to Base64 to Bypass WAF / @phith0n
20160216 / Ajax encrypt(RC4) channel / @phith0n
