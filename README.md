# Boilerplate Craft
You will discover my recipe for finding out of Craft CMS as BackEnd part couple to VueJS.  
**DISCLAMER: This repository is for my personal testing...** _Don't judge me and don't throw me some rocks_

## The objectives
- Create a back office with **Craft CMS**
- Use **GraphQL** with **VueJS 3**
- Create a mini application and boilerplate
- Enjoy & learn

## Install Craft
Before all, you have to download Craft on the official Website.
- Start `docker-compose up -d`
- Enter in your docker container *PHP* `docker-compose exec php bash`
- Tap `php composer.phar create craftcms/craft myproject`
- Wait some minutes _(it depends of your connexion)_
- Put the content from `myproject` in `craft/` folder in root.
- Follow the guide for installation in your command line
```
Are you ready to begin the setup? (yes|no) [no]:y
Generating an application ID ... done (CraftCMS--d3b2b0fa-176b-4763-9756-1ab39ec987c2)

Which database driver are you using? [mysql,pgsql,?]: mysql
Database server name or IP address: [127.0.0.1] localhost
Database port: [3306] 3306
Database username: [root] anonymous
Database password: helloworld
Database name: alpha
Database table prefix: vue
```
**Don't worries, all these informations can be modified after the installation, you can find them in `.env` file**  
_Probably, you have to enter your infos for creating the admin user, let us guide you..._

 ## Configuration 

 ### Install your craft instance
 Visit the install link in this address [install link](http://localhost/index.php?p=admin/install).  
 You have to follow the instructions and adding the informations relative to your `docker-compose.yml` file.

 ### Modifing our config
 At any time, you can change your configuration in `.env` file.
 ```bash
SECURITY_KEY=L5G-bu7INd0Pd8pdbbFI09iJpWSVWQ5y
DB_DRIVER=mysql
DB_SERVER=mysql
DB_PORT=3306
DB_DATABASE=alpha
DB_USER=anonymous
DB_PASSWORD=helloworld
DB_SCHEMA=
DB_TABLE_PREFIX=vue_
```

Sometime you can have some issues with your admin... You have to change the configuration for giving the access to the Admin.
You have to change the configuration in `craft/config/general.php`. 

```php
// craft/config/general.php
[...]
'allowAdminChanges' => true,
[...]
```

--- 
**Made with <3 with the best the recipe**
