# Rails Hello World

## 安装Rails

```
gem install rails -v 4.2.2
```
## 创建第一个应用

* ```rails new``` 并指定版本号

```
rails _4.2.2_ new hello_app
```
执行 rails new 命令生成所有文件之后，会自动执行 bundle install 命令。

* Bundler

使用 Bundler 安装和包含该应用所需的 gem。

```
cd hello_app/
bundle install
```

* ```rails server```

指定IP端口
```
rails server -b $IP -p $PORT
```



