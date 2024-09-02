<>里面放单词，
strong表加粗  eg:<strong>内容</strong>
网页固定结构
<html>网页整体
   <head>网页头部
     <title>网页标题</title>
   </head>
   <body>
   网页主题内容
   </body>
</html>
vscode输入“！”回车出格式
注释 ctrl+/
标签由<>/英文字母或单词组成
有开始有结束双标签，其他为单
嵌套关系，并列关系
标题标签
h系列，h1到h6依次递减，输h1
段落标签
p，独占一行，两段间有缝
换行
br，强制换行
水平线标签
hr
文本格式化标签（下划，加粗，倾斜，删除线等）
b\strong 加粗
u\ins 下划线
i\em 倾斜
s\del删除线
语义，
媒体标签（音频，视频，图片）
图片标签
img+标签属性
./选择路径，可以有多个属性，无序
src后原本图片，alt替换文本（原图片不显示）
title，鼠标悬停时提示字，不止在图片
width,height宽度和高度，只设置一个会等比例缩放
路径（页面加载图片，先找图片）
绝对路径（了解）：盘符开始
相对路径（常用）：从当前文件开始找目标文件：同级别：法一：图片名。法二：./图片名
下级：文件夹/目标图片.
上级：../(一级)文件夹名/图片名
音频：audio./音乐文件名。目前支持三种格式：多用mp3
src:路径。controls:显示播放控件。autoplay:自动播放（部分浏览器不支持）。loop：循环播放。
视频标签：video controls autoplay(谷歌需要配合muted实现静音播放) loop 支持：mp4
链接标签：<a 链接/路径，可改颜色
target:控制目标网页打开形式。 +_blank(保留原网页)/+_self(不保留原网页)
列表标签：按行展示相关的内容，分无序列表，有序列表，自定义列表
无序列表：ul：表示无序整体，只能包含li  li：无序列表中的每一行，可包含任何内容
有序列表：有顺序之分。ol:表整体。li：有序的每一行
自定义列表：网页底部自定义表现。dl：自定义列表整体（只有dd，dt）。dt：自定义列表主题。dd：默认缩进。
表格标签：table：表格整体（包tr）。tr：每行（包td）。td：表格单元格。
表格属性：border：边框宽度。width：表格宽。height：表格高。（实际开发推荐css）
表格标题和表头单元格标签：整体大标题和一列小标题。caption：表格大标题，默认居中。th：通常表格第一行加粗
表格结构标签：thead：表格头部。tbody：表格主体。tfoot：表格底部。
合并单元格：1.明确合并哪个。2.上下合并保留最上，左右合并保留最左。3.保留的单元格加代码，rowspan（跨行）属性：合并的个数，colspan（跨列）：属性：合并的个数。
同一个结构才能合并，不能跨（thead，tbody）。
表单标签：
1.input:根据type属性不同，效果不同. placeholder：占位符，提示输入内容。
text:单行文本，文本框。password：密码框。radio：单选框。name:相同属性为一组。checked:默认选中checkbox:多选框.file:文件选择，提交  mutiply 多个。submit:提交按钮。reset:重置按钮.button:默认无功能，与js添加功能,可加submit，reset.
select:下拉菜单整体。option：下拉菜单的部分。selected:默认选中
文本域：textarea，实际开发样式用css
lable标签:1.lable把内容包起来。表单标签加id属性。lable标签for属性设置对应id值
2.lable把内容和表单包起来。删除lable的for
语义化标签:
div,span:无任何语义
有语义的标签（了解）：header:网页头部。nav:网页导航。footer：网页底部。aside：网页侧边栏。section：网页区块。
artical：网页文章。（手机端）
字符实体：空格：&nbsp；


CSS
写在哪：内嵌式：在style标签里，style一般在head里，title下面.选择器（查找属性）{}
外联式：写在单独一个css文件中，link引入（项目）
行内式：写在标签style属性（配合js）

