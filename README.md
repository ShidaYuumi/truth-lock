# truth-lock

#### 介绍
分布式锁（自己写的玩具）

#### 软件架构
玩具

#### 安装教程

```xml
        <dependency>
            <groupId>com.truth</groupId>
            <artifactId>truthLock-spring-boot-starter</artifactId>
            <version>${version}</version>
        </dependency>
```

#### 使用说明

1. 根据自己需要引入zookeeper、spring data redis、redisson依赖
2. 在配置中自己确认，自己使用的是那种分布式锁

```yaml
truth:
  lock:
    zookeeper:
      zk-servers: 127.0.0.1:2181
    # 使用zookeeper作为分布式锁
    lock-type: zookeeper
    # 在不指定的的情况下，使用zookeeper读锁作为默认锁
    executor: zookeeper_read_lock
...# 其他的具体看配置信息
```
