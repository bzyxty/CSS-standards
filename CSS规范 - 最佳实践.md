## CSS规范 - 最佳实践

#### 最佳选择器写法（模块）
```
/* 这是某个模块 */
.m-nav{}/* 模块容器（基类） */
.m-nav li,.m-nav a{}/* 先共性  优化组合 */
.m-nav li{}/* 后个性  语义化标签选择器 */
.m-nav a{}/* 后个性中的共性 按结构顺序 */
.m-nav a.a1{}/* 后个性中的个性 */
.m-nav a.a2{}/* 后个性中的个性 */
.m-nav .z-crt a{}/* 交互状态变化 */
.m-nav .z-crt a.a1{}
.m-nav .z-crt a.a2{}
.m-nav .btn{}/* 典型后代选择器 */
.m-nav .btn-1{}/* 典型后代选择器扩展 */
.m-nav .m-sch{}/* 控制内部其他模块位置 */
.m-nav .u-sel{}/* 控制内部其他元件位置 */
.m-nav-1{}/* 模块扩展 */
.m-nav-1 li{}

.m-nav2/* 这是完全不同的模块（基类） */
.m-nav2-1/* 这是完全不同模块的拓展 */
```

#### 统一语义理解和命名
> 命名的最佳实践是简洁、便于理解，在自己和他人维护时能够很容易理解
###### 布局（.g-）
语义 | 命名
---|---
文档 | doc
头部 | head
主体 | body	
尾部 | foot	
主栏 | main	
主栏子容器 | mainc	
侧栏 | side	
侧栏子容器 | sidec	
盒容器 | wrap/box

###### 模块（.m-）、元件（.u-）
语义|	命名
---|---
导航	|nav	
子导航	|subnav	
面包屑	|crumb	
菜单	|menu
选项卡	|tab	
标题区	|head/title	
内容区	|body/content	
列表	|list
表格	|table
表单	|form	
热点	|hot	
排行	|top	
登录	|login	
标志	|logo	
广告	|advertise
搜索	|search
幻灯	|slide	
提示	|tips	
帮助	|help	
新闻	|news
下载	|download
注册	|regist	
投票	|vote
版权	|copyright	
结果	|result	
标题	|title	
按钮	|button	
输入	|input	

###### 功能（.f-）
语义|	命名|	简写|	
---|---|---|---
浮动清除	|clearboth	|cb
向左浮动	|floatleft	|fl	
向右浮动	|floatright	|fr
内联块级	|inlineblock	|ib	
文本居中	|textaligncenter	|tac	
文本居右	|textalignright	|tar	
文本居左	|textalignleft	|tal	
垂直居中	|verticalalignmiddle	|vam	
溢出隐藏	|overflowhidden	|oh
完全消失	|displaynone	|dn	
字体大小	|fontsize	|fs	
字体粗细	|fontweight	|fw
相对定位    |absolute   |abs
绝对定位    |relative   |rlt
固定定位    |fixed  |fixed

###### 皮肤（.s-）
语义|	命名|	简写|
---|---|---
字体颜色	|fontcolor|fc	
背景	|background	|bg
背景颜色	|backgroundcolor|bgc	
背景图片	|backgroundimage	|bgi
背景定位	|backgroundposition	|bgp
边框颜色	|bordercolor	|bc

###### 状态（.z-）
语义|	命名
---|---
选中	|selected	
当前	|current/active	
显示	|show	
隐藏	|hide	
打开	|open	
关闭	|close	
出错	|error	
不可用	|disabled