选择器：标签{}，所有标签生效
类选择器：类名{}定义“.类名”（只有数字，字母，下划线，中划线，不能数字或中划线开头），多个类名用空格隔开
id选择器：#id属性值{} id只有一个，不能重复（js）
通配符选择器：*{}选所有标签，清除margin，padding
文字样式：字体大小：font-size （数字加px），默认16。font-weight：100-900（400正常（normal），700加粗（bold）） 是否倾斜：font-style：normal（正常），italic（倾斜）
字体：font-family
样式层叠：同一个标签相同属性，会覆盖。
font简写:font:style size/line-height weight
文本样式：文本缩进:text-indent +数字px或em:一个字的大小
文本水平对齐方式:text-align 左对齐left 右对齐right居中center,图片也可以
文本修饰:text-decoration下划线underline 删除线line-through overline 上划线 无装饰线none
行高:line-height :数字px 或倍数
颜色：文字color 背景background
标签居中：margin：0 auto；实现
选择器进阶：
后代选择器：选择器1 选择器2{}
子代选择器：选择器1 >选择器2{}
并集选择器： 选择器1，选择器2{}
交集选择器：选择器选择器
hover伪类选择器:鼠标悬停的状态 选择器：hover
emmet语法：快速生成代码
背景相关属性：
背景颜色：background-color
背景图片：background-image
背景平铺：background-repeat水平 no-repeat不平铺 repeat -x/y 沿x或y铺
背景位置：background-position 取值：水平left center right 垂直：center bottom 数字px 左上角（0 0），x水平向右，y水平向左
背景相关属性连写
产品重要的img
不重要的div background 
元素显示模式：
块级元素：独占一行，可以设置宽高，默认和父级一样大
行内元素：一行多个，宽高默认由内容撑，不能设置宽高
行内块元素：一行多个，可以设置宽高，img，input，textarea
元素显示模式转换：
转块：display：block
行内块：display:inline-block
行内：display:inline
html嵌套注意:块一般做容器，p不能套div，h，p
a可以嵌套任何，不能a
继承性：文字都可以继承，生效自己的颜色（超链接）
层叠性：
优先级：i继承最低，
上一行出错，下一行受影响
盒子模型：标签/网页元素的矩形区域
内容区域：宽度和高度width 和height，数字px，
内边距区域：padding可以做复合属性，1：四个方向，4：顺时针，3；上，左右，下 ，2：上下，左右
边框区域：border 粗细 线条样式 颜色（无序），，取值空格隔开，实线solid，虚线dashed 点线dotted，border-方位（单独一个方向）
外边距区域
自动内减：box-sizing:border-box(加了border和padding不需要手动)
清除默认内外边距：margin
板心：margin 0 auto
去列表符号：list-style none；
外边距折叠问题，垂直布局块，上下margin会合并，最终为margin最大值，只给一个设
互相嵌套的块，子类的marging-top会影响父类，可以给父级设置overflow：hidden（专业），转换成行内块，设置浮动
行内元素的内外边距问题：想要通过margin padding改变行内标签垂直位置，无法生效，line-height
结构伪类选择器：根据元素的结构关系查找。第一个：first-child{}。最后一个：last-child。nth-child（n）{}第n个
nth-last-child（n）{}：倒数第n个
n偶数：2n，even 奇数：2n-1，2n+1，odd 前5个-n+5
伪元素：装饰小图，content加内容，：：before前面，：：after后面
1标准流：标签默认排版规则
2浮动：
作用：现代网页布局，块在一行排。以前图文环绕 float
特点：1脱离标准流，不占标准流位置。2浮动比标准流高半个级别，可覆盖元素，3下一个浮动在上一个左右浮动。4可以设置宽高，在一横排，有行内块特点。
注意：不能通过margin 0 auto； text align center居中
css书写顺序：1浮动或dispaly。2盒子模型相关：margin border pading 宽高背景。3文字样式
清除浮动：浮动给别的带来的影响。1直接加高度。2额外加标签：clear：both。3单伪元素清除法：：after。4双伪元素清除法。.clearfix::before,.clearfix::after{content:'';display:table;}.clearfix::after{clear:both}
5直接给父元素加overflow:hidden
3定位：属性名：position。偏移值：水平：left/right 垂直：top/bottom+数字px
相对定位：position：relative，占有原来的位置，仍具备标签原有的显示模式特点，相对原来位置移动，四个都有，先左上
绝对定位：position：absolute；先找已经定位的父级，如果有以此为参照物，没有以浏览器窗口为参照物。脱标，不占位，改变标签显示模式的特点（一行共存，宽高生效），就近找定位的父级，绝对定位的盒子不能使用margin auto居中
left50%整个盒子浏览器中间偏右，margin-left盒子向左侧移动自己宽度的一半
绝对定位的盒子现实模式有行内块的特点，，加宽高生效，如果没宽度和内容，宽度尺寸为0
固定定位：脱标，不占位置，改位置参考浏览器窗口
元素层级关系：
基线：浏览器文字排版中用于对齐的线
垂直对齐：vertical-align 顶部top 中间middle 底部bottom 水平text-align 都图片当作文字处理
光标类型：属性cursor pointer 可点击 text文本，可复制  move可以移动
边框圆角：属性border-radius 数字+px/百分比（半径），左上角顺时针，没有看对角
正圆：盒子为正方形，边框圆角为宽高一半或50%
胶囊：盒子长方形，边框圆角为一半
overflow溢出部分显示，hidden溢出隐藏，scroll无论是否溢出，显示滚动条，auto根据是否溢出是否显示滚动条
元素本身隐藏：1visibility：hidden 2display： none（不占位）
opacity： 0-1让元素整体变透明
精灵图：多张图合并为一张大图
1创造一个盒子，盒子尺寸和小图尺寸相同
2精灵图设置为盒子背景图
3修改位置background position：x y向左取负，向上取正
背景图片大小：background-size：宽度 高度；数字px/百分比/contain（等比，不超盒子）/cover（刚好填满盒子，可能显示不全）
盒子阴影；box-shadow：h-shadow（水平）y-shadow（垂直）blur（模糊）spread（阴影扩大）color（颜色）inset（内部）
过渡：transition，配合hover，谁变化谁加过度，transition： 变化（all全部）  数字s
!DOCTYPE html文档类型声明
lang=语言zh-CN中文
meta charset网页字符编码
seo：搜索引擎优化
 三大标签：title网页标题标签 description网页描述标签 keywards网页关键词标签
