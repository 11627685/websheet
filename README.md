# WebSheet

## 简介

WebSheet 是基于 HTML5 Canvas 和 JavaScript 开发的纯前端 xlsx 文件展示控件，着重于页面展示，主要实现了：文件导入 / 导出、文本展示、格式化文本、合并单元格、边框、底色、设置行列宽高、行列隐藏、视图锁定、基础表格、撤销 / 重做、快捷键、公式解析与计算等功能。支持自定义函数、单元格展示编辑以及右击菜单定制开发。

## 特性

- 三层架构，命令模式（Command）支持撤销重做
- 单元格合并、边框、填充色、数字格式（百分比 / 日期 / 千位分隔）
- 内置公式引擎50+ 函数
- 冻结行列、自动列宽、右键上下文菜单

## 快速开始

如果你是新手，可以从下面两篇文档入手，学习如何在纯 HTML 和 Vue 中加载 WebSheet、把控件渲染到页面，以及如何加载本地或网络上的 Excel 文件：

- [HTML 使用入门](http://wiki.websheet.cn/zh/HTML)
- [VUE 使用入门](http://wiki.websheet.cn/zh/VUE%E4%BD%BF%E7%94%A8)
- [打开文件](http://wiki.websheet.cn/zh/newfile)
- [文件导出](http://wiki.websheet.cn/zh/%E6%96%87%E4%BB%B6%E5%AF%BC%E5%87%BA)


## 快捷键

| 快捷键 | 功能说明 | 快捷键 | 功能说明 |
| ------- | ------- | ------- | ------- |
| Ctrl+O | 打开一个新文件 | Ctrl+X | 剪切 |
| Ctrl+C | 复制 | Ctrl+P | 粘贴 |
| Ctrl+Z | 撤销 | Ctrl+Y | 重做 |
| Ctrl+A | 全选 | Delete | 清除单元格值 |
| Ctrl+Shift+PageDown | 激活下一个 sheet | Ctrl+Shift+PageUp | 激活上一个 sheet |
| Ctrl+↑ | 视图切换到 sheet 开始行 | Ctrl+↓ | 视图切换到 sheet 结束行 |
| Ctrl+← | 视图切换到 sheet 开始列 | Ctrl+→ | 视图切换到 sheet 结束列 |
| Ctrl+E | 下载文件 | Ctrl+S | 下载文件 |
| Enter | 确认编辑并移动到下一个单元格 | Alt+鼠标滚轮 | 向左或右移动表格 |

## 进阶

如果你已了解该控件，想通过脚本动态控制其功能，可参考以下文档：

- [单元格](http://wiki.websheet.cn/zh/%E8%AE%BE%E7%BD%AE%E5%8D%95%E5%85%83%E6%A0%BC)
- [格式化单元格内容](http://wiki.websheet.cn/zh/%E6%A0%BC%E5%BC%8F%E5%8C%96%E5%8D%95%E5%85%83%E6%A0%BC%E5%86%85%E5%AE%B9)
- [行列设置及操作](http://wiki.websheet.cn/zh/%E8%A1%8C%E5%88%97%E8%AE%BE%E7%BD%AE%E5%8F%8A%E6%93%8D%E4%BD%9C)
- [sheet 操作](http://wiki.websheet.cn/zh/sheet%E6%93%8D%E4%BD%9C)
- [设置视图锁定（视图冻结）](http://wiki.websheet.cn/zh/%E8%AE%BE%E7%BD%AE%E8%A7%86%E5%9B%BE%E9%94%81%E5%AE%9A)
- [名称别名（名称管理）](http://wiki.websheet.cn/zh/%E5%90%8D%E7%A7%B0%E5%88%AB%E5%90%8D)
- [表格管理](http://wiki.websheet.cn/zh/table%E8%A1%A8%E6%A0%BC)
- [单元格编辑器](http://wiki.websheet.cn/zh/%E5%8D%95%E5%85%83%E6%A0%BC%E7%BC%96%E8%BE%91%E5%99%A8)
- [打印](http://wiki.websheet.cn/zh/%E6%89%93%E5%8D%B0)

> 待开发 / 远期规划：图片、过滤器、分组报表。

### 常用函数

| 函数名称 | 说明 | 例子 |
| :------- | ------- | ------- |
| SUM | 汇总函数 | SUM(A1:C1) |
| AVERAGE | 计算平均值 | AVERAGE(A1:C1) |
| IF | 条件函数 | IF(10>5,"Yes","No") |
| CONCATENATE | 链接函数 | CONCATENATE(text1,text2,[text3],...) |
| NOW | 当前系统日期及时间函数 | 参考 [日期时间格式化](http://wiki.websheet.cn/zh/%E6%A0%BC%E5%BC%8F%E5%8C%96%E5%8D%95%E5%85%83%E6%A0%BC%E5%86%85%E5%AE%B9#DataNow) |
| TRUNC | 截取函数 | TRUNC(3.141593) // 返回 3 |
| MAX | 获取最大值 | MAX(1,2,3) // 返回 3 |
| MIN | 获取最小值 | MIN(4,5,6,7,8) // 返回 4 |
| ROW | 返回当前行号 | ROW() // 返回当前行号 |

> 完整函数清单见 [函数清单](http://wiki.websheet.cn/zh/%E5%87%BD%E6%95%B0%E6%B8%85%E5%8D%95)。

### 常用事件

| 事件名称 | 说明 | 文档 |
| :------- | ------- | ------- |
| ActiveCellChange | 激活的单元格变化时触发 | [事件绑定](http://wiki.websheet.cn/zh/%E8%A1%A8%E6%A0%BC%E4%BA%8B%E4%BB%B6#ActiveCellChange) |
| SheetChange | 激活的 sheet 变化时触发 | [事件绑定](http://wiki.websheet.cn/zh/%E8%A1%A8%E6%A0%BC%E4%BA%8B%E4%BB%B6#SheetChange) |
| CellValueChage | 单元格值变化触发 | [事件绑定](http://wiki.websheet.cn/zh/%E8%A1%A8%E6%A0%BC%E4%BA%8B%E4%BB%B6#CellValueChage) |
| RowChange | 行增加删除时触发 | [事件绑定](http://wiki.websheet.cn/zh/%E8%A1%A8%E6%A0%BC%E4%BA%8B%E4%BB%B6#RowChange) |
| ColChange | 列增加删除时触发 | [事件绑定](http://wiki.websheet.cn/zh/%E8%A1%A8%E6%A0%BC%E4%BA%8B%E4%BB%B6#ColChange) |
| DocumentChange | 文件加载完成 | [事件绑定](http://wiki.websheet.cn/zh/%E8%A1%A8%E6%A0%BC%E4%BA%8B%E4%BB%B6#DocumentChange) |

> 更多事件见 [表格事件](http://wiki.websheet.cn/zh/%E8%A1%A8%E6%A0%BC%E4%BA%8B%E4%BB%B6)。

## 高级

- [自定义函数](http://wiki.websheet.cn/zh/%E8%87%AA%E5%AE%9A%E4%B9%89%E5%87%BD%E6%95%B0)
- [自定义展示控件](http://wiki.websheet.cn/zh/%E8%87%AA%E5%AE%9A%E4%B9%89%E5%B1%95%E7%A4%BA%E6%8E%A7%E4%BB%B6)
- [自定义右击菜单](http://wiki.websheet.cn/zh/%E8%87%AA%E5%AE%9A%E4%B9%89%E5%8F%B3%E5%87%BB%E8%8F%9C%E5%8D%95)

## 演示 Demo

所有展示代码及展示地址：[演示 demo](http://www.websheet.cn/xlsx/)

## 联系我们

- 邮箱：11627685@qq.com
- QQ 群：1036131666

## 应用效果

查看 [某集团公司应用效果图](http://wiki.websheet.cn/zh/%E5%BA%94%E7%94%A8%E6%95%88%E6%9E%9C)。

## 开源许可（License）

本项目以 **开源使用** 方式发布，采用 **MIT 许可证 + 水印保留条款**（详见 [LICENSE](./LICENSE)）。

- ✅ **允许**：个人 / 商业使用、二次开发、分发、再许可、销售。
- ✅ **无域名限制、无用途限制、无商业使用限制**。
- ⚠️ **唯一限制**：必须保留软件内置的**水印及防篡改机制**，不得移除、禁用或绕过。

> 简言之：除水印外，无任何其他限制。
