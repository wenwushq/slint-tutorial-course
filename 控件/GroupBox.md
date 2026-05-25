## GroupBox特有属性
* enabled：分组框是否可用 默认值为true
* title：分组框的标题
* content-padding：分组框内容的内边距

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
* 无

## 注意
1. 要使用GroupBox组件，必须要导入：import { GroupBox } from "std-widgets.slint";
1. enabled设置为false时，并不影响其子控件的交互（可能是官方bug）

## 示例代码
```
import { GroupBox , VerticalBox, CheckBox } from "std-widgets.slint";

export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    GroupBox {
        height: 150px; //分组框的高度
        width: 300px; //分组框的宽度
        title: "分组框"; //分组框的标题
        enabled: false; //分组框是否可用
        //content-padding: 10px; //分组框内容的内边距
        VerticalLayout {
            CheckBox { text: "Bread"; checked: true ;}
            CheckBox { text: "Fruits"; }
        }
    }
}
```