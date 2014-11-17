tipask
======
#用户账号相关接口

##用户注册

> URL：api_user/register.html  (http://192.168.1.21:8080/?api_user/register.html)

> HTTP请求方式

- POST

> 请求参数：

- username (string)
- password (string) 
- email (string)
- submit (string)


> 返回结果：

- json 数组用户资料

> 可能返回的错误原因：

- 您已登录!
- 系统注册功能暂时处于关闭状态!
- 您的当前的IP已经超过当日最大注册数目，如有疑问请联系管理员!
- 用户名或密码不能为空!
- 邮件地址不合法!
- 此邮件地址已经注册!
- 邮件地址被禁止注册!
- 用户名已经存在!

##用户登录


> URL：api_user/login.html  (http://192.168.1.21:8080/?api_user/login.html)

> HTTP请求方式

- POST

> 请求参数：

- username (string)
- password (string) 

> 返回结果：

- json 数组用户资料

> 可能返回的错误原因：

- 用户名或密码错误

#获取文章资讯列表

> URL：ca-all.html  (http://192.168.1.21:8080/?ca-all.html)

> HTTP请求方式

- GET

> 请求参数：

- cid (string)[all,1~N]
- status (string)[all,1~N]
- page (int)


> 返回结果：

- rownum (int) (总的记录数)
- curpage (int) (当前分页)
- pagesize (int) (每页显示文章数)
- cid (string)[all,1~N] (分类id)
- status (string)[all,1~N] (状态)
- sublist (Array) (分类数组) {id(分类id),name(分类名称),articles(分类文章数)}
- articlelist (Array) (文章数组){id(文档id),cid(分类id),title(文档名称),category_name(分类名),format_time(文档发布时间)}







