# SuperrrrrSqlHelper

#### 该项目为一个基于C#用来操作数据库的简单类库，可以嵌入.NET项目中使用。

### 如何使用(简单)
+ 类文件
```
//引用这个项目的DLL后
using SuperrrrrSqlHelper;

public void Demo()
{
   Sqlhelper sh = new Sqlhelper();
   return Json(sh.GetConn());
}
```
+ web.config
```
<appSettings>
    <add key="connectionString" value="Data Source=.;Initial Catalog=datatable;User ID=userid;Password=userpwd;" />
</appSettings>
```
