# install_redis  (centos7)

* 第一步
  * 先安裝python
```js
sudo yum install gcc  
sudo yum install zlib-devel  
cd /usr/src  
wget https://www.python.org/ftp/python/3.6.1/Python-3.6.1.tgz  
tar xzf Python-3.6.1.tgz  
cd Python-3.6.1  
./configure
make altinstall    #避免蓋掉舊版python
ln -s /usr/src/Python-3.6.1/python python3   # 建立 soft link 至開機執行目錄
python3.6    #執行python
```
* 第二步
  * 安裝pip
  ```js
  yum -y install epel-release
  yum install python-pip
  pip install --upgrade pip
  ```

* 可以開始安裝redis了

```js
wget http://download.redis.io/releases/redis-6.0.8.tar.gz
tar xzf redis-6.0.8.tar.gz
cd redis-6.0.8
make
```

* 如果出現錯誤代表gcc可能太舊
  * 安裝
  ```js
  sudo yum update    #先更新yum
  sudo yum install centos-release-scl
  sudo yum install devtoolset-7-gcc*
  sudo yum install devtoolset-7
  scl enable devtoolset-7 bash
  
  gcc --version   #安裝完後看一下gcc版本是否已更新到最新版
  ```
* 啟動redis(如果成功會看到redis的mark)

```js
src/redis-server
```

* 官網
[https://redis.io/download](https://redis.io/download)
