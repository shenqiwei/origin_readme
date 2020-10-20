## .htaccess 配置 [<a href="https://github.com/shenqiwei/origin_readme">返回</a>]
origin ver 1.0使用地址重写协议，如需要应用，可以复制粘贴。
  
    <IfModule mod_rewrite.c>    
    Options +FollowSymlinks
          RewriteEngine On    
          RewriteCond %{REQUEST_FILENAME} !-d    
          RewriteCond %{REQUEST_FILENAME} !-f    
          RewriteRule ^(.*)$ index.php/$1 [QSA,PT,L]    
    </IfModule>    