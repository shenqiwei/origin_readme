## Redis sequence模块

#### 调用方式
> `$_seq = $_redis->Sequence()；`

#### 函数说明

> `$_seq->add($key,$param,$value)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">序列增加元素对象内容值</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$param</td>
         <td>mixed</td>
         <td>标记</td>
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

> `$_seq->count($key)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">返回序列中元素对象内容数</td>
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

> `$_seq->mMCount($key,$min,$max)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">序列元素对象中区间值数量</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$min</td>
         <td>string</td>
         <td>最小区间数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$max</td>
         <td>string</td>
         <td>最大区间数</td>
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

> `$_seq->ai($key,$increment,$value)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">序列中元素对象值增加自增系数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$increment</td>
         <td>mixed</td>
         <td>自增系数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed</td>
         <td>值</td>
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

> `$_seq->different($new,$key,$param,$second)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">搜索两个序列指定系数成员内容，并存入新的序列中</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$new</td>
         <td>string</td>
         <td>目标序列键</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$param</td>
         <td>mixed</td>
         <td>索引系数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$second</td>
         <td>string</td>
         <td>比对索引对象键</td>
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

> `$_seq->dictCount($key,$min,$max)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">序列中字典区间值数量</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$min</td>
         <td>string</td>
         <td>最小区间系数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$max</td>
         <td>string</td>
         <td>最大区间系数</td>
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

> `$_seq->range($key,$min,$max)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">序列元素对象指定区间内容对象内容</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$min</td>
         <td>int</td>
         <td>最小区间系数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$max</td>
         <td>int</td>
         <td>最大区间系数</td>
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

> `$_seq->rdictRange($key,$min,$max)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">序列元素对象指定字典区间内容</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$min</td>
         <td>string</td>
         <td>最小区间系数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$max</td>
         <td>string</td>
         <td>最大区间系数</td>
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

> `$_seq->limitRange($key,$min,$max)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">序列元素对象指定分数区间内容</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$min</td>
         <td>int</td>
         <td>最小区间系数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$max</td>
         <td>int</td>
         <td>最大区间系数</td>
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

> `$_seq->index($key,$value)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">返回有序集合中指定成员的索引</td>
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
         <td>mixed</td>
         <td>值</td>
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

> `$_seq->remove($key,$value)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">移除有序集合中的一个成员</td>
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
         <td>mixed</td>
         <td>值</td>
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

> `$_seq->dictRemove($key,$start,$end)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">移除有序集合中给定的字典区间的所有成员</td>
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
         <td>string</td>
         <td>起始参数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$end</td>
         <td>string</td>
         <td>结尾参数</td>
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

> `$_seq->dictRank($key,$start,$end)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">移除有序集中，指定排名(rank)区间内的所有成员</td>
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
         <td>string</td>
         <td>起始参数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$end</td>
         <td>string</td>
         <td>结尾参数</td>
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

> `$_seq->dictScore($key,$min,$max)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">移除有序集中，指定分数（score）区间内的所有成员</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>检索对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$min</td>
         <td>int</td>
         <td>最小区间系数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$max</td>
         <td>int</td>
         <td>最大区间系数</td>
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

> `$_seq->descRange($key,$start,$end)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">返回有序集中，指定区间内的成员</td>
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
         <td>string</td>
         <td>起始参数</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$end</td>
         <td>string</td>
         <td>结尾参数</td>
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

> `$_seq->score($key,$value)`
<table style="width: 100px;">
     <tr>
         <td>说明</td>
         <td colspan="3">返回有序集中，成员的分数值</td>
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
         <td>mixed</td>
         <td>值</td>
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
