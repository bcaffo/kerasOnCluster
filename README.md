# kerasOnCluster
A document about installing keras on the cluster

[https://my.justhost.com/hosting/help/python-install](https://my.justhost.com/hosting/help/python-install)


First you have to install python locally:
```
wget http://www.python.org/ftp/python/2.7.2/Python-2.7.2.tgz
tar zxfv Python-2.7.2.tgz
find ~/python -type d | xargs chmod 0755
cd Python-2.7.2
./configure prefix=$HOME/python --with-threads --enable-shared
make
make install
```

add the following to your bashrc or bash_profile
```
export PATH=$HOME/python/Python-2.7.2/:$PATH
```
