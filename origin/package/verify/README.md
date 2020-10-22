## 验证码封装 [<a href="https://github.com/shenqiwei/origin_readme/tree/master/origin/package">返回</a>]
根据日常开发需求，Origin提供4种验证码函数

#### 调用方法
> Origin 封装结构需实例化类对象，来实现基本功能的调用    
> `use Origin\Package\Verify;` 调用封装包    
> `$_verify = new Verify($widht,$height)`实例化对象   

#### 函数说明

`(new Origin\Package\Verify($widht,$height))`：使用函数前需声明类对象并写入验证参数
> `$width`：图片展示宽度，默认值 120    
> `$height`：图片展示高度，默认值 50    
    
`(new Origin\Package\Verify())->main()`：英文字母与数字混合验证码     

`(new Origin\Package\Verify())->number()`：数字验证码     

`(new Origin\Package\Verify())->letter()`：英文字母验证码    

`(new Origin\Package\Verify())->han()`：汉字验证码     

`(new Origin\Package\Verify())->math()`：二元运算验证码    

验证码返回内容为image/png图片格式，前端调用时直接使用<img/>标签
