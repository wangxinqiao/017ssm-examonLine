#  017ssm在线答题系统
017ssm在线答题系统

#### 技术框架
使用SSM+Vue的形式来实现，SSM框架用于处理后台的数据逻辑，Vue框架用于前端的数据显示
系统分为客户端，管理端

源码获取： [**点此获取**](http://www.shuyue.fun/index.php?type=productinfo&id=120) 

## 注意事项
````
1 数据库文件在一级目录下，命名为answerWeb.sql，部署时，需要在answerWeb/config/dbconfig.properties配置文件中配置好数据库
2 管理端用户表为'admins'表
3 客户端用户表为'user'表，用户端登录页登录帐号为邮箱
4 管理端，在创建题目时，在选择完图片后，图片会立即上传到百度云BOS对象存储中（需要在util包的BOSUtil工具类你的BOS对象存储），未点击添加题目时，此时试题的资源（图片，视频）是在BOS的临时文件夹下（在QuestionController类定义路径），当点击添加题目后，会把此试题的资源添加到目标文件夹下（在QuestionController类定义路径），临时文件夹下的东西可以设置任务调度器进行定时删除，防止浪费BOS存储空间。
5 项目的jar包除了用maven管理外，有一部分jar需要手动导入（answerWeb/WebRoot/WEB-INF/lib）
````

## 运行截图
![输入图片说明](https://images.gitee.com/uploads/images/2021/0317/093715_b39d728d_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0317/093729_54a1679b_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0317/093738_370ded2f_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0317/093747_bff93d59_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0317/093755_e4df428b_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0317/093802_aea5799f_863230.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2021/0317/093812_041a1d96_863230.png "屏幕截图.png")


