## SpinBox特有属性
* value：微调控的当前值 默认值为0
* maximum：微调控的最大值 默认值为100
* minimum： 微调控的最小值 默认值为0
* read-only：是否只读 默认值为false
* step-size：微调框的步长 默认值为1 不能为小数
* horizontal-alignment：//水平对齐方式  默认值为left 可选值为left、center、right、start（文字方向的起始位置）、end（文字方向的结束位置

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
* edited()：当微调框的值被编辑时触发的事件

## 注意
1. 要使用SpinBox组件，必须要导入：import { SpinBox } from "std-widgets.slint";

## 示例代码
```
import { SpinBox } from "std-widgets.slint";

export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    SpinBox {
        width: 90%;
        height: 30px;
        value: 50; //微调框的当前值 默认值为0
        maximum: 100; //微调框的最大值 默认值为100
        minimum: 0; //微调框的最小值 默认值为0
        //read-only: true; //是否只读 默认值为false
        step-size: 5; //微调框的步长 默认值为1 不能为小数
        horizontal-alignment: left; //水平对齐方式 可选值为left、center、right、start（文字方向的起始位置）、end（文字方向的结束位置） 默认值为left
        edited(value) => { //当微调框的值被编辑时触发的事件，参数value为当前的值
            debug("New value: ", value);
        }
    }
}
```
