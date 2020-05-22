### Configuration Tweaks


```
# static number of workspaces
dconf write /org/gnome/mutter/dynamic-workspaces false
dconf write /org/gnome/desktop/wm/preferences/num-workspaces 4
```

```
# install gnome tweak tools
sudo apt install gnome-tweak-toolc
```
Use gnome-tweak to disable animations
```
# workspace switching on both monitors 
gsettings set org.gnome.mutter workspaces-only-on-primary false
```
### Developer Setup

Grabbed beta channel VSCode for preference sync

https://code.visualstudio.com/insiders/ 

#### Node

Install node using n
```
sudo apt-get install npm
sudo npm install -g n
n 12
n 10
n 8
```

#### yarn

``` npm install -g yarn```

#### RVM
```
gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
\curl -sSL https://get.rvm.io | bash
rvm install 2.4.1
```
#### Git
```
# in ~/dev
git clone git@github.com:hipponot/nimbee.git
git clone git@github.com:hipponot/vagrant.git
git clone git@github.com:hipponot/kudu.git
git clone git@github.com:hipponot/zapt.git
```
#### Build Gems
wootdevsetup.rb
```
cd ~/dev/nimbee/build_tools
wootdevsetup.rb setup -b
```

#### Haxe
Install haxe from this URL - https://haxe.org/download/version/4.0.0-preview.1/
```
sudo ln -snf /opt/haxe-4.0.0-rc1-linux64 /opt/haxe
# add /opt/haxe to your path
# need the below for haxelib
sudo apt install neko
mkdir ~/haxelib && haxelib setup ~/haxelib
```

#### Mounting the share
```
sudo apt install nfs-common
mkdir ~/shared
sudo mount -o resvport -t nfs -o proto=tcp,port=2049 10.0.1.20:/volume2/shared ~/shared
```
