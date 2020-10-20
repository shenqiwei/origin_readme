## Config 配置 [<a href="https://github.com/shenqiwei/origin_readme">返回</a>]
origin ver 1.0版本后配置文件部分功能由入口文件内的常量参数替代，配置仅对数据源，缓存结构，会话功能进行简单控制，
数据源结构同时支持8种数据库的基本配置需求，样例结构预先编写在origin封装文件当中。     
#### Config配置项说明

__数据源配置：__  
>`DEFAULT_ENGINE_TYPE` 数据驱动类型（innodb,由关系数据库配置限定，该配置只负责辅助框架完成事务管理操作）  
`DATA_USE_TRANSACTION` 数据驱动类型为innodb时，事务操作设置才会生效  
`DATA_CONNECT_MAX` 数据服务最大访问数量,设置该参数后,连接将会被监听,当到达最大连接值时,系统将挂起连接服务,直到有空余连接位置，默认值0（不作限制）  
`DATA_CONNECT_THREAD` 连接是否使用线程,当前版本暂不支持线程  
`DATA_USE_FACTORY` 是否是用数据工厂模式,当前版本暂不支持线程  
`DATA_TYPE` 选择数据库类型,当前版本支持Mysql,MariaDB,SQL server(mssql),PostgreSQL(pgsql),sqlite,Oracle,Redis,MongoDB(基础操作支持)   
`DATA_HOST`  服务访问地址  
`DATA_USER`  登录用户  
`DATA_PWD` 登录密码  
`DATA_PORT`  默认访问端口 mysql:3306,mariadb:3306,PostgreSQL:5432,Redis:6379,MongoDB:27017    
`DATA_DB` 访问数据库  
`DATA_USE_MEMCACHE` mysql是否使用memcache进行数据缓冲,默认值是0（不启用）,启用memcache需要在部署服务器上搭建memcache环境(暂时取消该功能支持)  
`MEMCACHE_SET_ADDRESSL:ADDRESS`暂不使用  
`MEMCACHE_SET_ADDRESSL:CAPACITY`暂不使用  
`DATA_MATRIX_CONFIG:DATA_NAME` 当前数据源名称(多数据结构支持，亦支持分布式数据结构)  
`DATA_MATRIX_CONFIG:DATA_HOST` 服务访问地址  
`DATA_MATRIX_CONFIG:DATA_USER` 登录用户  
`DATA_MATRIX_CONFIG:DATA_PWD` 登录密码  
`DATA_MATRIX_CONFIG:DATA_PORT` 默认访问端口  
`DATA_MATRIX_CONFIG:DATA_DB` 访问数据库  

__缓存状态配置：__  
>`ROOT_USE_BUFFER` 缓存状态设置 默认值：`true` true：缓存文件机制启动，false：缓存文件机制关闭，不再生成新的缓存文件内容  
  
__访问显示模式配置：(`1.0版本后改配置暂时停用该功能，系统缓存文件默认30分钟过期`)__  
>`BUFFER_TYPE` 使用缓存器类型（0:不适用缓存器,1:使用数据缓存,2:生成php缓存文件,3:生成静态文件）  
`BUFFER_TIME` 缓存器生命周期（0:不设限制,内容发生变化,缓存器执行更新,大于0时以秒为时间单位进行周期更新）  

<span id='config_session'></span>
__会话配置：__   
>`SESSION:SAVE_PATH` session存储位置，一般php.ini设置,如果需要修改存储位置,再填写  
`SESSION:NAME` 指定会话名以用做 cookie 的名字.只能由字母数字组成，默认为 `PHPSESSID`  
`SESSION:SAVE_HANDLER` 定义了来存储和获取与会话关联的数据的处理器的名字.默认为 `files`  
`SESSION:AUTO_START` 指定会话模块是否在请求开始时自动启动一个会话.默认为 `0（不启动）`  
`SESSION:GC_PROBABILITY` 与 gc_divisor 合起来用来管理 gc（garbage collection 垃圾回收）进程启动的概率.默认为 `1`  
`SESSION:GC_DIVISOR` 与 gc_probability 合起来定义了在每个会话初始化时启动 gc（garbage collection 垃圾回收）进程的概率.默认为 `100`  
`SESSION:'GC_MAXLIFTTIME` 指定过了多少秒之后数据就会被视为“垃圾”并被清除,垃圾搜集可能会在 session 启动的时候开始  
`SESSION:SERIALIZE_HANDLER` 定义用来序列化／解序列化的处理器名字  
`SESSION:USE_STRICT_MODE`  
`SESSION:REFERER_CHECK` 用来检查每个 HTTP Referer 的子串,如果客户端发送了 Referer 信息但是在其中并未找到该子串,则嵌入的会话 ID 会被标记为无效,默认为`空字符串 ''`  
`SESSION:ENTROPY_FILE` 给出一个到外部资源（文件）的路径,在会话 ID 创建进程中被用作附加的熵值资源  
`SESSION:ENTROPY_LENGTH` 指定了从上面的文件中读取的字节数,默认为 `0`  
`SESSION:CACHE_LIMITER` 指定会话页面所使用的缓冲控制方法.默认为 `nocache`  
`SESSION:CACHE_EXPIRE` 以分钟数指定缓冲的会话页面的存活期,此设定对 nocache 缓冲控制方法无效,默认为 `180`  
`SESSION:USE_TRANS_SID` 指定是否启用透明 SID 支持.默认为 `0（禁用）`  
`SESSION:HASH_FUNCTION` 允许用户指定生成会话 ID 的散列算法.'0' 表示 MD5（128 位）,'1' 表示 SHA-1（160 位）  
`SESSION:HASH_BITS_PER_CHARACTER` 允许用户定义将二进制散列数据转换为可读的格式时每个字符存放多少个比特,可能值为 '4'（0-9，a-f）默认,'5'（0-9，a-v）,以及 '6'（0-9，a-z，A-Z，"-"，","）  
`COOKIE:COOKIE_LIFETIME` 以秒数指定了发送到浏览器的 cookie 的生命周期,值为 0 表示“直到关闭浏览器”,默认为 `0`  
`COOKIE:COOKIE_PATH` 指定了要设定会话 cookie 的路径,默认为`空字符串 ''`  
`COOKIE:COOKIE_DOMAIN` 指定了要设定会话 cookie 的域名,默认为`空字符串 ''`  
`COOKIE:COOKIE_SECURE` 指定是否仅通过安全连接发送 cookie,默认为 `off`  
`COOKIE:COOKIE_HTTPONLY`标记cookie，只有通过HTTP协议访问，这意味着饼干不会访问的脚本语言,比如JavaScript，这个设置可以有效地帮助降低身份盗窃XSS攻击,仅部分浏览器支持  
`COOKIE:USE_COOKIES` 指定是否在客户端用 cookie 来存放会话 ID,默认为 `1`  
`COOKIE:USE_ONLY_COOKIES` 指定是否在客户端仅仅使用 cookie 来存放会话 ID,启用此设定可以防止有关通过 URL 传递会话 ID 的攻击,默认值改为`1`  