ico图标：link：favicon浏览器标题栏图标



进阶
字体图标：实现网页简洁图标效果，展示图标，本质是字体，处理简单颜色单一的图
使用：下载字体包（iconfont），使用字体图标
引入字体图标样式表，iconfont.css，调用图标对应的类名
图标库没有所需图标，上传svg矢量图
平面转换：使用transform实现位移，旋转，缩放
位移：transform：translate（水平（px/%），垂直），只给一个值是水平，单独方向translateX/Y（）
旋转：transform：rotate（角度（deg）），正为顺时针，反之
转换原点：transform-origin： 水平位置 垂直位置（方位名词，px，百分比）（默认盒子中心点）
transform复合属性：transform：translate（）rotate（），旋转会改变坐标轴向，多重转换旋转放最后
缩放：transform：scale（缩放倍数）scaleX/Y/Z/3d
渐变：多个颜色逐渐变化的视觉效果，一般用于盒子背景background-image：linear-gradient（ ，，，）（transparent（透明），）
空间转换：z轴正值指向自己，transform：translated3d/X/Y/Z（）
透视：perspective（添加给父级），取值px（一般800-1200），眼睛和屏幕的距离
空间旋转：transform：rotateZ/Y/X（） rotate3d（x，y，z，角度）（xyz为0-1）
立体呈现：transform-style：preserve-3d，子元素正真处于3d空间
动画：多个状态间变化过程，过程可控（重复播放，最终画面，暂停），最小单元帧
定义动画：@keyframs 动画名称{ from{}  to{}  } （两种状态） 或 @keyframs 动画名称{ 0%{} 5%{}}（多个，百分比是动画总时长的占比）
使用动画：animation：动画名称 时间 速度曲线 延迟时间 反复次数 动画方向 执行完毕状态；不分先后，infinite（无限循环），alternate（反复），forwards（停留在最后的状态），steps（数字）逐帧动画（配合精灵图）。 如果两个时间，1表动画，2表延迟
拆分（必须有名字和时间）
steps逐帧动画：盒子尺寸为一张小图的尺寸，改变背景图的位置（精灵图的宽度），steps（N）N为精灵图个数，添加无限
多组动画：animation：动画1，动画2；
animation-play-state：paused
back-ground-size背景图缩放，contain等比例缩放，宽或高等于盒子尺寸，图片不再缩放，cover完全覆盖，则可能不全
html默认高度和浏览器不一样，和body高度一样100%
移动端特点：pc屏幕大，固定版心：手机小，宽度100%
电脑：谷歌模拟器打开移动端页面
屏幕尺寸：屏幕对角线
分辨率：宽*高，缩放150%（/150%），硬件分辨率（出厂）（物理），由软件决定（逻辑），代码参照逻辑分辨率
视口：网页宽度和分辨率相同，自动生成，viewport，移动端没有视口标签宽度为980，pc端默认100%
百分比布局：宽度自适应，高度固定
flex布局（弹性布局）：浏览器提倡的布局，简单灵活，避免浮动脱标；caniuse。com（绿色表完全支持，红色表不支持）
父元素添加：dispaly：flex，子元素自动挤压或拉伸
组成：弹性容器，弹性盒子，主轴（默认水平），侧轴（交叉轴）（默认垂直）
justify——content调节主轴的对齐方式1center：居中。2space-between：间距在弹性盒子之间。3space-evenly所有地方间距相同。4space-around间距在子集两侧（子集间距离大，两侧距离小）
侧轴对齐方式：align-items：1center垂直居中。2stretch：拉伸，默认值（现有状态，测试时去掉子集的高度）
align-self：控制某个弹性盒子的对齐方式
伸缩比：flex：整数（只占用父级剩余尺寸的份数）
flex-direction修改主轴方向（默认水平）：column列，侧轴水平。视觉效果实现水平居中，justify-content：center垂直 align-items：center水平，先确定主轴方向
弹性盒子换行（加给父级）：flex-wrap：wrap；调整对齐方式：align-content
移动适配：网页元素宽高随设备改变
rem：目前多数企业
vw/vh：未来解决方案

