## curl远程请求封装 [<a href="https://github.com/shenqiwei/origin_readme/tree/master/origin/package">返回</a>]
curl封装依托于PHP curl模块进行再开发封装，对现有部分常用结构进行集成使用

#### 调用方法
> Origin 封装结构需实例化类对象，来实现基本功能的调用    
> `use Origin\Package\Curl;` 调用封装包    
> `$_curl = new Curl()`实例化对象 

#### 函数说明

`(new Origin\Package\Curl())->get($url, $param, $header, $ssl_peer, $ssl_host)`：模拟get请求，返回内容为string类型    
> `$url`：访问地址    
> `$param`：访问参数，（k/v）数组结构，默认值 array()     
> `$header`：请求报文，默认值 array()     
> `$ssl_peer`：验证证书，默认值 false <不验证>    
> `$ssl_host`：验证地址，默认值 false <不验证>    
> get与post在编码结构上基本相同，仅在post中增加了请求类型和请求周期限制

`(new Origin\Package\Curl())->post($url, $param, $header, $ssl_peer, $ssl_host)`：模拟post请求，返回内容为string类型    
> `$url`：访问地址    
> `$param`：访问参数，（k/v）数组结构，默认值 array()     
> `$header`：请求报文，默认值 array()     
> `$ssl_peer`：验证证书，默认值 false <不验证>    
> `$ssl_host`：验证地址，默认值 false <不验证>    

`(new Origin\Package\Curl())->upload($url, $folder, $type, $header, $input, $ssl_peer, $ssl_host)`：模拟post请求提交文件，返回内容为string类型    
> `$url`：访问地址    
> `$folder`：本地文件地址     
> `$type`：文件类型     
> `$header`：请求报文，默认值 array()     
> `$input`：表单名, 默认值 pic <图片简写>     
> `$ssl_peer`：验证证书，默认值 false <不验证>    
> `$ssl_host`：验证地址，默认值 false <不验证>
> upload模拟multipart/form-data模式进行提交，提交内容变量$folder需引述绝对路径

`(new curl())->get_curl_receipt()`：获取curl返回错误信息    
