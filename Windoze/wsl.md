# Windows Subsystem for Linux

WSL is a nice step forward for developing in Windoze, but it still has some issues.

1. Enable WSL in Powershell (as admin): `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`
2. Install Ubuntu from the Windows Store.
3. Install Zsh (via Ubuntu bash shell): `sudo apt install zsh`
4. Make Zsh the default shell: `chsh -s $(which zsh)`
5. Install OhmyZsh: `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
6. Edit `~/.zshrc` to your liking (theme: eastwood, plugins, etc)
7. Back in Windoze: Switch the default shell in VSCode to use the Ubuntu Bash shell.
8. ?
9.  Profit!

## Foundation by Zurb

- Install nvm with `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash`
- Install node v11.15.0 with `nvm install 11.15.0`
- Install Foundation CLI with `npm install -g foundation-cli`

## Troubleshooting

### Git Operations not Permitted

By default, Windoze doesn't mount it's own drives properly, so you need to remount with these options.

1. cd out of directory if in it first!
2. `sudo umount /mnt/c`
3. `sudo mount -t drvfs C: /mnt/c -o metadata`
4. Edit `/etc/wsl.conf`:
   1. ```ini
      [automount]
      enabled = true
      options = "metadata"
      ```