rem：相对单位，相对于html标签字号计算结果，1rem=1html
等比缩放
媒体查询设置差异化css样式
@media（媒体特性）{
   选择器{
       css属性
     }

}
html字号为视口的1/10
rem尺寸=px单位数值/基准根字号
flexible.js配合rem在不同设备加等比缩放，根据不同视口给网页html加font-size

less语法（快速生成css）：完成px到rem的转换，文件后缀为.less，扩充了css
注意：浏览器不识别less，要引入css文件
单行注释：//   块注释/**/
运算：加，减，乘直接写表达式，除法需添加（）或 '.'。

less嵌套生成后代选择器：注意&不生成后代选择器，表示选择当前选择器
.父级选择器{    .子级选择器{} }

使用less变量设置属性值：
定义变量：@变量名：值；
使用变量：css属性：@变量名；

使用less导入其他文件
@import 文件名'';如果是less文件，可不加.less

导出：
1.配置EasyLess插件，设置--搜索EasyLess--在setting。json中编辑（双引号加代码）
2.less文件第一行： //out ： 导出到文件名/导出为文件名.css

禁止导出
// out：false

vw/vh：相对于视口尺寸计算结果
1vw=1/100视口宽度
1vh=1/100视口高度
vw = px/（1/100视口宽度）
一个盒子不能混用，最好都为vh或vw，对全面屏不好

position:fixed固定

响应式网页：
媒体查询：根据设备宽度，设置差异化样式
max-width/min-width，屏幕方向：orientation
@media(){    选择器{} } 完整写法：@media 关键词 媒体特性 and （媒体特性）{}
也有层叠性，min（从小到大），max（从大到小）
外链式引入css： link css文件名 media=“（）”



BootStrap：使用框架快速开发响应式网页。（bootcss.com）
1下载：首页-bootstrap3
2使用：1引入：link bootstrap.(min)(压缩的).css  2使用版心（container）
container：宽度指定且居中
分别使用.row（-15外边距）和.col类名抵消container类的内边距
container-fluid:自带左右-15外边距
bootStrap栅格系统：响应式网页布局，默认将网页分成12份。超小（<768） 小（768-992）中（992-1200）大（>1200）
col-xs/sm/md/lg-*
全局css样式：控制某些标签
组件:网页常见区域（导航）
字体图标：glyphion
js插件：交互效果，实现交互效果 引入文件：script jQuery.js bootstrap.min.js
定制：框架里不一样，可以改













































