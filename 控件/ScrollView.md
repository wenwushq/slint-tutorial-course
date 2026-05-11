## ScrollView特有属性
* enabled：是否启用滚动视图 默认值为true
* viewport-x：滚动视图相对于视口的 x 位置, 通常是一个负值
* viewport-y：滚动视图相对于视口的 y 位置, 通常是一个负值
* viewport-width：滚动视口的宽度
* viewport-height：滚动视口的高度
* vertical-scrollbar-policy：垂直滚动条策略 默认值为as-needed 可选值为as-needed（根据需要显示）、always-off（禁用）、always-on（始终显示）
* horizontal-scrollbar-policy：水平滚动条策略 默认值为as-needed 可选值为as-needed（根据需要显示）、always-off（禁用）、always-on（始终显示）

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
* scrolled()：当列表视图被滚动时触发

## 注意
1. 要使用ScrollView组件，必须要导入：import { ScrollView } from "std-widgets.slint";
1. viewport的宽高必须大于ScrollView的宽高，才会有滚动的效果
1. 添加子控件的位置是以viewport计算的，如果viewport不设置，宽高等于滚动视图的宽高

## 示例代码
```
export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    ScrollView {
        width: 200px; //滚动视图的宽度
        height: 200px; //滚动视图的高度
        viewport-x: -50px; //滚动视图相对于视口的 x 位置, 通常是一个负值
        viewport-y: -50px; //滚动视图相对于视口的 y 位置, 通常是一个负值
        viewport-width: 300px; //滚动视口的宽度
        viewport-height: 300px; //滚动视口的高度
        enabled: false; //是否启用滚动视图 默认值为true
        //vertical-scrollbar-policy: always-off; //禁用垂直滚动条
        //vertical-scrollbar-policy: as-needed; //根据需要显示垂直滚动条 默认值
        //vertical-scrollbar-policy: always-on; //始终显示垂直滚动条
        //horizontal-scrollbar-policy: as-needed; //根据需要显示水平滚动条 默认值
        //horizontal-scrollbar-policy: always-off; //禁用水平滚动条
        //horizontal-scrollbar-policy: always-on; //始终显示水平滚动条
       
        Rectangle {
            width: 30px;
            height: 30px;
            x: 275px;
            y: 50px;
            background: blue;
        }

        Rectangle {
            width: 30px;
            height: 30px;
            x: 175px;
            y: 130px;
            background: red;
        }

        Rectangle {
            width: 30px;
            height: 30px;
            x: 25px;
            y: 210px;
            background: yellow;
        }

        Rectangle {
            width: 30px;
            height: 30px;
            x: 98px;
            y: 55px;
            background: orange;
        }

        scrolled() => {
            //当滚动视图被滚动时触发
        debug("viewport-x: ", self.viewport-x);
            debug("viewport-y: ", self.viewport-y);
        }
    }
}
```