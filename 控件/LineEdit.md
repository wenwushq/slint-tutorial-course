## LineEdit特有属性
* text：编辑框内容
* color：字体颜色
* font-family：字体
* font-size：字体大小
* font-italic：字体斜体
* horizontal-alignment：水平对齐方式 默认值为left 可选值为left、center、right、start（文字方向的起始位置）、end（文字方向的结束位置）
* input-type：输入类型，取值text（文本，默认值） password（密码）number（数字）decimal（小数）
* placeholder-text：编辑框的占位文本
* read-only：只读模式

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
* edited()：文本改变时调用
* key-pressed(KeyEvent) -> EventResult：按键按下时调用
* key-released(KeyEvent) -> EventResult：按键松开时调用

## 注意
1. 要使用LineEdit组件，必须要导入：import { LineEdit } from "std-widgets.slint";

## 示例代码
```
export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    LineEdit {
        height: 50px; //编辑框的高度
        text: "编辑框"; //编辑框的文本标签
        //enabled: false; //编辑框是否可用
        //font-size: 20px; //编辑框的字体大小 默认值为0px
        //font-family: "Arial"; //编辑框的字体类型 默认值为""
        //font-italic: true; //编辑框的字体是否斜体 默认值为false
        //horizontal-alignment: start; //水平对齐方式 默认值为left 可选值为left、center、right、start（文字方向的起始位置）、end（文字方向的结束位置）
        //input-type: password; //输入类型，取值text（文本，默认值） password（密码）number（数字）decimal（小数）
        //placeholder-text: "请输入内容"; //编辑框的占位文本
        //read-only: true; //编辑框是否只读 默认值为false
    }
}
```