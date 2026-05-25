## TabWidget特有属性
* current-index：当前选中的标签索引，默认为0
* orientation：标签排列方向，默认为horizontal(水平) 可选值为horizontal(水平)、vertical（垂直）
* title： Tab的特有属性 标签标题，可以包含换行符\n来实现多行显示

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
1. 要使用TabWidget组件，必须要导入：import { TabWidget } from "std-widgets.slint";

## 示例代码
```
import { TabWidget } from "std-widgets.slint";

export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    TabWidget {
        //current-index: 0; // 当前选中的标签索引，默认为0
        orientation: Orientation.vertical; // 标签排列方向，默认为horizontal(水平) vertical（垂直）
        Tab {
            //title: "标\n签\n组\n件\n1";
            title: "标签组件1"; // 标签标题，可以包含换行符\n来实现多行显示
            Rectangle {
                width: 100%;
                height: 100%;
                background: #f0f0f0;
            }
        }
        Tab {
            //title: "标\n签\n组\n件\n2";
            title: "标签组件2";
            Rectangle {
                width: 100%;
                height: 100%;
                background: #e0e0e0;
            }
        }
    }
}
```
