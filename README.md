# install_redis  

* 第一步
```js
wget http://download.redis.io/releases/redis-6.0.8.tar.gz
tar xzf redis-6.0.8.tar.gz
cd redis-6.0.8
make
```

* 如果出現錯誤代表gcc可能太舊
  * 安裝
  ```js
  sudo yum install centos-release-scl
  sudo yum install devtoolset-7
  scl enable devtoolset-7 bash
  
  gcc --version   #安裝完後看一夏gcc版本是否已更新到最新版
  ```
* 啟動redis(如果成功會看到redis的mark)

```js
src/redis-server
```

