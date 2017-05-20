# Lubuntu Setup

After installation, do the following:

## Applications

Install a few useful apps

### Opera Browser

```
sudo add-apt-repository "deb http://deb.opera.com/opera/ stable non-free"
wget -O - http://deb.opera.com/archive.key | sudo apt-key add -
sudo apt-get update
sudo apt-get install opera-stable -y
```
### Typora (Notes | Markdown)

```
# optional, but recommended
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE
# add Typora's repository
sudo add-apt-repository 'deb https://typora.io ./linux/'
sudo apt-get update
# install typora
sudo apt-get install typora
```
* Theme > Night

### Sublime Text 3

```
~$ sudo dpkg -i ~/Resources/Applications/sublime-text_build-3126_amd64.deb;sudo apt-get install -f
```



## Resources

Unpack Resources:

1. Fonts: `~$ unzip -n '~/Resources/Fonts/*.zip' -d ~/.local/share/fonts;fc-cache -fv`
2. Theme: `~$ sudo unzip -n ~/Resources/Themes/*.zip -d /usr/share/themes/`
3. ​

## Appearance

1. Terminal > Style
   1. 1. Font: Source Code Pro, Size: 10
      2. Background: rgba(0,0,0,170|67%)
2. Menu > Preferences
   1. Customize Look and Feel
      1. Widget: elementary Dark, Source Sans Pro | 12
      2. Icon Theme: GNOME
      3. Mouse Cursor: DMZ Black
      4. Window Border: Nightmare or Onyx
      5. Other:
         1. GUI Options:
            1. Toolbar Icon Size -> Small toolbar icon
   2. Openbox Configuration Manager
      1. Appearance
         1. Fonts: All Source Sans Pro Regular (10)
         2. Moving and Resizing Windows: Update the window contents while resizing
   3. Desktop Preferences

## Shortcuts

* `alt+f1` - Open Command Menu
* `alt+f2` - Command / Run
* `ctrl+alt+t` - Open Terminal (new window)
* ​