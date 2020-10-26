## Redis set模块

#### 调用方式
> `$_set = $_redis->Set()；`

#### 函数说明

> `$_set->add($key,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">集合：向集合添加一个或多个成员</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed 任意值</td>
         <td>元素对象内容值</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，返回值类型 int</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table>

> `$_set->count($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取集合内元素数量</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，返回值类型 int</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table>

> `$_set->diff($key,$second)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取两集合差值</td>
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
         <td>string</td>
         <td>比对元素对象键</td>
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

> `$_set->different($key,$second,$new)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取两集合之间的差值，并存入新集合中</td>
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
         <td>string</td>
         <td>比对元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$new</td>
         <td>string</td>
         <td>新集合元素对象</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，返回值类型 int</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table>

> `$_set->member($key,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">判断集合元素对象值是否存在元素对象中</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed 任意值</td>
         <td>元素对象内容值</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，返回值类型 int</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table>

> `$_set->reSet($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取两集合差值</td>
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

> `$_set->move($key,$second,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">元素对象集合值迁移至其他集合中</td>
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
         <td>string</td>
         <td>迁移集合对象</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed</td>
         <td>迁移值</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，返回值类型 int</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table>

> `$_set->pop($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">移除元素对象随机内容值</td>
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

> `$_set->randMember($key,$count)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">随机从元素对象中抽取指定数量元素内容值</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$count</td>
         <td>int</td>
         <td>随机抽调数量，默认值 1</td>
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

> `$_set->remove($key,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">移除元素对象中指定元素内容</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed 任意值</td>
         <td>元素对象内容值</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，返回值类型 int</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table>

> `$_set->merge($key,$second)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">移除元素对象中指定元素内容</td>
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
         <td>string</td>
         <td>索引元素对象键</td>
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

> `$_set->mergeTo($new,$key,$second)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">返回指定两个集合对象的并集</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$new</td>
         <td>string</td>
         <td>存储指向集合键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$second</td>
         <td>string</td>
         <td>索引元素对象键</td>
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

> `$_set->tree($key,$value,$cursor,$pattern)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">返回指定两个集合对象的并集</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>string</td>
         <td>索引值</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$cursor</td>
         <td>int</td>
         <td>执行标尺，默认值 0</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$pattern</td>
         <td>string</td>
         <td>操作参数，默认值 match</td>
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