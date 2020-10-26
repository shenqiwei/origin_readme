## Redis string模块

#### 调用方式
> `$_str = $_redis->str()；`

#### 函数说明

> `$_str->create($key,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">创建元素对象值内容</td>
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
         <td colspan="3">从redis直接返回结果内容，返回值类型 boolean</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 

> `$_str->createSec($key,$value,$second)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">创建元素对象，并设置生命周期</td>
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
         <td>*</td>
         <td>$second</td>
         <td>int</td>
         <td>生命周期时间（second），默认值 0</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，，返回值类型 boolean</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 

> `$_str->createOnly($key,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">创建元素对象值内容</td>
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

> `$_str->createMil($key,$value,$milli)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">创建元素对象，并设置生命周期</td>
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
         <td>*</td>
         <td>$milli</td>
         <td>int</td>
         <td>生命周期时间（second），默认值 0</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3">从redis直接返回结果内容，返回值类型 boolean</td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">暂无</td>
     </tr>
  </table> 

> `$_str->get($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取元素对象内容</td>
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

> `$_str->append($key,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">叠加（创建）对象元素值内容</td>
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

> `$_str->cBit($key,$value,$offset)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">设置元素对象偏移值</td>
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
         <td>int</td>
         <td>元素对象内容值</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$offset</td>
         <td>int</td>
         <td>偏移系数</td>
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

> `$_str->gBit($key,$value)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">获取元素对象偏移值</td>
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
         <td>int</td>
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

> `$_str->getLen($key)`
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">检索元素对象值内容长度</td>
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

> `$_str->getRange($key,$start,$end)`：     
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">检索元素对象值（区间截取）内容，（大于0的整数从左开始执行，小于0的整数从右开始执行）</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$start</td>
         <td>int</td>
         <td>起始位置参数，默认值 1 </td>
     </tr>
     <tr>
         <td>*</td>
         <td>$end</td>
         <td>int1</td>
         <td>结束位置参数，默认值 -1</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3"></td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">application</td>
     </tr>
  </table> 

> `$_str->getRollback($key,$value)`：     
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">替换原有值内容，并返回原有值内容</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$value</td>
         <td>mixed 任意类型</td>
         <td>对象内容值</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3"></td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">application</td>
     </tr>
  </table> 
  
> `$_str->createList($columns)`：    
<table>
       <tr>
           <td>说明</td>
           <td colspan="3">创建元素列表</td>
       </tr>
       <tr>
           <td>*</td>
           <td>$columns</td>
           <td>array</td>
           <td>对应元素列表数组</td>
       </tr>
       <tr>
           <td>返回值</td>
           <td colspan="3"></td>
       </tr>
       <tr>
           <td>实例</td>
           <td colspan="3">application</td>
       </tr>
    </table> 

> `$_str->createListOnly($columns)`：      
<table>
      <tr>
          <td>说明</td>
          <td colspan="3">非替换创建元素列表</td>
      </tr>
      <tr>
          <td>*</td>
          <td>$columns</td>
          <td>array</td>
          <td>对应元素列表数组</td>
      </tr>
      <tr>
          <td>返回值</td>
          <td colspan="3"></td>
      </tr>
      <tr>
          <td>实例</td>
          <td colspan="3">application</td>
      </tr>
   </table> 

> `$_str->getList($keys)`：     
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">检索元素列表</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$keys</td>
         <td>array</td>
         <td>对应元素列表数组</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3"></td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">application</td>
     </tr>
  </table> 

> `$_str->plus($key,$increment)`：    
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">对应元素（数据）指定值自增</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$increment</td>
         <td>int</td>
         <td>自增系数值，默认值 1</td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3"></td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">application</td>
     </tr>
  </table>  

> `$_str->minus($key,$decrement)`：     
<table>
     <tr>
         <td>说明</td>
         <td colspan="3">对应元素（数据）指定值自减 </td>
     </tr>
     <tr>
         <td>*</td>
         <td>$key</td>
         <td>string</td>
         <td>对象键名</td>
     </tr>
     <tr>
         <td>*</td>
         <td>$increment</td>
         <td>int</td>
         <td>自减系数值，默认值 1 </td>
     </tr>
     <tr>
         <td>返回值</td>
         <td colspan="3"></td>
     </tr>
     <tr>
         <td>实例</td>
         <td colspan="3">application</td>
     </tr>
  </table>  