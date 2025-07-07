

## What is WEBSHEET
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Websheet is a pure front-end xlsx file display control developed based on HTML5 CANVAS and JAVASCRIPT. This control focuses on page display and mainly implements functions including file import/export, text display, formatted text, merged cells, borders, background colors, setting row/column width/height, hiding rows/columns, view locking, basic tables, undo/redo, keyboard shortcuts, formula parsing and calculation. It supports custom functions, cell display/editing, and right-click menu customization.


##  Translations

 <a target="_blank" href="https://github.com/11627685/websheet/blob/main/README_zh.md">中文文档</a>

##  homepage
 <a target="_blank" href="http://wiki.websheet.cn/zh/home">主页</a>
 <p>
 <a target="_blank" href="http://wiki.websheet.cn/en/home">homepage</a>
 
---
# 1. Getting Started
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;If you're new to Websheet, you can start with the following two articles. These will teach you how to load Websheet in pure HTML and VUE, how to render the control on your page, and how to load local or online EXCEL files. You can also see complete, usable examples at the demo address.
<center>
   <div class="link-container">
    <a target="_blank" href="http://wiki.websheet.cn/en/htmlusage">HTML Getting Started</a>
    <a target="_blank" href="http://wiki.websheet.cn/en/vueUsage">VUE Getting Started
       <a target="_blank" href="http://wiki.websheet.cn/en/OpenFile">Open File</a>
       <a target="_blank" href="http://wiki.websheet.cn/en/FileExport">Export File</a> 
  </div>
     
</center>
  
 ---   
     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Currently supported shortcuts  
     
 <center>  
  
| Shortcut | Function |   Shortcut | Function |   
| ------- | ------- | ------- | ------- | 
 |Ctrl+O | Open new file | Ctrl+X  | Cut  |
 |Ctrl+C | Copy|     Ctrl+P | Paste | 
 |Ctrl+Z | Undo |   Ctrl+Y | Redo | 
 |Ctrl+A | Select All |   Delete   | Clear cell value | 
 |Ctrl+Shitf+PageDown | Activate next sheet|   Ctrl+Shitf+PageUp | Activate previous sheet| 
 |Ctrl+↑| View switches to sheet start row|   Ctrl+↓ | View switches to sheet end row |  
 |Ctrl+← | View switches to sheet start column |   Ctrl+→ | View switches to sheet end column |  
 |Enter | Confirm edit and move to next cell |  Alt+Mouse Wheel   | Move table left/right |   
</center>

  
---

# 2. Intermediate
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;If you're already familiar with the control and want to dynamically control some of its functions in your project using scripts, you can learn about the following content. These sections will cover how to set cells, add/delete rows/columns, set row/column height/width, listen to Websheet events, and use supported functions.
<center>
   
  |  <a target="_blank" href="http://wiki.websheet.cn/en/CellEDITOR">Cells</a> |  <a target="_blank" href="http://wiki.websheet.cn/en/Fromat">Formatting</a> |     <a target="_blank" href="http://wiki.websheet.cn/en/RowandRow-Settings">Columns & Rows</a> | 
|------- | ------- | ------- |  
  
 |  <a target="_blank" href="http://wiki.websheet.cn/en/SheetOperation">Sheet Operations</a> |   <a target="_blank" href="http://wiki.websheet.cn/en/ViewLock">View Freeze</a> |      <a target="_blank" href="http://wiki.websheet.cn/en/Names">Name Management</a>| 
| ------- | ------- | ------- |  
  
   |  <a target="_blank" href="http://wiki.websheet.cn/en/table">Table Management</a>  |   <a target="_blank" href="http://wiki.websheet.cn/en/CellEDITOR">Editor</a> |       <a target="_blank" href="http://wiki.websheet.cn/en/print">Print</a> | 
| ------- | ------- | ------- |  
   
 

</center>

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Upcoming features and development order:
  <center>
   <div class="link-container"> 
  </div>
</center>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Long-term:
  <center>
   <div class="link-container">
      <span target="_blank" href="./"> Images</span>
     <span   target="_blank" href="./">Filters</span>
     <span target="_blank" href="./">Grouped Reports</span>
  </div>
</center>

  
---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Currently supported common functions:

 <center>  
  
| Function | Description |  Example| 
| :------- | ------- |   ------- |
 |SUM | Sum function | Sum values from A1 to C1: SUM(A1:C1) |
 |IF | Conditional function  |  IF(10>5,"Yes","No")  | 
 |CONCATENATE| Concatenation function|    CONCATENATE(text1,text2,[text3],...)  |
 |NOW| Current system date/time function |  Reference:  <a target="_blank" href="http://wiki.websheet.cn/en/Fromat#DataNow">DateTime Formatting</a> |
 |TRUNC| Truncation function |    TRUNC(3.141593) // returns 3 |
</center>


<right>
   <div class="link-container-right">
    <a target="_blank" href="http://wiki.websheet.cn/en/FunctionOrFormula">More Functions</a>
  </div>
</right>

---

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Currently supported common events are listed below. For event binding, refer to: <a target="_blank" href="http://wiki.websheet.cn/en/EventList">Event Binding</a>:


 <center>  
  
| Event | Description |  Binding Link| 
| :------- | ------- |   ------- |
 | ActiveCellChange| Triggered when active cell changes |  <a target="_blank" href="http://wiki.websheet.cn/en/EventList#ActiveCellChange">Event Binding</a> |
 | SheetChange| Triggered when active sheet changes |   <a target="_blank" href="http://wiki.websheet.cn/en/EventList#SheetChange">Event Binding</a> |
 | CellValueChage|Triggered when cell value changes | <a target="_blank" href="http://wiki.websheet.cn/en/EventList#CellValueChage">Event Binding</a>   | 
 | RowChange| Triggered when rows are added/deleted |   <a target="_blank" href="http://wiki.websheet.cn/en/EventList#RowChange">Event Binding</a>  |
 | ColChange| Triggered when columns are added/deleted |   <a target="_blank" href="http://wiki.websheet.cn/en/EventList#ColChange">Event Binding</a>  |
 | DocumentChange| Triggered when file loading completes |   <a target="_blank" href="http://wiki.websheet.cn/en/EventList#DocumentChange">Event Binding</a>  |  
  
   
  
</center>
 
 
  
<right>
   <div class="link-container-right">
    <a target="_blank" href="http://wiki.websheet.cn/en/EventList">More Events</a>
  </div>
</right>

---

# 3. Advanced
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This section allows you to extend Websheet's functionality, such as displaying your controls within Websheet, using your custom functions, and customizing the right-click menu in interactions.
 <center>
   <div class="link-container">
    <a target="_blank" href="http://wiki.websheet.cn/en/CustomFunctionsOrFormulas">Custom Functions</a>
    <a target="_blank" href="http://wiki.websheet.cn/en/CustomDisplayControl">Custom Display Controls</a>
     <a target="_blank" href="http://wiki.websheet.cn/en/CustomizeRightClickMenu">Custom Right-Click Menu</a>
    
  </div>
</center>

---
# 4. Online Code

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; All demo code and display address: <a target="_blank" href="http://www.websheet.cn/xlsx/">Demo</a>
# 5. About Copyright
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;localhost is free.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Commercial use is prohibited without permission.
  
---
  
# 6. Contact Us
  
  Email: 11627685@qq.com
  QQ Group: 1036131666
  
---
  
  <center>
  
![biglogo.png](/biglogo.png =200x200)
</center>
