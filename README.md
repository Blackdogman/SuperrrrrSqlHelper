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
+ 有哪些方法
```
//得到Conn
GetConn();
//执行不带参数的增删改语句
ExecuteNonQuery(string cmdText, CommandType ct);
//执行带参数的增删改语句
ExecuteNonQuery(string cmdText, SqlParameter[] paras, CommandType ct);
//不带参的查询
ExecuteQuery(string cmdText, CommandType ct)
return DataTable;
//带参的查询
ExecuteQuery(string cmdText, SqlParameter[] paras, CommandType ct)
return DataTable;
//查询返回第一行第一列
ExecuteScalar(string sql);
```
