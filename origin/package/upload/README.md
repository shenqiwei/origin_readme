## Upload封装 [<a href="https://github.com/shenqiwei/origin_readme/tree/master/origin/package">返回</a>]
upload封装使用$_FILE属性结构，并增加了前置条件验证内容

#### 调用方法
> Origin 封装结构需实例化类对象，来实现基本功能的调用    
> `use Origin\Package\Upload;` 调用封装包    
> `$_upload = new Upload()`实例化对象     

#### 函数说明

`(new Origin\Package\Upload())->condition($input, $type, $size=0)`：设置上传文件的3个基本条件：对象表单名、文件类型、文件大小限制    
> `$input`：表单名称 form type 设置为 'multipart/form-data' 该结构有效    
> `$type`：上传文件类型，origin为了更好识别一些常用文件类型，在类型比对中加入了验证数组
> 
>   text/plain' => 'txt',    
    'application/vnd.ms-excel' =>  'xls',    
    'application/vnd.openxmlformats-officedocument.spreadsheetml.sheet' => 'xlsx',    
    'application/msword' => 'doc',    
    'application/vnd.openxmlformats-officedocument.wordprocessingml.document' => 'docx',    
    'application/vnd.ms-powerpoint' => 'ppt',     
    'application/vnd.openxmlformats-officedocument.presentationml.presentation' => 'pptx',     
    'text/html' => 'html',    
    'image/png' => 'png',    
    'image/jpeg' => 'jpg',     
    'image/gif' => 'gif',    
>
> `$size`：上传文件大小，默认值 0 即受php.ini上传文件大小限制 upload_max_filesize = 2M （初始）

`(new Origin\Package\Upload())->store($guide)`：设置存储路径    
> `$guide` : 存储路径，Origin默认地址指向（resource/upload/当天日期），当前版本下，文件整合功能未进行测试

`(new Origin\Package\Upload())->update()`：上传执行函数        
> 方法会在上传完成之后以上传文件的相对路径，如果失败返回值为null

`(new Origin\Package\Upload())->getError()`：错误返回函数    
> 该方法会返回错误信息