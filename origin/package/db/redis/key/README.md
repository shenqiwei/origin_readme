## Redis key模块

#### 调用方式
> `$_key = $_redis->key()；`

#### 函数说明

> `$_key->del($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">删除元素对象内容</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，如果访问失败则返回false</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 
  
> `$_key->dump($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">序列化元素对象内容</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，如果访问失败或nil内容则返回 null</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 
  
> `$_key->setTSC($key,$timestamp)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">使用时间戳设置元素对象生命周期</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$timestamp</td>
         <td>int</td>
         <td>时间戳</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 
  
> `$_key->setSec($key,$second)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">使用秒计时单位设置元素对象生命周期</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$second</td>
         <td>int</td>
         <td>以秒为基本计算单位的时间长度</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 
  
> `$_key->setTSM($key,$timestamp)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">使用毫秒时间戳设置元素对象生命周期</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$timestamp</td>
         <td>int</td>
         <td>时间戳</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 
  
> `$_key->setMil($key,$millisecond)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">使用毫秒时间戳设置元素对象生命周期</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$millisecond</td>
         <td>int</td>
         <td>以毫秒为基本计算单位的时间长度</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 
  
 > `$_key->setMil($key,$millisecond)`
 <table>
      <tr>
          <td>说明</td>
          <td colspan="3">使用毫秒时间戳设置元素对象生命周期</td>
      </tr>
      <tr>
          <td>*</td>
          <td>$key</td>
          <td>string</td>
          <td>检索对象键名</td>
      </tr>
      <tr>
          <td>*</td>
          <td>$millisecond</td>
          <td>int</td>
          <td>以毫秒为基本计算单位的时间长度</td>
      </tr>
      <tr>
          <td>返回值</td>
          <td colspan="3">从redis直接返回结果内容</td>
      </tr>
      <tr>
          <td>实例</td>
          <td colspan="3">暂无</td>
      </tr>
   </table> 
   
> `$_key->rmCycle($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">移除元素目标生命周期限制</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，可作为boolean值判定</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 
  
> `$_key->remaining($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取元素对象剩余周期时间(毫秒)</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，int型</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 
  
> `$_key->remain($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取元素对象剩余周期时间(秒)</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，int型</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 
  
> `$_key->keys($closeKey)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取搜索相近元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$closeKey</td>
         <td>string</td>
         <td>相近元素对象（key*）</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，如果访问失败或nil内容则返回 null</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 
  
> `$_key->randKey()`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">随机返回元素键</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，如果访问失败或nil内容则返回 null</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 

> `$_key->rnKey($key,$newKey)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">重命名元素对象</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$Key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$newKey</td>
         <td>string</td>
         <td>新命名</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，可作为boolean值判定</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table>
  
> `$_key->irnKey($key,$newKey)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">非重名元素对象重命名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$Key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$newKey</td>
         <td>string</td>
         <td>新命名</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，可作为boolean值判定</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table>

> `$_key->type($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取元素对象内容数据类型</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$Key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，返回值类型 string，如果访问失败或nil内容则返回 null</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table>

> `$_key->inDB($key,$database)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">将元素对象存入数据库</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$Key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$database</td>
         <td>string</td>
         <td>对象数据库名</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，可作为boolean值判定</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table>
