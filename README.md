# tgonpython

Steps to get telegram CLI on python2

### Create pyenv

$ cd ~
$ wget https://bootstrap.pypa.io/get-pip.py
$ sudo python get-pip.py
$ sudo pip install virtualenv virtualenvwrapper
$ sudo rm -rf ~/get-pip.py ~/.cache/pip
$ echo -e "\n# virtualenv and virtualenvwrapper" >> ~/.bashrc
$ echo "export WORKON_HOME=$HOME/.virtualenvs" >> ~/.bashrc
$ echo "source /usr/local/bin/virtualenvwrapper.sh" >> ~/.bashrc
$ source ~/.bashrc
$ mkvirtualenv pytg -p python2

### Install telegramCLI
### https://github.com/vysheng/tg

$ git clone --recursive https://github.com/vysheng/tg.git && cd tg

### Install telegramCLI python support

$ sudo apt-get install libreadline-dev libconfig-dev libssl-dev lua5.2 liblua5.2-dev libevent-dev libjansson-dev libpython-dev make 

$ ./configure
$  make

### Install the Telegram python wrapper (from @vysheng)
### https://github.com/luckydonald/pytg

$ pip install pytg

then see https://github.com/luckydonald/pytg for hello world

### gotchas

if dpkg is locked 

You can delete the lock file with the following command:

sudo rm /var/lib/apt/lists/lock

You may also need to delete the lock file in the cache directory:

sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock
