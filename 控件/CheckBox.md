## CheckBox特有属性
* text：复选框文本
* checked：复选框是否选中
* enabled：复选框是否可用

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
* toggled()：复选框状态改变时调用

## 注意
1. 要使用CheckBox组件，必须要导入：import { CheckBox } from "std-widgets.slint";

## 示例代码
```
import { CheckBox } from "std-widgets.slint";

export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    checkItem := CheckBox {
        x: 5px;
        //width: parent.width;
        //height: parent.height;
        text: "复选框"; //复选框文本
        //checked: true;  //复选框是否选中
        //enabled: false; //复选框是否可用
        toggled() => { //复选框状态改变时触发的事件
            checkItem.text = "复选框 " + (self.checked ? "选中" : "未选中");
        }
    }
}
```
