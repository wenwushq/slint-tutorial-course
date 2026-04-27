## Slider特有属性
* value：滑块的当前值 默认值为0
* maximum：滑块的最大值 默认值为100
* minimum： 滑块的最小值 默认值为0
* orientation：滑块的方向 可选值为horizontal（水平）vertical（垂直）默认值为horizontal
* step：按方向键时滑块的步长 默认值为1 水平方向时按左右键增加或减少值 垂直方向时按上或下键增加或减少值

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
* changed()：当滑块的值发生变化时触发的事件
* released()：当滑块鼠标释放或方向键抬起时触发的事件

## 注意
1. 要使用Slider组件，必须要导入：import { Slider } from "std-widgets.slint";

## 示例代码
```
export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    Slider {
        width: 90%;
        height: 30px;  
        value: 50; //滑块的当前值 默认值为0
        maximum: 100; //滑块的最大值 默认值为100
        minimum: 0; //滑块的最小值 默认值为0
        //orientation: horizontal; //滑块的方向 可选值为"horizontal"或"vertical" 默认值为"horizontal"
        /*width: 30px;
        height: 90%;
        orientation: vertical;*/
        step: 5; //按方向键时滑块的步长 默认值为1 水平方向时按左右键增加或减少值 垂直方向时按上或下键增加或减少值
        changed(value) => { //当滑块的值发生变化时触发的事件
            debug("new value:", value);
        }
        released(pos) => { //当滑块鼠标释放或方向键抬起时触发的事件
            debug("released at position:", pos)
        }
    }
}

```
