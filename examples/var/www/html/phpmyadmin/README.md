# phpMyAdmin Installation and Configuration Guide

This guide explains how to download and set up phpMyAdmin in this directory for both Windows and Linux systems. It also includes basic configuration steps for PMO (phpMyAdmin Operations).

---

## 1. Download phpMyAdmin

### Official Website

Visit the official phpMyAdmin website:  
[https://www.phpmyadmin.net/downloads/](https://www.phpmyadmin.net/downloads/)

### For Windows

1. Download the `.zip` archive from the website.
2. Extract the contents of the archive into this folder.
3. Ensure all files are extracted directly into the folder (not in a subfolder).

### For Linux

1. Open a terminal.
2. Navigate to the target directory:
    ```bash
    cd /var/www/html/phpmyadmin
    ```
3. Download the latest phpMyAdmin release (replace the URL with the latest version if needed):
    ```bash
    wget https://www.phpmyadmin.net/downloads/phpMyAdmin-latest-all-languages.tar.gz
    ```
4. Extract the archive:
    ```bash
    tar xvf phpMyAdmin-latest-all-languages.tar.gz --strip-components=1
    ```
5. Remove the archive:
    ```bash
    rm phpMyAdmin-latest-all-languages.tar.gz
    ```

---

## 2. Basic Configuration

### Create Configuration File

1. Copy the sample configuration file:
    ```bash
    cp config.sample.inc.php config.inc.php
    ```
2. Open `config.inc.php` in a text editor.

### Set the Secret Passphrase

Find the following line:
```php
$cfg['blowfish_secret'] = '';
```
Replace it with a random string (at least 32 characters):
```php
$cfg['blowfish_secret'] = 'your_random_secret_passphrase_here';
```
> **Tip:**  
> You can generate a secure Blowfish secret using an online generator such as:  
> [https://phpsolved.com/phpmyadmin-blowfish-secret-generator/](https://phpsolved.com/phpmyadmin-blowfish-secret-generator/)  
>  
> Alternatively, on Linux, you can generate one via terminal:  
> ```bash
> openssl rand -base64 32
> ```

### Configure PMO (phpMyAdmin Operations)

- By default, phpMyAdmin works out-of-the-box for basic operations.
- For advanced features (bookmarks, relations, etc.), create the phpMyAdmin configuration storage database:
  1. Log in to phpMyAdmin.
  2. Select your database server.
  3. Go to the "Import" tab.
  4. Import the `sql/create_tables.sql` file found in the phpMyAdmin directory.
  5. Update `config.inc.php` with the database credentials for the configuration storage.

Example:
```php
$cfg['Servers'][$i]['controluser'] = 'pma';
$cfg['Servers'][$i]['controlpass'] = 'your_pma_password';
```

---

## 3. Access phpMyAdmin

- Open your browser and go to:  
  `http://localhost/phpmyadmin/`  
  or the appropriate URL for your server.

---

## 4. Security Recommendations

- Do **not** leave the `config.inc.php` file world-writable.
- Consider restricting access to phpMyAdmin using web server configuration or `.htaccess`.

---

For more details, refer to the [official documentation](https://docs.phpmyadmin.net/).