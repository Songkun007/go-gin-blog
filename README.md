# go-gin-blog
A go example project

# day1
#### 一、初始化项目目录

go-gin-blog/

├── conf

├── middleware

├── models

├── pkg

├── routers

└── runtime

1、conf：用于存储配置文件

2、middleware：应用中间件

3、models：应用数据库模型

4、pkg：第三方包

5、routers 路由逻辑处理

6、runtime：应用运行时数据


#### 二、添加 Go Modules Replace
打开 go.mod 文件，新增 replace 配置项

？？？ 为什么要添加replace配置项？

答：在go.mod中我们可以看到，我们用的完整的外部模块引用路径，github.com/EDDYCJY/go-gin-example/xxx），而这个模块还没推送到远程，是没有办法下载下来的，因此需要用 replace 将其指定读取本地的模块路径，这样子就可以解决本地模块读取的问题
后续每新增一个本地应用目录，你都需要主动去 go.mod 文件里新增一条 replace



#### 三、编写配置包

1、拉去go-ini/ini 的依赖包：go get -u github.com/go-ini/ini

2、在conf目录下创建app.ini配置文件

3、建立调用配置的setting模块，在pkg目录下新建setting目录，新建setting.go文件，该文件的作用是引入app.ini配置文件，并进行一些初始化处理

#### 四、编写API错误包
1、建立错误码的e模块，在pkg目录下新建e目录，新建code.go和msg.go文件
，该模块的作用主要是接口的错误码和错误信息，以及相关函数的定义

#### 五、编写分页工具包
1、在pkg目录下新建util目录，并拉取com的依赖：go get -u github.com/unknwon/com

2、在util目录下新建pagination.go

#### 六、初始化mysql的models
1、拉取gorm的依赖包：go get -u github.com/jinzhu/gorm

2、拉取mysql驱动的依赖包：go get -u github.com/go-sql-driver/mysql

3、在models目录下新建models.go

#### 七、编写Demo

#### 八、优化路由
在routers目录下新疆router.go文件

