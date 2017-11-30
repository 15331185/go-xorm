# 使用xorm构建数据服务


### 1、任务要求   

使用 xorm 或 gorm 实现本文的程序，从编程效率、程序结构、服务性能等角度对比 database/sql 与 orm 实现的异同！ 
  
### 2、实验过程  
#### (1)启动容器　　
![此处输入图片的描述][1]　　


#### (2)运行mysql  
![此处输入图片的描述][2] 
  
#### (3)创建数据库    
![此处输入图片的描述][3]  

#### (4)测试 web 服务  
##### a.运行服务器  
![此处输入图片的描述][4]

##### b.插入数据  
![此处输入图片的描述][5]

##### c.查询数据  

![此处输入图片的描述][6]　　

#### (5)性能测试  　
##### a.database/sql 的性能测试　　
![此处输入图片的描述][7]　　

##### b.xorm 的性能测试　　
　　
![此处输入图片的描述][8]　　
　　
由time taken for tests 可以看出xorm的效率要低一些。　　
　　
### 3、比较异同　　
##### a.编程效率　　
从编程效率来看，显然xorm要更胜一筹，xorm通过连写操作，可以通过很少的语句完成数据库操作。　　 支持缓存，事务，乐观锁，多种数据库支持，反转等等特性，而不用关心细节。　　
　　
##### b.程序结构　　
xorm通过连写操作,能简化程序。　　
　　
##### c.服务性能　　
xorm的效率要低一些。

  [1]: https://raw.githubusercontent.com/thougr/cloudgo-data/master/sreenshot/ps.png
  [2]: https://raw.githubusercontent.com/thougr/cloudgo-data/master/sreenshot/run%20mysql.png
  [3]: https://raw.githubusercontent.com/thougr/cloudgo-data/master/sreenshot/createtables.png
  [4]: https://raw.githubusercontent.com/thougr/cloudgo-data/master/sreenshot/runserver.png
  [5]: https://raw.githubusercontent.com/thougr/cloudgo-data/master/sreenshot/insert.png
  [6]: https://raw.githubusercontent.com/thougr/cloudgo-data/master/sreenshot/selectall.png
  [7]: https://raw.githubusercontent.com/thougr/cloudgo-data/master/sreenshot/absql.png
  [8]: https://raw.githubusercontent.com/thougr/cloudgo-data/master/sreenshot/abxorm.png

