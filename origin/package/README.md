<span id='origin_package'></span>
## Package 功能封装 [<a href="https://github.com/shenqiwei/origin_readme">返回</a>]
Origin ver 1.0以后版本都会现有结构为基础进行升级加强，现有结构取消了原有按功能分类方式，使用同一命名空间结构

`Origin\Package\Unit`功能控制类（单元），该结构封装了web功能交互的基础函数内容，应用类通过继承该类实现内容调用 

> `$this->param($key,$value);` 用于调用前端变量数据交换方法,方法参数（$key:变量名，$value:变量值）      
> `$key`：变量名,值结构不需要带变量($)符号,前端标签 echo(输出)结构调用：{$key}, 一般结构调用：$key    
> `$value`：变量值    

> `$this->template($template);` 用于调用前端模板视图模板文件方法，结构视图模板地址(application/应用名/template/类名/方法名.html)     
> `$template`：模板名称，默认值 null 自动调用同名文件内容，设置模板指向时，则调用指向模板内容    
    
> `$this->get_class();` 获取当前被访问对象类名称   
  
> `$this->get_function();` 获取当前被访问对象方法名称     

> `$this->success($message,$url,$time);` 用于操作行文成功后进行地址重定向（redirect）,在重定向前会调用预设模板显示$message中设置内容    
> `$message`：自定义以信息    
> `$url`：重定向地址    
> `$time`：等待重定向时间    
  
> `$this->error($message,$url,$time);` 用于操作行文失败后进行地址重定向（redirect）,在重定向前会调用预设模板显示$message中设置内容    
> `$message`：自定义以信息    
> `$url`：重定向地址    
> `$time`：等待重定向时间    
> success和error调用默认模板(origin/template/201.html),也可以自定模板（存储位置resource/public/temp）success:200.html,error:400.html
 
> `$this->json($array);`将传入数据内容转为json格式，并返回json串     

