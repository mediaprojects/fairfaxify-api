Fairfaxify API
=============

#### What is this?

This is a simple API built in Kohana by Tim Sheehan to serve JSONP data to Fairfaxify Mobile. Kohana is a PHP framework and requires PHP5.x to run, data is stored using MySQL.

#### Installation

Installation is simple and only requires modification of two base paths and database configuration. Once installed both API methods can be called from the following url's:

 - `yourhost.com/[base_url]/rest/articles`
 - `yourhost.com/[base_url]/rest/article/[article_id]`
 
###### Paths

*.htaccess*

 - `Line 5:` Change RewriteBase (if required) e.g. RewriteBase /fairfaxify/

*application/bootstrap.php*

 - `Line 83:` Change base_url (if required) e.g. 'base_url'   => '/fairfaxify/'

###### MySQL

Import fairfaxify.sql into the target database.

*application/config/database.php*

 - `Line 21:` Change hostname e.g. 'hostname'   => 'yourhost',
 - `Line 22:` Change database name e.g. 'database'   => 'user_database',
 - `Line 23:` Change user name e.g. 'username'   => 'root',
 - `Line 24:` Change password e.g. 'password'   => 'abc123',
 
###### Security

If used in a production environment it is recommended that the application, modules and system folder be moved below web root and their respective paths changed in index.php.