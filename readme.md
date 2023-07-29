# 简易版抖音项目

## 项目启动
### 建表
resources/initial.sql  
resources/insertData.sql  

### 替换redis地址
config/redis.go  

### 替换腾讯云oss服务密钥
config/tencent_oss


### 直接启动
```shell
cd go 
```
```shell
go run main.go 
```  

## APP 操作
设置服务端地址
为方便测试登录和注册，及修改网络请求的服务器地址，提供了退出登录和高级设置两个能力。
1. 点击退出登录会自动重启
2. 在高级设置中可以配置自己的服务端项目的前缀地址，如下配置的http://192.168.1.7:8080
   在app中访问上述某个接口时就会拼接该前缀地址，例如访问 http://192.168.1.7:8080/douyin/feed/ 拉取视频列表
![](https://image-bed-1313520634.cos.ap-beijing.myqcloud.com/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202023-03-07%20162902.png)

## 表数据

## 使用mvc分层结构
参考文献  （不懂的可以参考这篇文章）
https://juejin.cn/post/7152299022017888286



## 版本  
* go版本 1.19  
* mysql 8.0+
* redis驱动
## 使用到的框架与依赖  
+ gin框架
+ gorm框架
+ mysql驱动
+ golang的jwt框架
+ 腾讯云的oss存储（设置了工作流用于截取视频的第一帧(.jpg)并储存在相同的桶中）文献: https://juejin.cn/post/7195857732846567485
+ redis驱动


## 注意
* **目前上传文件接口只支持mp4格式**

