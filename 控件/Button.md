## Button特有属性
* text：按钮文本
* checkable：按钮是否可选中
* checked：按钮是否选中
* enabled：按钮是否可用
* icon：按钮图标 如icon: @image-url("assets/icon.png");
* icon-size：图标大小
* colorize-icon：图标是否随按钮文本颜色变化
* primary：是否应用主要强调色样式

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
* 无

## 回调
* clicked()：按钮点击时调用

## 注意
1. 要使用Button组件，必须要导入：import { Button } from "std-widgets.slint";

## 示例代码
```
import { Button } from "std-widgets.slint";

export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    VerticalLayout {
        input := Text {
            text: "input text";
        }

        HorizontalLayout {
            spacing: 10px; //按钮之间的间距
            Button {
                width: 100px;
                height: 40px;
                text: "click"; //按钮文本
                //text: "修改文本";
                //checkable: true; //按钮是否可选中
                //checked: true; //按钮是否选中
                //enabled: false; //按钮是否可用
                //icon: @image-url("assets/icon.png"); //按钮图标
                //icon-size: 50px; //图标大小
                //colorize-icon: true; //图标是否随按钮文本颜色变化
                //primary: true; //是否应用主要强调色样式
                clicked => {
                    input.text = "text changed"; //修改文本
                }
            }

            Button {
                width: 100px;
                height: 40px;
                text: "cancel";
            }

            Button {
                width: 100px;
                height: 40px;
                text: "ok";
            }
        }
    }
}
```
