属性文件实例：

##1、单机模式

##### redisson lock
    redisson.address=redis://10.18.75.115:6379
    redisson.password=

    这里如果不加redis://前缀会报URI构建错误，
    Caused by: java.net.URISyntaxException: Illegal character in scheme name at index 0

    其次，在redis进行连接的时候如果不对密码进行空判断，会出现AUTH校验失败的情况。
    Caused by: org.redisson.client.RedisException: ERR Client sent AUTH, but no password is set. channel

##2、哨兵模式

    redisson.master-name=mymaster
    redisson.password=xxxx
    redisson.sentinel-addresses=10.47.91.83:26379,10.47.91.83:26380,10.47.91.83:26381

