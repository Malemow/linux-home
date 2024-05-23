建立 Debain 12
### 下載基本套件
===
```bash
apt install -y vim git openssh-server curl
```

### 將 ssh-server 設定為可以使用 root 登入
```bash
sed -i 's/^#\?PermitRootLogin.*/PermitRootLogin yes/' /etc/ssh/sshd_config
```

### 如果要修改網路的話請修改 /etc/network/interfaces
```bash
#iface ens192 inet static
#address your_address
#netmask your_netmask
#gateway your_gateway
```

### 下載 node 使用 nvm
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
nvm install node
```

### 使用 git 的設定
```bash
mv ~/.bashrc ~/.bashrc.bak
mv ~/.profile ~/.profile.bak
git clone https://github.com/Malemow/linux-home.git ~/

mv ~/linux-home/.* ~/
mv ~/linux-home/* ~/

rm ~/linux-home
```

### 下載 Powerline 並且重新套用 bashrc
```bash
apt install -y powerline
fc-cache ~/.fonts/
source ~/.bashrc
```

### 開始設定 Vim
```bash
vim +PlugInstall
#install ctages

#git clone https://github.com/universal-ctags/ctags.git ~/
#apt install -y autoconf automake libtool pkg-config build-essential
#cd ~/ctags
#./autogen.sh
#./configure
#make
#make install
#cd ~/
#rm -rf ~/ctags
```

