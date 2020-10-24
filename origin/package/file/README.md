## File 文件操作封装 [<a href="https://github.com/shenqiwei/origin_readme/tree/master/origin/package">返回</a>]
Origin ver 1.0 文件夹与文件封装改为两个独立封装类，File封装部分功能继承Folder实现

#### 调用方法
> Origin 封装结构需实例化类对象，来实现基本功能的调用    
> `use Origin\Package\File;` 调用封装包      
> `$_folder = new File($root)`实例化对象    

#### 函数说明
`new Origin\Package\File($root)`：使用函数前需声明类对象并地址根参数
> `$root`：根目录地址信息,默认为项目根(ROOT)目录地址   

`(new Origin\Package\File())->create($folder, $autocomplete,$throw)`：创建文件，权限默认 0777，返回值类型 boolean   
> `$folder`：文件路径    
> `$autocomplete`：自动创建完整文件结构，默认值 false <不执行自动创建>，true <执行自动创建>    
> `$throw`：是否直接显示错误信息内容，默认值 false <显示>，true <不显示>    
> 已创建文件函数会返回true    

`(new Origin\Package\File())->remove($folder,$throw)`：删除当文件，返回值类型 boolean     
> `$folder`：文件路径    
> `$throw`：是否直接显示错误信息内容，默认值 false <显示>，true <不显示>     
> 如文件不存在会返回true     

`(new Origin\Package\File())->rename($folder, $name, $throw)`：修改文件名称，，返回值类型 boolean    
> `$folder`：文件夹路径     
> `$folder`：修改名称 <不需要指定完整文件路径>    
> `$throw`：是否直接显示错误信息内容，默认值 false <显示>，true <不显示>     
> 如文件不存在，修改失败     

`(new Origin\Package\File())->read($file,$operate,$throw)`：读取文件，返回值 false 或 文件内容   
> `$folder`：文件夹路径     
> `$operate`：文件读取方式    
   * r:读取操作 操作方式：r   
   * rw:读写操作 操作方式：r+   
   * sr: 数据结构读取操作 操作对应函数file   
   * rr: 读取全文 调用对应函数 file_get_contents   
> `$throw`：是否直接显示错误信息内容，默认值 false <显示>，true <不显示>     
> 如文件不存在，读取失败     

`(new Origin\Package\File())->write($file,$operate,$throw)`：读取文件，返回值类型 boolean   
> `$folder`：文件夹路径     
> `$operate`：文件写入方式     
   * w：写入操作 操作方式：w     
   * lw：前写入 操作方式：w+    
   * bw：后写入 操作方式：a    
   * fw：补充写入 操作方式：a+    
   * re：重写 调用对应函数 file_put_contents    
> `$throw`：是否直接显示错误信息内容，默认值 false <显示>，true <不显示>     
 

`(new Origin\Package\File())->getBreakpoint()`：获取文件路径断点

`(new Origin\Package\File())->getError()`：获取执行后错误信息
> 当执行方法中参数 `$throw` 为true，可以利用该方法获取错误信息内容