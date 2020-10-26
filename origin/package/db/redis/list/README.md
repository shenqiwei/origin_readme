## Redis list模块

#### 调用方式
> `$_list = $_redis->Lists()；`

#### 函数说明

> `$_list->removeFirst($keys,$time)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">移出并获取列表的第一个元素</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$keys</td>
         <td>array</td>
         <td>索引元素对象列表</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$time</td>
         <td>int</td>
         <td>最大等待时长</td>
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

> `$_list->removeLast($keys,$time)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取列表的最后一个元素</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$keys</td>
         <td>array</td>
         <td>索引元素对象列表</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$time</td>
         <td>int</td>
         <td>最大等待时长</td>
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

> `$_list->reIn($key,$write,$time)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">抽取元素对象值内容，转存至目标元素对象中</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$write</td>
         <td>string</td>
         <td>转存目标对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$time</td>
         <td>int</td>
         <td>最大等待时长</td>
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

> `$_list->index($key,$index)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">索引元素对象，并返回内容信息（大于0从左开始，小于0从右侧开始）</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$index</td>
         <td>int</td>
         <td>索引位置参数</td>
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

> `$_list->insert($key,$value,$write,$be)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">索引元素对象，并返回内容信息（大于0从左开始，小于0从右侧开始）</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed</td>
         <td>对象元素值</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$write</td>
         <td>mixed</td>
         <td>写入值</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$be</td>
         <td>string</td>
         <td>插入位置，默认值 after（后插入），before（前插入）</td>
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

> `$_list->count($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">返回列表的长度</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
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

> `$_list->popFirst($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">移除并返回列表的第一个元素</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
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

> `$_list->popLast($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">移除并返回列表的最后一个元素</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
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

> `$_list->popWrite($key,$write)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">将元素对象列表的最后一个元素移除并返回，并将该元素添加到另一个列表</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$write</td>
         <td>string</td>
         <td>写入元素对象键</td>
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

> `$_list->inFirst($key,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">在列表头部插入一个或多个值</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed</td>
         <td>写入元素对象值</td>
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

> `$_list->inLast($key,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">在列表尾部插入一个或多个值</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed</td>
         <td>写入元素对象值</td>
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

> `$_list->inFFirst($key,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">在已存在的列表头部插入一个值</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed</td>
         <td>写入元素对象值</td>
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

> `$_list->inFLast($key,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">在已存在的列表尾部插入一个值</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed</td>
         <td>写入元素对象值</td>
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

> `$_list->range($key,$start,$end)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">返回列表中指定区间内的元素</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$start</td>
         <td>int</td>
         <td>起始位置参数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$end</td>
         <td>int</td>
         <td>结束位置参数</td>
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

> `$_list->rem($key,$count,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">根据参数 COUNT 的值，移除列表中与参数 VALUE 相等的元素</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$count</td>
         <td>int</td>
         <td>执行(总数)系数 (count > 0: 从表头开始向表尾搜索,count < 0:从表尾开始向表头搜索，count = 0: 删除所有与value相同的)</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed</td>
         <td>操作值</td>
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

> `$_list->indexSet($key,$index,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">根据参数 COUNT 的值，移除列表中与参数 VALUE 相等的元素</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$index</td>
         <td>int</td>
         <td>索引系数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed</td>
         <td>操作值</td>
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

> `$_list->trim($key,$start,$end)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">保留指定区间内的元素</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>索引元素对象键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$start</td>
         <td>int</td>
         <td>起始位置参数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$end</td>
         <td>int</td>
         <td>结束位置参数</td>
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
