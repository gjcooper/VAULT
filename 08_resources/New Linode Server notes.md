# Notes related to my new linode server

Defaulting to mariadb native commands etc.

_Notes from the mariadb docs:_
### DEFAULT MARIADB SERVER SETTINGS ARE SECURE

For reference, these are the default users, grants and databases in a fresh
MariaDB installation:

```sql
SELECT User,Host FROM mysql.user;
+-------------+-----------+
| User        | Host      |
+-------------+-----------+
| mariadb.sys | localhost |
| mysql       | localhost |
| root        | localhost |
+-------------+-----------+

SHOW GRANTS FOR 'mariadb.sys'@'localhost';
+-------------------------------------------------------------------+
| Grants for mariadb.sys@localhost                                   |
+-------------------------------------------------------------------+
| GRANT USAGE ON *.* TO `mariadb.sys`@`localhost`                    |
| GRANT SELECT, DELETE ON `mysql`.`global_priv` TO                   |
|         mariadb.sys`@`localhost`                                   |
+-------------------------------------------------------------------+

-- Other tables of granted priviledges on mariadb omitted - see docs

SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
```
These are secure. All users are bound to localhost only. The `root` user is used by the Linux root user (or somebody running `sudo`) accessing MariaDB. The user `mysql` is used by some system automation scripts that don't need full database root access. The user `mariadb.sys` cannot be used to login at all, and exists only as an internal construct for system table access.

There is absolutely no need to run the script `mariadb-secure-installation` or (`mysql_secure_installation`) after installing MariaDB with `apt install mariadb-server`. The script is useless, and very misleading with reporting "Success!" after every step even if it did nothing.

The script claims to activate unix socket authentication for root, but Debian/Ubuntu has already been using it by default for over a decade. The script also claims to remove remote access for the root user, but the default root user is already bound to localhost only by default. Additionally the script claims to drop anonymous users and remove test databases, but there are none. The script itself hasn't really been maintained for over a decade, and it is best to not trust it in any way.
### CREATING DATABASES AND USERS FOR APPS

On Debian/MariaDB running `apt install mariadb-server` will set up a sane and secure MariaDB server by default. The commands `mariadb-install-db` and `mariadb-upgrade` run automatically when needed.

The primary tasks for the administrator is to create new users and databases, and add custom settings in `/etc/mysql/mariadb.conf.d/`.

To add a custom database for an app, and create a custom password-authenticated user that has full access to that database over the network, run the following commands using the `mariadb` client (e.g., via `sudo mariadb`):

```sql
-- Create the database
CREATE DATABASE app_db;

-- Create the user 'app_user' with a secure password, allowing connections from any IP address
CREATE USER 'app_user'@'%' IDENTIFIED BY 'your_secure_password';

-- Grant full privileges to the 'app_user' user on the 'app_db' database
GRANT ALL PRIVILEGES ON app_db.* TO 'app_user'@'%';

-- Reload the privilege tables to apply changes
FLUSH PRIVILEGES;
```

Remember to replace 'your_secure_password' with a strong, unique password. Using '%' for the host allows connections from any IP address, which is less secure than restricting connections to a specific IP address or subnet if possible.