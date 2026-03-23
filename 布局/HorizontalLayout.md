## HorizontalLayout特有属性
* spacing： 元素之间的距离 例：5px 默认值为0px
* padding：内边距，四个边统一设置，默认值为0px
* padding-left：左内边距 默认值为0px
* padding-right：右内边距 默认值为0px
* padding-top：上内边距 默认值为0px
* padding-bottom：下内边距 默认值为0px
* alignment：对齐方式 取值：stretch（拉伸 默认值）、center（居中）、start（起始元素）、end（结束元素）、space-between（元素之间平均分布）、space-around（元素之间平均分布，且两端有一半的间距）、space-evenly（元素之间平均分布，且两端有相同的间距）

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
1. padding-left、padding-right、padding-top、padding-bottom的优先级高于padding属性

## 示例代码
```
export component MainWindow inherits Window {
    width: 400px;
    height: 300px;
    HorizontalLayout {
        spacing: 5px; // 元素之间的距离
        //padding: 10px; // 内边距
        //padding-left: 20px; // 左内边距
        width: 100%; // 占满父级宽度
        height: 100%; // 占满父级高度
        x: 0px;
        y: 0px;
        //alignment: center; // 居中对齐
        //alignment: start; // 起始元素对齐
        //alignment: end; // 结束元素对齐
        //alignment: space-between; // 元素之间平均分布
        //alignment: space-around; // 元素之间平均分布，且两端有一半的间距
        //alignment: space-evenly; // 元素之间平均分布，且两端有相同的间距
    
        Rectangle { background: red; width:50px; height: 30px; }
        Rectangle { background: green; width:100px; height: 30px; }
        Rectangle { background: blue; width:50px; height: 80px; }
    }
}
```
