## Redis hash模块

#### 调用方式
> `$_hash = $_redis->Hash()；`

#### 函数说明

> `$_set->create($key,$field,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">创建hash元素对象内容</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$field</td>
         <td>string</td>
         <td>hash对象字段名(域)</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed</td>
         <td>内容值</td>
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

> `$_set->createList($key,$array)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">创建hash元素对象列表</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$array</td>
         <td>array</td>
         <td>字段数组列表</td>
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

> `$_set->createNE($key,$field,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">非替换创建hash元素对象内容</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$field</td>
         <td>string</td>
         <td>hash对象字段名(域)</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed</td>
         <td>内容值</td>
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

> `$_set->get($key,$field)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取hash元素对象内容</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$field</td>
         <td>string</td>
         <td>hash对象字段名(域)</td>
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

> `$_set->lists($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">返回hash元素对象列表</td>
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

> `$_set->getList($key,$fields)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取hash元素对象内容</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$fields</td>
         <td>array</td>
         <td>字段数组列表</td>
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

> `$_set->limit($key,$start,$pattern,$count)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取hash元素对象区间列表内容(用于redis翻页功能)</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$start</td>
         <td>int</td>
         <td>起始位置标记</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$pattern</td>
         <td>string</td>
         <td>执行模板(搜索模板)</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$count</td>
         <td>int</td>
         <td>显示总数</td>
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

> `$_set->values($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">返回hash元素对象列表</td>
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

> `$_set->del($key,$field)`
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
         <td>*</td>
         <td>$field</td>
         <td>string</td>
         <td>hash对象字段名(域)</td>
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

> `$_set->plus($key,$field,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">设置hash元素对象增量值</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$field</td>
         <td>array</td>
         <td>hash对象字段名(域)</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>int</td>
         <td>字段数组列表</td>
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

> `$_set->fields($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取hash元素对象全部字段名(域)</td>
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

> `$_set->len($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取hash元素对象字段内容（域）长度</td>
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
