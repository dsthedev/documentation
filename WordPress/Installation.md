# Installing WordPress

This document will cover getting the latest version of WordPress, installing it locally, and getting the basic configuration done.  By the end of it, there should be a custom WordPress installation setup and ready to use for a new project!

###### Requirements

* LAMP Stack
* Browser

## Install Locally

1. Go to the WordPress downloads page, and download the latest .zip version here
	- Direct download link
2. Unzip and move `wordpress/` to `www/htdocs` folder
	- `F:/ampps/www/project`
3. Create new database & user
	- Recommend using adminer over phpmyadmin
	- Don't use the default `root` or `admin` users!
	- Make sure the user password is strong
4. Run famous 5 min install
	- Create admin user (to be replaced immediately!)
5. Login to new site & verify everything works
	- Check a few admin pages (Settings, permalinks, pages, etc)
	- View home page & nested pages like the sample page
6. Move on to configuring the new site

## WP-CLI

1. Make sure you have php installed and in your path so you can execute it globally.
2. Download [wp-cli.phar](https://raw.github.com/wp-cli/builds/gh-pages/phar/wp-cli.phar) manually and save it to a folder, for example `c:\wp-cli`
3. Create a file named `wp.bat` in `c:\wp-cli\` with the following contents:

```bat
@ECHO OFF
php "c:/wp-cli/wp-cli.phar" %*
```

4. **DO NOT DO THIS!** *It will do weird stuff to path variable.  Add it manually instead!* Add c:\wp-cli to your path:
	5. `setx path "%path%;c:\wp-cli"`

You can now use WP-CLI from anywhere in Windows command line.

## Resources

- [MAMP](https://www.mamp.info/en/downloads/)
- [Adminer](https://www.adminer.org/)
- [Latest Wordpress](https://wordpress.org/download/)
- [Password Generator](https://lastpass.com/generatepassword.php)
