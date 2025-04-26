 ## 什么是WEBSHEET
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;websheet基于HTML5的CANVAS和JAVASCRIPT开发的纯前端xlsx文件展示控件，该控件着重的页面展示，主要完成了文件导入、导出、文本展示、格式化文本、合并单元格、边框、底色、设置行列宽度高度，行列隐藏、视图锁定、基础表格、撤销、重做、快捷键、公式的解析和计算等功能。支持自定义函数，单元格展示编辑和右击菜单定制开发。

---
# 一、入门
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;如果你是新手也不熟悉websheet，则可以从下面两篇文章入手，这些篇幅的内容将会教会你如何在纯HTML和VUE中加载websheet,如何把该控件渲染到你的页面上，以及如何加载本地或网络上的EXCEL文件。也可以在demo地址看到完整的可以使用的例子。


<center>  
  
|  <a target="_blank" href="http://wiki.websheet.cn/zh/HTML">HTML使用入门</a> |   <a target="_blank" href="http://wiki.websheet.cn/zh/VUE%E4%BD%BF%E7%94%A8">VUE使用入门 </a> |     <a target="_blank" href="http://wiki.websheet.cn/zh/newfile">打开文件</a> |  <a target="_blank" href="http://wiki.websheet.cn/zh/文件导出">文件导出</a>  |   
| ------- | ------- | ------- | ------- | 
 
</center> 
   
</center>
  
 ---   
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;目前支持的快捷键  
     
 <center>  
  
| 快捷键 | 功能说明 |   快捷键 | 功能说明 |   
| ------- | ------- | ------- | ------- | 
 |Ctrl+O | 打开一个新文件 | Ctrl+X  | 剪切  |
 |Ctrl+C | 复制|     Ctrl+P | 粘贴 | 
 |Ctrl+Z | 撤销 |   Ctrl+Y | 重做 | 
 |Ctrl+A | 全选 |   Delete   | 清除单元格值 | 
 |Ctrl+Shitf+PageDown | 激活下一个sheet|   Ctrl+Shitf+PageUp | 激活上一个sheet| 
 |Ctrl+↑| 试图切换到sheet开始行|   Ctrl+↓ | 试图切换到sheet结束行 |  
 |Ctrl+← | 试图切换到sheet开始列 |   Ctrl+→ | 试图切换到sheet结束列 |  
 |Enter | 确认编辑并向下一个单元格 |  Alt+鼠标滚轮   | 向左或右移动表格 |   
</center>

  
---

# 二、进阶
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;如果你对该控件已经有了解，想在自己项目中利用脚本动态控制该控件的部分功能，则可以了解以下篇幅内容，在以下篇幅将会了解到如何设置单元、如何删除、增加行列，设置行列的高度和宽度、监听websheet的事件以及使用已经支持的功能函数。


| <a target="_blank" href="http://wiki.websheet.cn/zh/设置单元格">单元格</a>  |   <a target="_blank" href="http://wiki.websheet.cn/zh/格式化单元格内容">格式化</a> | <a target="_blank" href="http://wiki.websheet.cn/zh/行列设置及操作">列和行</a> |  
| ------- | ------- | ------- | 

|  <a target="_blank" href="http://wiki.websheet.cn/zh/sheet操作">sheet操作</a> |    <a target="_blank" href="http://wiki.websheet.cn/zh/设置视图锁定">视图冻结</a>|     <a target="_blank" href="http://wiki.websheet.cn/zh/名称别名">名称管理</a> |  
| ------- | ------- | ------- | 

| <a target="_blank" href="http://wiki.websheet.cn/zh/table表格">表格管理</a>  |  <a target="_blank" href="http://wiki.websheet.cn/zh/单元格编辑器">编辑器</a> |      <a target="_blank" href="http://wiki.websheet.cn/zh/打印">&nbsp;打&nbsp;&nbsp;&nbsp;&nbsp;印</a>|  
| ------- | ------- | ------- | 
 
 
---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;目前支持的常用函数清单：

 <center>  
  
| 函数名称 | 说明 |  例子| 
| :------- | ------- |   ------- |
 |SUM | 汇总函数 | 汇总A1到C1单元格的值 SUM(A1:C1) |
 |IF | 条件函数  |  IF(10>5,"Yes","No")  | 
 |CONCATENATE| 链接 函数|    CONCATENATE(text1,text2,[text3],...)  |
 |NOW| 当前系统日期及时间函数 |  参考：  <a target="_blank" href="http://wiki.websheet.cn/zh/格式化单元格内容#DataNow">日期时间格式化</a> |
 |TRUNC| 截取函数 |    TRUNC(3.141593) // 返回 3 |
</center>


<right>
   <div class="link-container-right">
    <a target="_blank" href="http://wiki.websheet.cn/zh/函数清单">更多函数</a>
  </div>
</right>

---

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;目前支持常用事件清单见下面表格，绑定事件可以参考：<a target="_blank" href="http://wiki.websheet.cn/zh/表格事件">事件绑定</a>：


 <center>  
  
| 事件名称 | 说明 |  绑定链接| 
| :------- | ------- |   ------- |
 | ActiveCellChange| 激活的单元格变化时触发 |  <a target="_blank" href="http://wiki.websheet.cn/zh/表格事件#ActiveCellChange">事件绑定</a> |
 | SheetChange| 激活的sheet变化时触发 |   <a target="_blank" href="http://wiki.websheet.cn/zh/表格事件#SheetChange">事件绑定</a> |
 | CellValueChage|单元格值变化触发 | <a target="_blank" href="http://wiki.websheet.cn/zh/表格事件#CellValueChage">事件绑定</a>   | 
 | RowChange| 行增加删除时触发 |   <a target="_blank" href="http://wiki.websheet.cn/zh/表格事件#RowChange">事件绑定</a>  |
 | ColChange| 列增加删除时触发 |   <a target="_blank" href="http://wiki.websheet.cn/zh/表格事件#ColChange">事件绑定</a>  |
 | DocumentChange| 文件加载完成 |   <a target="_blank" href="http://wiki.websheet.cn/zh/表格事件#DocumentChange">事件绑定</a>  |  
 

</center>

<right>
   <div class="link-container-right">
    <a target="_blank" href="http://wiki.websheet.cn/zh/表格事件">更多事件</a>
  </div>
</right>

---

# 三、高级
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;该部分篇幅允许你对websheet的功能进行扩展。比如如何在websheet内展示你的控件，使用你自定义的功能函数以及交互中的右击菜单。

|  <a target="_blank" href="http://wiki.websheet.cn/zh/%E8%87%AA%E5%AE%9A%E4%B9%89%E5%87%BD%E6%95%B0">自定义函数</a> |      <a target="_blank" href="http://wiki.websheet.cn/zh/%E8%87%AA%E5%AE%9A%E4%B9%89%E5%B1%95%E7%A4%BA%E6%8E%A7%E4%BB%B6">自定义展示控件</a> |       <a target="_blank" href="http://wiki.websheet.cn/zh/自定义右击菜单">自定义右击菜单</a> |     
| ------- | ------- | ------- |  

 
 ---
# 四、在线代码

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 所有展现代码及展示地址： <a target="_blank" href="http://www.websheet.cn/xlsx/">演示demo</a>

---
# 五、关于版权
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;未经允许禁止用于商业用途。
  
---
  
# 六、联系我们
  
  邮箱地址：11627685@qq.com
  QQ群：1036131666
  
---
  
 
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b4750942416441b484dc288669f6aa23.png =200x200)


