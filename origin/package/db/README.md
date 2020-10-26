## DB 数据库封装 [<a href="https://github.com/shenqiwei/origin_readme/tree/master/origin/package">返回</a>]
Origin ver 1.0后数据支持Mysql，MariaDB，SQL server，PostgreSQL，Sqlite，Oracle，Mongodb（基础功能支持），Redis（部分结构支持）。
功能实现封装在DB类中，使用时需预先在配置文件（common/config/config.php）中设置数据参数  

#### 调用方式
Origin DB模块使用静态方式进行数据库对象封装

`use Origin\Package\DB;`
`$_db = DB::数据库(数据源配置名)`：数据源配置名称对应的时config中数据库配置项`DATA_NAME`内容

#### 关系型数据库
> `mysql`：`DB::mysql($connect_name)` mariaDB与mysql驱动结构完全一致，故引用方法使用mysql     
> `SQL server`：`DB::mssql($connect_name)`    
> `PostgreSQL`：`DB::pgsql($connect_name)`    
> `Oracle`：`DB::oracle($connect_name)`    
> `Sqlite`：`DB::sqlite($connect_name)`   
>
关系数据库功能函数
`$_db->table($table,$table_as)`：标记操作表名（主表）    
> `$table`：表名    
> `$table_as`：表名别称     

`$_db->setPrimary($field)`：标记自增主键字段名信息     
> `$field`：表主键字段名      

`$_db->join($join_table,$join_field,$major_field,$join_table_as=null,$join_type)`： 表关联操作
> `$join_table`：关联表名     
> `$join_field`：关联字段名    
> `$major_field`：主表关联字段名    
> `$join_table_as`：关联表别名    
> `$join_type`：关联方式    
    
`$_db->iJoin($join_table,$join_field,$major_field,$join_table_as)`：内关联     
`$_db->lJoin($join_table,$join_field,$major_field,$join_table_as)`：左关联    
`$_db->rJoin($join_table,$join_field,$major_field,$join_table_as)`：右关联 
> 三个表关联基于join函数，关联类型限定
   
`$_db->top($number, $percent)`：mssql数据支持显示指定数量或百分比数据函数     
> `$number`：显示数量
> `$percent`：百分比

`$_db->total($field)`：获取数据总数     
> `$field`：字段名，或者 * 不指定

`$_db->field($field)`：查询字段名，默认信息是符号（*）
> `$field`：字段名，数组类型，$key为原字段名，$value为简写名（可省略）   
      
`$_db->distinct($field)`：列出单列字段名不同值 distinct 语句，该语句仅支持单列字段显示，如果需要显示多列信息，需要时group     
> `$field`：字段名，数组类型，$key为原字段名，$value为简写名（可省略）    

`$_db->union($table, $field)`：对多个查询语句的相同字段中的相同数据进行合并,当前版本仅支持两个表单字段查询，并对输入结构进行验证和隔离     
> `$table`：表名
> `$field`：字段名

`$_db->data($field)`：添加修改值获取方法，   
> `$field`：字段名，数组类型，数组key为字段名，数组value为传入值     

`$_db->where($condition)`：条件信息加载方法，传入值类型支持字符串、数组，数组结构可以为多级数组
> 1.当数组key为字段名，数组value为条件值，条件表述为等于条件，若数组value为数组结构    
> 2.当数组key为特定字符串（$and 或 $or）,数组value必须为数组结构，数组结构表述与表述 1要求相同    
> 3.数组关系结构中，同级条件结构放在同一个上级数组内容    
> 4.当为字符串，要求条件信息符合SQL语句规则    
     
`$_db->group($field)`： 去重（分组，指定字段名）显示列表信息    
> `$field`：字段名    

`$_db->abs($field)`：求正整数值，支持单字段名    
> `$field`：字段名

`$_db->avg($field)`：求平均数值，支持单字段名     
> `$field`：字段名

