# PHP

Eventually I'd like to have custom installation instructions in here.  For now it's just going to be some tips.

## Install XDebug (MAMP + Windows)

1. Download [php_xdebug-2.6.0-7.1-vc14.dll](http://xdebug.org/files/php_xdebug-2.6.0-7.1-vc14.dll)
2. Move the downloaded file to E:\MAMP\bin\php\php7.1.5\ext
3. Edit E:\MAMP\conf\php7.1.5\php.ini and add the line
	4. zend_extension = E:\MAMP\bin\php\php7.1.5\ext\php_xdebug-2.6.0-7.1-vc14.dll
5. Restart the webserver

Optionally, add the following for a custom IP/Port setup:

```ini
[XDebug]
zend_extension = C:\php\ext\php_xdebug-2.6.0-7.1-vc14.dll
xdebug.remote_autostart=1
xdebug.remote_enable=1
xdebug.remote_host=172.16.64.202
xdebug.remote_port=9000
xdebug.remote_handler=dbgp
```

## Add PHP to Windows Path

This needs to be done to use `php` from command prompt and powershell.

1. `Win+PauseBreak`
2. In the Computer window click the System properties button on navigation bar.
3. In the System properties window click the Advanced system settings link.
4. In the Advanced system settings window click the Environment Variables… button.
5. In the Environment Variables window select the path in the user variables section and click the Edit… button.
6. In the Edit User Variable window place your cursor at the end of the contents within the Variable value: input and add the location of PHP to that string. In a typical WAMP installation, PHP is located in C:\wamp\bin\php\php.#.#.# where #.#.# corresponds to the version of PHP that you are running. **Note**: locations are separated by semicolons. So, make sure there is a semicolon before you define the location of PHP in the variable value.
7. After you have entered the location of PHP, click the OK button and restart your command prompt. Congrats, you can now run PHP from the Windows command prompt!
