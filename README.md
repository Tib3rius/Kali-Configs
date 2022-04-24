# Kali-Configs

The following is a setup guide for Kali Linux, using my config files that I've acquired / developed over the years.

## Install Open VM Tools (if applicable)

```bash
sudo apt update
sudo apt install -y --reinstall open-vm-tools-desktop fuse3
sudo reboot -f
kali-tweaks
	-> Virtualization -> Configure
```

## Install oh-my-zsh

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Copy .zshrc into ~/

```bash
cp .zshrc ~/
```

## Install tmux and powerline.

```bash
sudo apt install tmux powerline
```

### Copy tmux config into ~/

```bash
cp .tmux.conf .tmux.conf.local ~/
```

## Copy .vimrc into ~/

```bash
cp .vimrc ~/
```

## Configure Apache

```bash
sudo cp 000-default.conf /etc/apache2/sites-available/
sudo mkdir /var/www/phpnoexec
sudo rm -rf /var/www/html
sudo touch /var/www/index.php
sudo service apache2 restart
```
