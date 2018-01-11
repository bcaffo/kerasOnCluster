# kerasOnCluster
A document about installing keras on the cluster

[https://my.justhost.com/hosting/help/python-install](https://my.justhost.com/hosting/help/python-install)


First you have to install python locally:
```
mkdir ~/python
cd ~/python
wget https://www.python.org/ftp/python/2.7.14/Python-2.7.14.tgz
cd Python-2.7.14
./configure prefix=$HOME/python --with-threads --enable-shared LDFLAGS="-Wl,--rpath=$HOME/python/lib"
make
make install
```

add the following to your bashrc or bash_profile
```
export PATH=$HOME/python/Python-2.7.14/:$HOME/bin/:$HOME/.local/bin:$PATH
```

[Install pip](https://gist.github.com/saurabhshri/46e4069164b87a708b39d947e4527298)
```
wget https://bootstrap.pypa.io/get-pip.py
python get-pip.py --user 
```

Install a ton of python libraries
```
pip install virtualenv --user
pip install keras --user
pip install theano --user
```
