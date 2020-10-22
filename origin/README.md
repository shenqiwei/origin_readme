## Origin 入口文件
origin入口文件包含origin基本结构调用全部初始化内容常量，部分常量的设置将影响origin部分功能的实现

#### 常量说明
`DEBUG` 设置debug模式状态，默认值 true <开启>，开启状态下origin会自动获取封装及函数实例出现的服务500错误，false状态下页面会自动变成空白    
`TIME`  设置反应时间显示状态，默认值 false <关闭>，开启状态是页面右下角会出现一个时间，时间与实际消耗差10-32ms  
`RELOAD_MARK` 设置模板编码， 默认值 false <关闭>，开启状态view封装结构会自动删除所有'\n'和多余‘\s’内容    
`ERROR` 设置异常显示模式，默认值 false，Debug模式下ERROR依然会正常显示相关信息，当Debug和ERROR同为false时Origin仅显示部分异常信息    
> 错误信息显示
>- E_ALL = 11 所有的错误信息
>- E_ERROR = 1 报致命错误
>- E_WARNING = 2 报警告错误
>- E_NOTICE = 8 报通知警告
>- E_ALL& ~E_NOTICE = 3 不报NOTICE错误, 常量参数 TRUE

`DEFAULT_APPLICATION` 默认访问应用结构指向,默认值 home    
`DEFAULT_CLASS` 默认访问应用类对象指向，默认值 index    
`DEFAULT_FUNCTION` 默认访问对象方法指向，默认值 index    
