## library 实例封装 [<a href="https://github.com/shenqiwei/origin_readme">返回</a>]
Origin ver 1.0以后取消部分应用实例封装，仅保留了6基本函数用于完成一半web开发内容需求

`replace()` 路径链接符替换函数，用于将当前系统反向符号转换为链接符,该函数主要在WIN条件下使用    

    function replace($uri)
    {
        return str_replace(RE_DS,DS,$uri);
    }
> $url：文件夹访问路径    

`is_true()` 判断正则对象是否有效    

    function is_true($regular,$param)
    {
        $_validate = new Origin\Package\Validate($param);
        return $_validate->_type($regular);
    }
> 函数方法实现调用Origin Validate封装结构，_type()基于（preg_match）用于验证对象内容是否符合正则要求，返回值为bool类型    
> $regular：正则表达式    
> $param：验证对象    
    
`request()` 用于相应input对象请求，其请求类型为request，即POST&GET任意请求内容，请返回值内容为string类型    
> $key：请求对象键    
> $default：请求失效后返回默认值，初始值 null    
> $delete：执行获取后删除操作，默认值 false <不删除>    
> $type：请求类型，默认值 request    
    
`post()` 获取input post请求，其实现功能主要依托于request()，返回值及功能类型与request()相一致，仅其类型固定为post    

    function post($key, $default=null, $delete=false)
    {
        return request($key, $default, $delete,"post");
    }
> $key：请求对象键    
> $default：请求失效后返回默认值，初始值 null    
> $delete：执行获取后删除操作，默认值 false <不删除>   

`get()` 获取input get请求，其实现功能主要依托于request()，返回值及功能类型与request()相一致，仅其类型固定为get     

    function get($key, $default=null, $delete=false)
    {
        return request($key, $default, $delete,"get");
    }
> $key：请求对象键    
> $default：请求失效后返回默认值，初始值 null    
> $delete：执行获取后删除操作，默认值 false <不删除>      
    
`session()`用于进行简单会话内容操作函数，其返回值为预设值或null

    function session($key,$value=null)
    {
        $_session = new \Origin\Package\Session();
        if(is_null($value)){
            return $_session->get($key);
        }else{
            return $_session->set($key,$value);
        }
    }
> 函数方法实现基于Origin\Package\Session中两个基本方法，根据$value值状态进行区分调用     
> $key：会话键名     
> $value：会话值     
   