## Origin 应用目录[<a href="https://github.com/shenqiwei/origin_readme">返回</a>]

#### 快速通道
<table>
    <tr>
        <th align="left">快速访问 -- menu</th>
    </tr>
    <tr>
        <td><a href="#common">全局公共函数</a> -- common</td>
    </tr>
    <tr>
        <td><a href="#home">默认访问单元</a> -- home</td>
    </tr>
</table>

## common目录
Origin ver 1.0版本Common仅保留用于函数挂在和链接的public.php文件，其文件中编写或引入的函数，相应范围为整个应用结构 

## home目录
home目录为预设默认访问指向目录，其指向地址和名称，可以在origin入口文件中进行修改，也可以通过修改根目录中的index.php文件常量值实现变更
> classes:应用类目录，类需编写命名空间（namespace application/home/classes;），home可以替换成其他自定义目录名称，目录中结构与home结构一致其命名规则相同。    
    
    实例文件地址（application/home/classes/Index.php）
    namespace Application\Home\Classes;
    
    use Origin\Package\Unit;
    
    class Index extends Unit
    {
        function __construct()
        {
            parent::__construct();
            $this->param('title','origin framework');
        }
    
        function index()
        {
            $welcomes = array(
                array('statement' => '感谢使用Origin ver 1.0'),
                array('statement' => 'Origin已经完成结构初始化，日志地址（common/log/initialize/initialize.log）'),
                array('statement' => '若需要重新初始化，请删除application、common、resource文件夹并刷新浏览器'),
                array('statement' => 'Origin的部分功能需要独立安装插件，请在使用前根据跟人需要进行匹配安装'),
                array('statement' => 'Github地址：https://github.com/shenqiwei/origin_framework'),
                array('statement' => '说明文档地址：https://github.com/shenqiwei/origin_readme'),
            );
            $this->param("welcome",$welcomes);
            $this->param("year",date("Y"));
            $this->template();
        }
    }
    
> common：应用内公共函数目录，origin默认创建一个public.php文件，功能用途与全局公共函数文件一致，但其作用范围只在home目录下。    
> template：视图模板目录，其结构表述（template/index/index.html）:(template/类名/方法名.html)文件名小写     

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>{$title}</title>
        <style>
            html,body{ background-color: #115990; height: 100%; top:0; left: 0; padding: 0; margin: 0; color: #ffffff; }
            .main{ width:40rem; }
            .orange{ width: 4rem; font-size:4rem; padding:1rem 0 0 1rem; }
            .o{ background-color: #009999; border-radius: 0.5rem; filter:alpha(opacity=94); -moz-opacity:0.94; opacity:0.94; }
            .list ul li{ line-height: 1.5rem; }
            .mark{ clear:both; list-style: none; line-height: 4rem; font-size:1rem; text-align: right; }
        </style>
    </head>
    <body>
    <div class="main">
        <div class="orange"><span class="o">O</span>rigin.</div>
        <div class="list">
            <ul>
                <for operation="$welcome">
                <li>{$welcome.statement}</li>
                </for>
            </ul>
        </div>
        <div class="mark">origin framework {$year}.</div>
    </div>
    </body>
    </html>