## Redis 学习笔记：

### 1、java 连接Redis

​	用到的核心 jar `Jedis`

```xml
<dependency>
    <groupId>redis.clients</groupId>
    <artifactId>jedis</artifactId>
    <version>3.0.1</version>
</dependency>
```


Windows 上开启 Redis服务：

​	cmd 命令：`redis-server --service-install redis.windows-service.conf --loglevel verbose`

测试代码：

```java
public static void main(String[] args) {
    //连接本地的 Redis 服务
    Jedis jedis = new Jedis("localhost");
    System.out.println("连接成功");
    //查看服务是否运行
    System.out.println("服务正在运行: "+jedis.ping());
}
```


