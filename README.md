# cakephp2.x_all_green

## Requirement

- [virtualbox](https://www.virtualbox.org/wiki/Downloads)
- [vagrant](https://www.vagrantup.com/downloads.html)

## Installation

$ vagrant up

$ vagrant ssh

$ cd /var/www/

$ composer install

$ cp ./public/Config/core.php.default ./public/Config/core.php

$ cp ./public/Config/core.php.default ./public/Config/database.php

$ vim ./public/Config/database.php

```diff
--- a/public/Config/database.php
+++ b/public/Config/database.php
@@ -55,11 +55,11 @@ class DATABASE_CONFIG {
                'datasource' => 'Database/Mysql',
                'persistent' => false,
                'host' => 'localhost',
-               'login' => 'user',
-               'password' => 'password',
-               'database' => 'database_name',
+               'login' => 'root',
+               'password' => 'root',
+               'database' => 'scotchbox',
                'prefix' => '',
-               //'encoding' => 'utf8',
+               'encoding' => 'utf8',
        );

```
