## ComboBox特有属性
* model：下拉列表的选项 如model: ["选项一", "选项二", "选项三"];
* enabled：下拉列表是否可用
* current-value：设置下拉列表选中项的值
* current-index：设置下拉列表选中项 从0开始计数

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
* selected()：选项被选中时调用

## 注意
1. 要使用ComboBox组件，必须要导入：import { ComboBox } from "std-widgets.slint";

## 示例代码
```
import { ComboBox } from "std-widgets.slint";

export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    ComboBox {
        x: 5px;
        y: 5px;
        width: 100px;
        model: ["选项一", "选项二", "选项三"]; // 设置下拉列表的选项
        current-index: 1; // 设置下拉列表选中项 从0开始计数
        current-value: "选项三"; // 设置下拉列表选中项的值
        enabled: true; // 下拉列表是否可用
        selected(value) => { // 选项被选中时触发的事件
            debug("Selected value: ", value);
        }
    }
}
```
