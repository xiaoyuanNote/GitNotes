## Win系统中，Https转换成Ssh链接github远程仓库

> 使用ssh连接远程仓库



### 需求背景

因为通过https来提交github仓库时，老是要填写账户密码，所以我改用ssh来连接仓库。



### 实际操作

##### 步骤 1（生成密钥）

- Win打开cmd
- 输入：ssh-keygen.exe
- 连续回车就OK
- 完成后，将在电脑用户目录下的**.ssh**目录下，生成公钥和私钥

```
id_rsa: 私钥
id_rsa.pub：公钥
```

![](.\md.assets\7.png)



##### 步骤 2（获取密钥，添加到github上）

- Win打开cmd（定位到电脑目录的.ssh文件下）
- 直接输入命令`cat id_rsa.pub`，查看公钥内容
- 复制公钥内容，打开github网页，在Setting中新增SSH key

![](.\md.assets\8.png)



### 参考链接

- [Windows 配置 ssh 免密登录](https://blog.csdn.net/qq_43901693/article/details/103700272)
- [查看本机ssh公钥，生成公钥](https://blog.csdn.net/shog808/article/details/76563136)