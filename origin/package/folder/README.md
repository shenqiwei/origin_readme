## Folder文件夹操作封装 [<a href="https://github.com/shenqiwei/origin_readme/tree/master/origin/package">返回</a>]
Origin ver 1.0 文件夹与文件封装改为两个独立封装类，Folder封装则作为File父类提供部分功能补全

#### 调用方法
> Origin 封装结构需实例化类对象，来实现基本功能的调用    
> `use Origin\Package\Folder;` 调用封装包      
> `$_folder = new Folder($root)`实例化对象    

#### 函数说明
`new Origin\Package\Folder($root)`：使用函数前需声明类对象并地址根参数
> `$root`：根目录地址信息,默认为项目根(ROOT)目录地址    

`(new Origin\Package\Folder())->create($folder, $autocomplete,$throw)`：创建文件夹，权限默认 0777，返回值类型 boolean   
> `$folder`：文件夹路径    
> `$autocomplete`：自动创建完整文件结构，默认值 false <不执行自动创建>，true <执行自动创建>    
> `$throw`：是否直接显示错误信息内容，默认值 false <显示>，true <不显示>    
> 已创建文件夹函数会返回true     

`(new Origin\Package\Folder())->remove($folder,$throw)`：删除当文件夹，返回值类型 boolean     
> `$folder`：文件夹路径     
> `$throw`：是否直接显示错误信息内容，默认值 false <显示>，true <不显示>    
> 如文件夹内有其他文件，删除失败     

`(new Origin\Package\Folder())->rename($folder, $name, $throw)`：修改文件夹名称，，返回值类型 boolean    
> `$folder`：文件夹路径    
> `$folder`：修改名称 <不需要指定完整文件路径>    
> `$throw`：是否直接显示错误信息内容，默认值 false <显示>，true <不显示>    
> 如文件夹不存在，修改失败     

`(new Origin\Package\Folder())->getBreakpoint()`：获取文件夹路径断点     

`(new Origin\Package\Folder())->getError()`：获取执行后错误信息    
> 当执行方法中参数 `$throw` 为true，可以利用该方法获取错误信息内容