`$_db->max($field)`：查询语句指定字段中最大值，支持单字段名     
> `$field`：字段名

`$_db->min($field)`：查询语句指定字段中最小值，支持单字段名    
> `$field`：字段名

`$_db->sum($field)`：查询指定字段下所有列值的总和，只支持数字型字段列    
> `$field`：字段名

`$_db->mod($field,$second)`：取余    
> `$field`：字段名
> `$second`：比对字段名

`$_db->random()`：求随机数    

`$_db->lTrim($field,$str)`：去除左边指定字符（空格）    
> `$field`：字段名    
> `$str`：需去除的符号    

`$_db->trim($field,$str)`：去除指定字符（空格）    
> `$field`：字段名    
> `$str`：需去除的符号    

`$_db->rTrim($field,$str)`：去除右边指定字符（空格）    
> `$field`：字段名    
> `$str`：需去除的符号    

`$_db->replace($field,$pattern,$replace)`：指定字符替换    
> `$field`：指定字段名    
> `$pattern`：搜索值    
> `$replace`：替换值    

`$_db->upper($field)`：返回指定字段信息中的字母全部大写，支持数组及字符串    
> `$field`：指定字段名

`$_db->lower($field)`：返回指定字段信息中的字母全部小写，支持数组及字符串    
> `$field`：指定字段名

`$_db->mid($field, $start, $length)`：查询语句对指定字段进行截取    
> `$field`：字段名     
> `$start`：起始位置     
> `$length`：截取长度    

`$_db->length($field)`：计算指定字段列记录值长度，一般只应用于文本格式信息    
> `$field`：字段名

`$_db->round($field, $decimals,$accuracy)`：对指定字段进行限定小数长度的四舍五入运算    
> `$field`：字段名    
> `$decimals`：取舍精度    
> `$accuracy`：截断精度 mssql支持语法参数项，默认值 null，mssql需填写参数    

`$_db->now()`：获取数据库当前时间    

`$_db->format($field, $format)`：对指定字段记录进行格式化处理    
> `$field`：字段名
> `$format`：格式化表达式

`$_db->having($func, $field, $symbol, $value)`：函数结构应用, 单项内容操作，暂不推荐使用    

`$_db->order($field, $type='asc')`：查询语句排序条件    
> `$field`：字段名
> `$type`：排序规则，asc正序，desc倒叙

`$_db->limit($start, $length=0)`：查询语句查询限制，有两个参数构成，起始位置，显示长度    
> `$start`：起始位置   
> `$length`：显示长度   

`$_db->fetch($fetch_type)`：数据库查询返回内容类型
> `$fetch_type`：查询输出类型，包含3种基本参数，all：完整结构模式，nv：自然数结构模式，kv：字典结构模式    

关系数据库执行函数

`$_db->count()`：查询总数结构方法，返回一个整数结果    

`$_db->select()`：查询表格信息方法，并返回数组结果集    

`$_db->insert()`：向表插入信息方法，并返回插入成功后插入后数据id，0表示失败    

`$_db->update()`：删除指定数据记录，并返回执行结果信息，大于等于1值表示已成功，0表示失败    

`$_db->delete()`：修改指定数据记录，并返回执行结果信息，大于等于1值表示已成功，0表示失败      

`$_db->query($query)`：执行自定义查询语句,并返回执行结果    
> `$query`：sql语句 
> 如果sql语句结构比较复杂时，可直接使用该函数方法进行sql操作
> query函数返回值内容，根据select，insert，update，delete类型决定

`$_db->getErrorMsg()`：返回错误信息        

#### 非关系型数据库    
> `Mongodb`：<a href="https://github.com/shenqiwei/origin_readme/tree/master/origin/package/db/mongo">访问文档</a>     

> `Redis`：<a href="https://github.com/shenqiwei/origin_readme/tree/master/origin/package/db/redis">访问文档</a>   