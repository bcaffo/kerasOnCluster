# kerasOnCluster
A document about installing keras on the cluster

Try python latest release
```
mkdir ~/python
cd ~/python
wget https://www.python.org/ftp/python/3.6.4/Python-3.6.4.tgz
tar -xvf Python-3.6.4.tgz
cd Python-3.6.4
./configure prefix=$HOME/python --with-threads --enable-shared LDFLAGS="-Wl,--rpath=$HOME/python/lib"
make
make install
```

tensorflow is hard. do the following: [https://www.tensorflow.org/install/install_linux#CommonInstallationProblems](https://www.tensorflow.org/install/install_linux#CommonInstallationProblems)
```
virtualenv --system-site-packages -p python3 ~/tensorflow
source ~/tensorflow/bin/activate
easy_install -U pip
pip3 install --upgrade tensorflow
```

Then do this to use tensorflow in the virtualenv
```
source ~/tensorflow/activate
```

```
pip3 install keras --user
pip3 install theano --user
pip3 install virtualenv --user
```




old stuff
Add `$HOME/python/bin` to your path. 
```
reticulate:::use_python("~/python/bin/python3")
```



This worked from John

In bash
```
module load conda/3.0
module load conda_R/3.4.x
```

Then just install keras as per the documentation


```
pip install keras --user
pip install theano --user
pip install tensorflow --user
```
