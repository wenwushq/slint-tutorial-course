## StandardListView特有属性
* enabled：是否启用列表视图 默认值为true
* vertical-scrollbar-policy：垂直滚动条策略 默认值为as-needed 可选值为as-needed（根据需要显示）、always-off（禁用）、always-on（始终显示）
* current-item：当前选中的项的索引 默认值为-1，表示没有选中任何项
* model：标准列表视图的数据模型 如model:[{text:"item0"}, {text:"item1"}];

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
* set-current-item(int)：设置当前选中项

## 回调
* scrolled()：当列表视图被滚动时触发
* current-item-changed(index)：当前选中的项发生变化时触发
* item-pointer-event(index, event, point)：项发生指针事件时触发

## 注意
1. 要使用StandardListView组件，必须要导入：import { StandardListView } from "std-widgets.slint";
1. StandardListView的使用频率比ListView高，更实用

## 示例代码
```
export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    StandardListView {
        width: 100px; //标准列表视图的宽度
        height: 100%; //标准列表视图的高度
        enabled: true; //是否启用标准列表视图 默认值为true
        //vertical-scrollbar-policy: always-off; //禁用垂直滚动条
        //vertical-scrollbar-policy: as-needed; //根据需要显示垂直滚动条 默认值
        //vertical-scrollbar-policy: always-on; //始终显示垂直滚动条
        //current-item: 2; //当前选中的项的索引 默认值为-1，表示没有选中任何项
       
        model: [ //标准列表视图的数据模型
            { text: "Blue11111111111111111111" },
            { text: "Red" },
            { text: "Green" },
            { text: "Yellow" },
            { text: "Black" },
            { text: "White" },
            { text: "Magenta" },
            { text: "Cyan" }
        ];

        scrolled() => {
            //当滚动视图被滚动时触发
            debug("viewport-x: ", self.viewport-x);
            debug("viewport-y: ", self.viewport-y);
        }
        /*current-item-changed(index) => { //当前选中的项发生变化时触发
            debug("Current item: ", index);
        }*/
        /*item-pointer-event(index, event, point) => { //当项发生指针事件时触发
            debug("Item pointer event: ", index, event, point);
        }*/
    }
}
```