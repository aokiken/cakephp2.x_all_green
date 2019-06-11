# cakephp2.x_all_green

## Requirement

- [virtualbox](https://www.virtualbox.org/wiki/Downloads)
- [vagrant](https://www.vagrantup.com/downloads.html)

## Installation

$ vagrant up

$ vagrant ssh -- cd /var/www/ && composer install

$ cp ./public/Config/core.php.default ./public/Config/core.php

$ vim ./public/Config/core.php

```diff
--- a/public/Config/core.php
+++ b/public/Config/core.php
@@ -233,12 +233,12 @@q
 /**
  * A random string used in security hashing methods.
  */
-       Configure::write('Security.salt', 'DYhG93b0qyJfIxfs2guVoUubWwvniR2G0FgaC9mi');
+       Configure::write('Security.salt', OTHER_RANDOM_STRING);
 
 /**
  * A random numeric string (digits only) used to encrypt/decrypt strings.
  */
-       Configure::write('Security.cipherSeed', '76859309657453542496749683645');
+       Configure::write('Security.cipherSeed', OTHER_RANDOM_NUMERIC_STRING);
```

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
