## Text特有属性
* text：Text显示内容
* color：字体颜色
* font-family：字体
* font-size：字体大小
* font-weight：字体加粗 取值范围100-900，数值越大越粗 400为正常字体
* font-italic：字体斜体
* horizontal-alignment：水平对齐方式，取值center（居中）left（靠左）right（靠右）
* vertical-alignment：垂直对齐方式，取值center（居中）top（靠上）bottom（靠下）
* letter-spacing：字母间距
* overflow：文本溢出时的处理方式，取值clip（裁剪）elide（省略号）
* wrap：文本换行，取值no-wrap（不换行）word-wrap（单词内换行）char-wrap（字符内换行）
* stroke: 文本描边颜色
* stroke-width: 文本描边宽度
* stroke-style:文本描边样式，取值outside（在文本外侧描边）center（在文本中心描边）

## 和其他控件共有属性
*  x：起始x坐标 例：5px
*  y：起始y坐标 例：5px
*  width：窗口固定宽度 例 800px
*  height：窗口固定高度 例 600px
*  preferred-width：窗口首选宽度 例 800px
*  preferred-height：窗口首选高度 例 600px
*  min-width： 窗口最小宽度 例 400px
*  min-height：窗口最小高度 例 300px
*  max-width：窗口最大宽度 例 800px
*  max-height：窗口最大高度 例 600px

## 方法
*  无

## 注意
*  无

## 示例代码
```
export component MainWindow inherits Window {
    in-out property <string> content;
    width: 400px;
    height: 400px;
    Text {
        //text: content;
        text: "Hello World"; //Text显示内容
        color: #3586f4; //字体颜色
        //font-family: "Microsoft YaHei"; //字体
        font-size: 30px; //字体大小
        //font-weight: 800; //字体加粗 取值范围100-900，数值越大越粗 400为正常字体
        //font-italic: true; //字体斜体
        //horizontal-alignment: center; //水平对齐方式
        //vertical-alignment: center; //垂直对齐方式
        //letter-spacing: 10px; //字母间距
        //overflow: clip; //文本溢出时的处理方式，裁剪
        //overflow: elide; //文本溢出时的处理方式，省略号
        //text: "Hello World,Hello World,Hello World";
        //width: 200px;
        //wrap: no-wrap; //文本换行，不换行
        //wrap: word-wrap; //文本换行，单词内换行
        //wrap: char-wrap; //文本换行，字符内换行
        //stroke: #ff0000; //文本描边颜色
        //stroke-width: 2px; //文本描边宽度
        //stroke-style: outside; //文本描边样式 在文本外侧描边
        //stroke-style: center; //文本描边样式 在文本中心描边
    }
}
```