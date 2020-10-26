## 非关系型数据库 Redis   
> Origin ver 1.0版本后 redis封装结构集成了6个功能子包   

#### 调用方式
> `use Origin\Package\DB;`
> `$_redis->DB::redis($connect_name)`

Redis函数列表(redis主包内包含部分功能函数，与子包掉能用方式不同)    

主包：     
> `$_redis->flush($obj)`：执行Redis刷新    
> `$_redis->selectDB($db)`：切换到指定的数据库，数据库索引号 index 用数字值指定，以 0 作为起始索引值     
> `$_redis->saveTime()`：最近一次 Redis 成功将数据保存到磁盘上的时间，以 UNIX 时间戳格式表示    
> `$_redis->time()`：返回redis服务器时间    
> `$_redis->dbSize()`：返回数据库容量使用信息    
> `$_redis->bgAOF()`：异步执行一个 AOF（AppendOnly File） 文件重写操作    
> `$_redis->bgSave()`：异步保存当前数据库的数据到磁盘    
> `$_redis->save()`：保存当前数据库的数据到磁盘   

子包：    
<table>
    <tr>
        <td>redis kv操作封装  </td>
        <td>$_key = $_redis->key()</td>
        <td><a href="https://github.com/shenqiwei/origin_readme/tree/master/common/config">访问文档</a></td>
    </tr>
    <tr>
        <td>redis字符串操作封装</td>
        <td>$_str = $_redis->string()</td>
        <td><a href="https://github.com/shenqiwei/origin_readme/tree/master/common/config">访问文档</a></td>
    </tr>
    <tr>
        <td>redis集合操作封装</td>
        <td>$set = $_redis->set()</td>
        <td><a href="https://github.com/shenqiwei/origin_readme/tree/master/common/config">访问文档</a></td>
    </tr>
    <tr>
        <td>redis哈希表操作封装</td>
        <td>$_hash = $_redis->hash()</td>
        <td><a href="https://github.com/shenqiwei/origin_readme/tree/master/common/config">访问文档</a></td>
    </tr>
    <tr>
        <td>redis类数组操作封装</td>
        <td>$_list = $_redis->lists()</td>
        <td><a href="https://github.com/shenqiwei/origin_readme/tree/master/common/config">访问文档</a></td>
    </tr>
    <tr>
        <td>redis序列化操作封装</td>
        <td>$_seq = $_redis->seq()</td>
        <td><a href="https://github.com/shenqiwei/origin_readme/tree/master/common/config">访问文档</a></td>
    </tr>
</table>