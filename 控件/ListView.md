## ListView特有属性
* enabled：是否启用列表视图 默认值为true
* vertical-scrollbar-policy：垂直滚动条策略 默认值为as-needed 可选值为as-needed（根据需要显示）、always-off（禁用）、always-on（始终显示）

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
1. 要使用ListView组件，必须要导入：import { ListView } from "std-widgets.slint";
1. ListView相当于一个垂直布局且带有滚动条的容器，添加的子控件会自动布局
1. ListView添加子控件，必须采用for的形式进行添加

## 示例代码
```
export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    ListView {
        width: 100px; //列表视图的宽度
        height: 100%; //列表视图的高度
        enabled: true; //是否启用列表视图 默认值为true
        //vertical-scrollbar-policy: always-off; //禁用垂直滚动条
        //vertical-scrollbar-policy: as-needed; //根据需要显示垂直滚动条 默认值
        //vertical-scrollbar-policy: always-on; //始终显示垂直滚动条
         for data in [
            { text: "Blue11111111111111aaaaaaaaaa", color: #0000ff, bg: #eeeeee },
            { text: "Red", color: #ff0000, bg: #eeeeee },
            { text: "Green", color: #00ff00, bg: #eeeeee },
            { text: "Yellow", color: #ffff00, bg: #222222 },
            { text: "Black", color: #000000, bg: #eeeeee },
            { text: "White", color: #ffffff, bg: #222222 },
            { text: "Magenta", color: #ff00ff, bg: #eeeeee },
            { text: "Cyan", color: #00ffff, bg: #222222 },
        ]: Rectangle {
            height: 30px;
            background: data.bg;
            width: parent.width;
            Text {
                x: 0;
                text: data.text;
                color: data.color;
            }
        }

        scrolled() => { //当列表视图被滚动时触发
            debug("viewport-x: ", self.viewport-x);
            debug("viewport-y: ", self.viewport-y);
        }
    }
}
```