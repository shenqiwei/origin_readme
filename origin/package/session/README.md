##Session 服务器会话封装 [<a href="https://github.com/shenqiwei/origin_readme/tree/master/origin/package">返回</a>]
session封装将session设置，创建会话，获取会话拆分设计，分成3个基本功能函数，构造函数会自动对session状态进行判断

#### 调用方法
> Origin 封装结构需实例化类对象，来实现基本功能的调用    
> `use Origin\Package\Session;` 调用封装包    
> `$_session = new Session()`实例化对象 

#### 函数说明    

`(new Origin\Package\Session())->edit($option,$key)` 设置session状态及获取系统值    
> `$option`：设置项，默认值 null     
> `$key`：会话键名    
>
session设置对象    
> `id`：获取session_id值    
> `unset`：注销整个会话内容    
> `destroy`：清空整个会话内容    
> `regenerate`：重置session_id    
> `reset`：重置会话内容    
> `delete`：删除指定会话内容，这里需标明<$key>值    
> `encode`：对会话内容编码    
> `decode`：解码指定会话内容，这里需标明<$key>值    

`(new Origin\Package\Session())->set($key,$value)` 创建会话内容    
> `$key`会话键名    
> `$value`：会话值    

`(new Origin\Package\Session())->get($key)`获取会话内容    
> `$key`：会话键名    