# 几个重要概念
1. 文档流Normal Flow
2. 块、内联、内联块
3. margin合并
4. 两种盒模型(border-box较为符合人类思维)

# 文档流
## 流动方向
1. inline 元素从左到右, 到达最右边才会换行
2. block 元素从上到下, 每一个都另起一行
3. inline-block 从左到右, 当一行末尾不能放下一个元素的时候会另起一行
## 宽度
1. inline 宽度为内部inline元素的和, 不能用width指定
2. block 默认自动计算宽度, 可以使用width指定
2. inline-block 结合前两者特点, 可用width
## 高度
1. inline 高度由line-height 间接确定, 跟height无关
2. block 高度由内部文档流元素确定, 可以设height
2. inline-block 跟block类似, 可以设置height

# 注意
1. inline元素不能含有block元素
2. div的宽度是能有宽就多宽, 不一定是100%, 在设置div宽度的时候不要设置100%
3. 元素脱离文档流
  1. float
  2. position: absolute / fixed

# CSS盒模型
1. 两种盒模型: content-box, border-box
2. content-box的宽度只包含content
2. border-box的宽度含border、margin、padding、content

* content-box 内容盒-内容就是盒子的边界
* border-box 边框盒-边框才是盒子的边界
* content-box: width = 内容宽度
* border-box: width = 内容宽度 + padding + border
* border-box 好用
* 同时指定padding、width、border就知道为什么了

# margin合并
1. 父子margin合并
2. 兄弟margin合并
# 如何阻止合并
1. 父子合并用 padding / border挡住
2. 父子合并 overflow: hidden 挡住
3. 父子合并 display: flex
4. 兄弟合并是符合预期的
5. 兄弟合并可以用inline-block消除

# 颜色取值
1. 颜色英语名称
2. 颜色16进制代码
3. rgb
4. rgba a 代表透明度, 取值范围0-1, 1是完全不透明, 0是完全透明
5. 透明简写 transparent
6. hsl (0-360, 百分数, 百分数); 色相, 饱和度, 亮度