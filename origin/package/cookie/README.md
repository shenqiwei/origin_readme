## Cookie 浏览器会话封装 [<a href="https://github.com/shenqiwei/origin_readme/tree/master/origin/package">返回</a>]
cookie封装结构与session一直

#### 调用方法
> Origin 封装结构需实例化类对象，来实现基本功能的调用    
> `use Origin\Package\Cookie;` 调用封装包    
> `$_cookie = new Cookie()`实例化对象 

#### 函数说明

`(new Origin\Package\Cookie())->edit($option,$key)` 设置session状态及获取系统值    
> `$option`：设置项，默认值 null     
> `$key`：会话键名    
>
cookie设置对象    
> 当前版本cookie设置项使用ini_set实现，所以设置对象可以参照PHP官网进行相关操作

`(new Origin\Package\Cookie())->set($key,$value)` 创建会话内容    
> `$key`会话键名    
> `$value`：会话值    

`(new Origin\Package\Cookie())->get($key)`获取会话内容    
> `$key`：会话键名 