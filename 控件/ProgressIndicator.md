## ProgressIndicator特有属性
* progress：进度条的当前进度值，范围从 0.0 到 1.0
* indeterminate：进度条的进度是否是不确定的 默认值为false 如果操作的进度无法通过数值确定，则设置为 true

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
1. 要使用ProgressIndicator组件，必须要导入：import { ProgressIndicator } from "std-widgets.slint";

## 示例代码
```
import { ProgressIndicator } from "std-widgets.slint";

export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    ProgressIndicator {
        width: 90%;
        height: 30px;  
        //indeterminate: false; //进度条的进度是否是不确定的 如果操作的进度无法通过数值确定，则设置为 true。
        progress: 0.6; //进度条的当前进度值，范围从 0.0 到 1.0。
    }
}
```
