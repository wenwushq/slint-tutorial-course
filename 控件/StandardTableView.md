## StandardTableView特有属性
* enabled：是否启用标准表格视图
* current-row：当前选中的行索引 默认值为-1表示没有选中任何行
* columns：表格的列标题 如columns: [{ title: "Header 1" }, { title: "Header 2" }];
* rows：表格的行数据 如rows: [[{ text: "Item 1" }, { text: "Item 2" }]];
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
* set-current-row(int)：通过索引设置当前行并将其显示出来

## 回调
* sort-ascending(column)：当用户点击列标题以升序排序时触发
* sort-descending(column)：当用户点击列标题以降序排序时触发
* current-row-changed(index)：当前选中的行发生变化时触发
* row-pointer-event(row, event, position)：当用户在表格行上发生指针事件（如点击、悬停等）时触发

## 注意
1. 要使用StandardTableView组件，必须要导入：import { StandardTableView } from "std-widgets.slint";
1. 设置columns时，最好设置下min-width（最小的宽度）

## 示例代码
```
export component MainWindow inherits Window {
    width: 400px;
    height: 200px;
    StandardTableView {
        width: 230px; //标准表格视图的宽度
        height: 100%; //标准表格视图的高度
        //enabled: true; //是否启用标准表格视图 默认值为true
        //vertical-scrollbar-policy: always-off; //禁用垂直滚动条
        //vertical-scrollbar-policy: as-needed; //根据需要显示垂直滚动条 默认值
        //vertical-scrollbar-policy: always-on; //始终显示垂直滚动条
        //horizontal-scrollbar-policy: always-off; //禁用水平滚动条
        //horizontal-scrollbar-policy: as-needed; //根据需要显示水平滚动条 默认值
        //horizontal-scrollbar-policy: always-on; //始终显示水平滚动条
        //current-row: 0; //当前选中的行索引 默认值为-1表示没有选中任何行
        
        columns: [ //表格的列标题 如columns: [{ title: "Header 1" }, { title: "Header 2" }];
            { title: "学号", width: 150px, min-width: 100px },
            { title: "姓名", width: 80px, min-width: 60px },
        ];
        rows: [ //表格的行数据 如rows: [[{ text: "Item 1" }, { text: "Item 2" }]];
            [
                { text: "000001" },
                { text: "张三" },
            ],
            [
                { text: "000002" },
                { text: "李四" },
            ],
            [
                { text: "000003" },
                { text: "王五" },
            ]
        ];

        /*sort-ascending(column) => { //当用户点击列标题以升序排序时触发的事件处理器
            debug("Sort ascending by column: ", column);
        }

        sort-descending(column) => { //当用户点击列标题以降序排序时触发的事件处理器
            debug("Sort descending by column: ", column);
        }

        row-pointer-event(row, event, position) => { //当用户在表格行上发生指针事件（如点击、悬停等）时触发的事件处理器
            debug("Pointer event on row: ", row, " Event: ", event, " Position: ", position);
        }

        current-row-changed(index) => { //当前选中的行发生变化时触发的事件处理器
            debug("Current row: ", index);
        }*/
    }
}
```