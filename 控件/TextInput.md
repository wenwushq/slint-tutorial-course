## TextInput特有属性
* text：文本内容
* color：字体颜色
* font-family：字体
* font-size：字体大小
* font-weight：字体加粗 取值范围100-900，数值越大越粗 400为正常字体
* font-italic：字体斜体
* horizontal-alignment：水平对齐方式，取值center（居中）left（靠左）right（靠右）
* vertical-alignment：垂直对齐方式，取值center（居中）top（靠上）bottom（靠下）
* letter-spacing：字母间距
* input-type：输入类型，取值text（文本，默认值） password（密码）number（数字）decimal（小数）
* page-height：页面的高度用于计算当用户按页上或页下时滚动的距离
* read-only：只读模式
* selection-background-color：选中文本的背景颜色
* selection-foreground-color：选中文本的颜色
* single-line: 单行输入模式
* text-cursor-width: 光标宽度
* wrap：文本换行，取值no-wrap（不换行）word-wrap（单词内换行）char-wrap（字符内换行）

## 和其他控件共有属性
*  width：窗口固定宽度 例 800px
*  height：窗口固定高度 例 600px
*  preferred-width：窗口首选宽度 例 800px
*  preferred-height：窗口首选高度 例 600px
*  min-width： 窗口最小宽度 例 400px
*  min-height：窗口最小高度 例 300px
*  max-width：窗口最大宽度 例 800px
*  max-height：窗口最大高度 例 600px

## 方法
* focus()：获取输入焦点
* clear-focus()：清除焦点
* set-selection-offsets(int, int)：选择位于两个 UTF-8 偏移量之间的文本
* select-all()：全选
* clear-selection()：清除选择标记
* copy()：复制
* cut()：剪切
* paste()：粘贴

## 回调
* accepted()：回车键按下时调用
* cursor-position-changed(Point)：光标位置改变时调用
* edited()：文本改变时调用
* key-pressed(KeyEvent) -> EventResult：按键按下时调用
* key-released(KeyEvent) -> EventResult：按键松开时调用

## 注意
1. 无

## 示例代码
```
export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    TextInput {
        text: "中国"; // 设置文本内容
        //text: "hello world"; // 设置文本内容
        color: red; // 设置文本颜色
        font-family: "Microsoft YaHei"; // 设置字体
        font-size: 24px; // 设置字体大小
        //font-weight: 800; // 设置字体加粗
        //font-italic: true; // 设置字体斜体
        horizontal-alignment: center; // 设置水平对齐方式为居中
        vertical-alignment: center; // 设置垂直对齐方式为居中
        //horizontal-alignment: left; // 设置水平对齐方式为左对齐
        //vertical-alignment: top; // 设置垂直对齐方式为顶部对齐
        //horizontal-alignment: right; // 设置水平对齐方式为右对齐
        //vertical-alignment: bottom; // 设置垂直对齐方式为底部对
        //input-type: text; // 设置输入类型为文本
        //input-type: password; // 设置输入类型为密码
        //input-type: number; // 设置输入类型为数字
        //input-type: decimal; // 设置输入类型为小数
        //letter-spacing: 10px; // 设置字符间距
        //page-height: 30px; // 页面的高度用于计算当用户按页上或页下时滚动的距离
        //read-only: true; // 设置为只读模式
        //selection-background-color: red; // 设置选中文本的背景颜色
        //selection-foreground-color: black; // 设置选中文本的颜色
        //single-line: false; // 设置单行输入模式
        //text-cursor-width: 10px; // 设置光标宽度
        //wrap: no-wrap; // 设置文本自动换行
        //wrap: word-wrap; // 设置文本自动换行，单词换行
        //wrap: char-wrap; // 设置文本自动换行，字符换行
    }
}
```
