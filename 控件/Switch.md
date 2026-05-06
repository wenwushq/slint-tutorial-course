## Switch特有属性
* text：开关组件的文本标签
* checked：开关组件是否打开
* enabled：开关组件是否可用

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
* toggled()：开关组件的状态发生变化时调用

## 注意
1. 要使用Switch组件，必须要导入：import { Switch } from "std-widgets.slint";
1. 高度设置过小时，字体会显示有问题，高度尽量不要设置

## 示例代码
```
import { Switch } from "std-widgets.slint";

export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    Switch {
        //height: 10px; //开关组件的高度
        //checked: true; //开关组件是否打开
        //enabled: false; //开关组件是否可用
        text: "开关组件"; //开关组件的文本标签
        toggled => { //当开关组件的状态发生变化时触发的事件
            self.text = "开关组件 " + (self.checked ? "开" : "关");
        }
       
    }
}
```
