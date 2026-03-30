## Path特有属性
* stroke：描边颜色
* stroke-width：描边宽度
* stroke-line-cap：线条末端样式 butt、round、square
* stroke-line-join：线条连接样式 miter、round、bevel
* fill：填充颜色 例#ff0000
* fill-rule：填充规则，取值nonzero、evenodd
* anti-alias：是否启用抗锯齿
* Commands：描述svg path的命令

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
*  无

## 注意
1. 如果width和height没有设置，则Path会占满整个父窗口
1. 需要Path的地方我个人觉得是可以用Image替换的，svg图片编辑及可视化都比Path要方便

## 示例代码
```
export component MainWindow inherits Window {
    width: 400px;
    height: 500px;
    Path {
        //width: 100px;
        //height: 100px;
        commands: "M110,0  h90 v90 h-90 z M130,20 h50 v50 h-50 z";
        stroke: blue;// 描边颜色
        stroke-width: 5px;
        fill: #ff0000; // 填充颜色
        //fill-rule: nonzero;
        //fill-rule: evenodd;
        //stroke-line-cap: butt; // 线条末端样式
        //stroke-line-cap: round; // 线条末端样式
        //stroke-line-cap: square; // 线条末端样式
        //stroke-line-join: miter; // 线条连接样式
        //stroke-line-join: round; // 线条连接样式
        //stroke-line-join: bevel; // 线条连接样式
       anti-alias: true; // 是否启用抗锯齿
    }
}
```