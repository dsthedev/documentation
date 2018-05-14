# Configuring WordPress

If you've never used WordPress before, it's highly recommend that you take some time checking out the `wp-admin` area (15m) to familiarize yourself with the options, layout, etc.

This document will walk through setting up WordPress with some common, sensible options and give a brief description why.

## Settings

Most of these options are set automatically in the installation process.  Below are some that are not:

### General

- **Timezone**: UTC-6 (Obviously set this to your own)
- **Date Format**: Y-m-d (Preference, but it should be set accordingly)

### Reading

- **Front page displays**: Set to static pages for both front and Posts.
	- **Tip**: Go to the Pages screen and make 2 pages first, if they don't exist already:
		- Front Page (*Front page*)
		- Blog (*Posts page*)

### Discussion

- **Other comment settings**: Check "Users must be registered and logged in to comment (Prevent spam & anonymous activity)

### Media

- **Medium size**: 480x480 (300 to 1024 is a big gap, plus 480 shrinks on mobile and stretches on tablets better)

### Permalinks

- **Common**: Custom Structure -> `/%category%/%postname%/` (Simple and intuitive permalink structure)

## Other Options

Aside from setting settings, there are a few other things to check for when configuring a new site:

### Appearance

- **Themes**: Remove all twenty- themes other than the most recent (They are outdated, but you should keep at least one WP theme to fall back on)

### Users

Remove the admin user, and create at least 1 new Administrator user account.  Follow the rules below for best results!

- **Username**: Choose a username that's actually unique, it shouldn't be easily guessed by your name and/or email!
	- Example: Joe Smith | jsmith@gmail.com
		- Bad Usernames: jsmith, joe, sjoe
		- Good Usernames: jdawg, cheesyJ, swordFanJ (Okay, maybe not _good_, but they're _better_)
- **Password**: Make sure it's a very strong password.  (Some may complain, but it's better than getting hacked)
- **Send User Notification?*- Only if you didn't choose the users password (WP set's a fairly strong password by default)
- **Role**: WordPress user roles provide great security and stability if used properly:
	- Administrator: Only have 1 or a few of these accounts (Full access to all settings, can make & break sites)
	- Editor: Recommended for most users affiliated with the business/organization/group that will manage the site's content.
	- Author: For users that should only be able to edit their own posts.
	- Contributor: Users that can write and manage only their own posts, but can't publish them
	- Subscriber: Can only manage their profile


## Resources

- [WP User Roles](https://codex.wordpress.org/Roles_and_Capabilities)