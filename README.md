My Ubuntu Desktop
===
<img src="https://raw.githubusercontent.com/jenghung/my-ubuntu-desktop/master/screenshots/screenshot1.png">

* More screenshots:

> https://plus.google.com/communities/112725216256580894446/stream/921e0ee8-fdd9-43ee-b6c5-355c4c1d8cff

## Basic Install And Settings
### Utility 
```sh
sudo apt-get update
sudo apt-get install vim 
sudo apt-get install git
sudo apt-get install unity-tweak-tool
```
### Settings
* .bashrc
```sh
alias ls='ls -a --color=auto' 
alias rm='rm -i'
```
* nautilus


## Chinese Input
### fcitx
* install
```sh
sudo apt-get install fcitx
sudo add-apt-repository ppa:fcitx-team/nightly
sudo apt-get update
sudo apt-get install fcitx-chewing
```
* change default ibus to fcitx

> References:
>
> http://lodour.blogspot.tw/2014/08/ubuntu.html

## Brightness Fn Shortcut
http://askubuntu.com/questions/230609/brightness-keyboard-buttons-do-not-work-on-asus-1225c

## Fonts
* Download Google Noto Sans Font:

https://www.google.com/get/noto/pkgs/Noto-hinted.zip

* Download Adobe Source Pro Series Fonts:

https://github.com/adobe-fonts/source-serif-pro/releases

https://github.com/adobe-fonts/source-code-pro/releases

https://github.com/adobe-fonts/source-sans-pro/releases

* Move to all .otf to *~/.fonts* directory

* Edit *~/.config/fontconfig/fonts.conf*
```sh
<fontconfig>
  <match target="pattern">
    <test qual="any" name="family">
      <string>serif</string>
    </test>
    <edit name="family" mode="prepend" binding="strong">
      <string>SourceSerif Pro</string>
      <string>Noto Sans CJK TC</string>
      <string>Noto Sans CJK SC</string>
      <string>Noto Sans CJK JP</string>
      <string>Noto Sans CJK KR</string>
    </edit>
  </match> 
  <match target="pattern">
    <test qual="any" name="family">
      <string>sans-serif</string>
    </test>
    <edit name="family" mode="prepend" binding="strong">
      <string>SourceSans Pro</string>
      <string>Noto Sans CJK TC</string>
      <string>Noto Sans CJK SC</string>
      <string>Noto Sans CJK JP</string>
      <string>Noto Sans CJK KR</string>
    </edit>
  </match>
  <match target="pattern">
    <test qual="any" name="family">
      <string>monospace</string>
    </test>
    <edit name="family" mode="prepend" binding="strong">
      <string>SourceCode Pro</string>
      <string>Noto Sans CJK TC</string>
      <string>Noto Sans CJK SC</string>
      <string>Noto Sans CJK JP</string>
      <string>Noto Sans CJK KR</string>
    </edit>
  </match>
</fontconfig>
```

> References:
> 
> http://scar.simcz.tw/article/2014/04/22/fix-ubuntu-14-04-lts-zh-font-selector/
> 
> http://ingramchen.io/blog/2014/07/ubuntu-noto-font.html
> 
> http://samwhelp.github.io/blog/read/linux/ubuntu/font/font-noto/
> 
> https://github.com/adobe-fonts

## Ubuntu yosemite Theme
http://www.noobslab.com/2014/11/mbuntu-macbuntu-1410-transformation.html

http://www.noobslab.com/2014/04/macbuntu-1404-pack-is-released.html

http://jamyy.us.to/blog/2014/12/6917.html

http://dgk15.deviantart.com/art/OS-X-Yosemite-theme-0-2-for-Ubuntu-14-04-472626539

https://www.youtube.com/watch?v=hh3x4loZPCw

https://www.youtube.com/watch?v=DSf7aujD7tI

http://andrewjhazelton.deviantart.com/art/OS-X-10-10-Yosemite-Wallpaper-Blur-458548536

## Flat Theme
http://gnome-look.org/content/show.php/Ultra-Flat?content=167473

http://snwh.org/paper/

https://medium.com/@foxoman/royal-ubuntu-theme-40a635534e1

## Flat Icons
https://numixproject.org/

https://github.com/numixproject/numix-icon-theme-circle

https://github.com/NitruxSA/flattr-icons

http://gnome-look.org/content/show.php/Ultra-Flat-Icons?content=167477

## Solarized Color Theme
https://github.com/Anthony25/gnome-terminal-colors-solarized

https://github.com/seebi/dircolors-solarized

https://gist.github.com/gmodarelli/5942850

https://github.com/mattcan/solarized-gedit

## GIT
* git prompt
```sh
#git bash
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}
PS1="${debian_chroot:+($debian_chroot)}\u@\h:\w\$(parse_git_branch)$ "
```
* git gui tools
```sh
sudo apt get install gitg
sudo apt get install meld
```
http://wiki.rabbitvcs.org/wiki/install/ubuntu
http://www.gitguys.com/topics/merging-with-a-gui/?lang=zh
https://groups.google.com/forum/#!topic/rabbitvcs/hOvlrZTyz6M  (Use en_GB)

## JAVA Development Environment
http://www.webupd8.org/2012/01/install-oracle-java-jdk-7-in-ubuntu-via.html

plugin: jrebel, quick serach, eclipse color theme, easy shell

http://sourceforge.net/projects/realignmentjd/files/

server: Jboss AS Tools

http://stackoverflow.com/questions/11805784/very-large-tabs-in-eclipse-panes-on-ubuntu

http://stackoverflow.com/questions/3124629/how-can-i-configure-the-font-size-for-the-tree-item-in-the-package-explorer-in-e

## Microsoft Office
### Lync
http://nknu.net/ubuntu-14-04-exchange-configuration-thunderbird-pidgin/#pidgin

http://www.howtogeek.com/45932/how-to-disable-pidgin-notifications-in-ubuntu/

### Office
http://www.omgubuntu.co.uk/2014/07/run-microsoft-office-web-apps-ubuntu-desktop

### One Drive
http://www.omgubuntu.co.uk/2014/06/one-drive-ubuntu-integration

https://github.com/xybu/onedrive-d
