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

## Resources

- [MAMP](https://www.mamp.info/en/downloads/)
- [Adminer](https://www.adminer.org/)
- [Latest Wordpress](https://wordpress.org/download/)
- [Password Generator](https://lastpass.com/generatepassword.php)
