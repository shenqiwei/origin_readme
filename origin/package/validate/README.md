## 变量验证封装 [<a href="https://github.com/shenqiwei/origin_readme/tree/master/origin/package">返回</a>]
origin ver 1.0取消原有整个方式，将原始封装分成4个基本验证函数

#### 调用方法
> Origin 封装结构需实例化类对象，来实现基本功能的调用    
> `use Origin\Package\Validate;` 调用封装包    
> `$_validate = new Validate($vaiable)`实例化对象 

#### 函数说明
`new Origin\Package\Validate($variable)`：使用函数前需声明类对象并写入验证参数    
> `$variable`：需验证参数值，参数类型不能为数组    

`(new Origin\Package\Validate($vaiable))->_empty()`：验证对象是否为空，值为空返回 false，反之返回true   
> 函数内部对数字，特定字符串，bool值内容进行区别限定验证，所以 0，false等特定值将不再是为空值内容
  
`(new Origin\Package\Validate($vaiable))->_size($min,$max)`：验证传入值长度是否在限定范围，当限定为0，则返回值默认为 true   
> `$min`：最小限定值，默认值 0
> `$max`：最大限定值，默认值 0
> 当$min值大于$max时，origin自定转换值内容，以完成验证过程

`(new Origin\Package\Validate($vaiable))->_type($format)`：验证传入值是否符合正则表达式限定要求，符合返回 true，不符合返回 false 
> 为了更好使用该功能，Origin的实例结构中已经编写了一个直接调用函数
   
`(new Origin\Package\Validate($vaiable))->_ipv4()`：验证ipv4格式，由于开发需求，所以单独编写结构    

`(new Origin\Package\Validate($vaiable))->_ipv6()`：验证ipv6格式，由于开发需求，所以单独编写结构    

`(new Origin\Package\Validate($vaiable))->getError()`：获取验证内容错误信息    