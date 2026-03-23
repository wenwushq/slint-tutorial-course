## GridLayout特有属性
* spacing： 元素之间的距离 例：5px 默认值为0px
* spacing-horizontal： 水平元素之间的距离 例：5px 默认值为0px
* spacing-vertical： 垂直元素之间的距离 例：5px 默认值为0px
* padding：内边距，四个边统一设置，默认值为0px
* padding-left：左内边距 默认值为0px
* padding-right：右内边距 默认值为0px
* padding-top：上内边距 默认值为0px
* padding-bottom：下内边距 默认值为0px

## 子元素特有属性
* row： 子元素位于GridLayout中的第几行，行以0开始
* col： 子元素位于GridLayout中的第几列，列以0开始
* rowspan： 子元素占据几行
* colspan：子元素占据几列

## 和其他控件共有属性
*  x：起始x坐标 例：5px
*  y：起始y坐标 例：5px
*  width：窗口固定宽度 例 800px
*  height：窗口固定高度 例 600px
*  preferred-width：窗口首选宽度 例 800px
*  preferred-height：窗口首选高度 例 600px
*  min-width： 窗口最小宽度 例 400px
*  min-height：窗口最小高度 例 300px
*  max-width：窗口最大宽度 例 800px
*  max-height：窗口最大高度 例 600px

## 方法
*  无

## 注意
1. spacing-horizontal、spacing-vertical的优先级高于spacing属性
1. padding-left、padding-right、padding-top、padding-bottom的优先级高于padding属性

## 示例代码
```
export component MainWindow inherits Window {
    width: 400px;
    height: 300px;
    GridLayout {
        spacing: 5px; // 元素之间的距离
        spacing-horizontal: 10px; // 水平元素之间的距离
        //spacing-vertical: 10px; // 垂直元素之间的距离
        //padding: 10px; // 内边距
        //padding-left: 20px; // 左内边距
        width: 100%; // 占满父级宽度
        height: 100%; // 占满父级高度
        x: 0px;
        y: 0px;
    
        //第一行
        Rectangle { background: red; width:50px; height: 30px; }
        Rectangle { background: green; width:100px; height: 30px; }
        Rectangle { background: blue; width:50px; height: 80px; }

        //第二行
        Rectangle { background: red; width:50px; height: 30px; row: 1; col: 0; }
        Rectangle { background: green; width:100px; height: 30px; row: 1; col: 1; }
        Rectangle { background: blue; width:50px; height: 80px; row: 1; col: 2; }

        //第三行
        //Rectangle { background: red; width:50px; height: 30px; row: 2; col: 0; }
        Rectangle { background: green; width:300px; height: 30px; row: 2; col: 1; colspan: 2; }

        //第四行
        Rectangle { background: red; width:50px; height: 100px; row: 2; col: 0;  rowspan: 2; }
        Rectangle { background: green; width:100px; height: 30px; row: 3; col: 1; }
        Rectangle { background: blue; width:50px; height: 80px; row: 3; col: 2; }
    }
}
```
