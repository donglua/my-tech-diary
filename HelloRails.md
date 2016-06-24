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

指定IP和端口
```
rails server -b $IP -p $PORT
```

## MVC结构
* 模型
* 视图
* 控制器


## Hello World

添加一个控制器动作，渲染字符串“hello, world!
* 在 ApplicationController 中添加 hello 动作
_app/controllers/application_controller.rb_
```ruby
class ApplicationController < ActionController::Base
  # Prevent CSRF attacks by raising an exception.
  # For APIs, you may want to use :null_session instead.
  protect_from_forgery with: :exception

  def hello
    render text: "hello, world!"
  end
end
```
* 修改Rails路由

_config/routes.rb_

```
Rails.application.routes.draw do
  # You can have the root of your site routed with "root"
  # root 'welcome#index”
  root 'application#hello'
end
```







