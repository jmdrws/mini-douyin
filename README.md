# simple-demo

## 抖音项目服务端简单示例

具体功能内容参考飞书说明文档

工程无其他依赖，直接编译运行即可

```shell
go build && ./simple-demo
```

### 功能说明

接口功能不完善，仅作为示例

* 用户登录数据保存在内存中，单次运行过程中有效
* 视频上传后会保存到本地 public 目录中，访问时用 127.0.0.1:8080/static/video_name 即可

### 测试数据

测试数据写在 demo_data.go 中，用于列表接口的 mock 测试

## 功能实现

跳过登录验证

user.go中的usersLoginInfo里是测试的用户名密码，拿那个登录

### 投稿功能

data是一个视频文件，token就是user+psd

上传视频时的data参数是客户端那边封装好了的（保存到public文件夹了）

TODO:实测用户查看视频时下载速度有点慢，该怎么解决

数据库里面应该有关list的数据表

用户id 视频名

每个视频是有个url的

封面也是有url的