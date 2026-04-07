## Rectangle特有属性
* background：背景颜色 不设置背景颜色则默认为透明
* border-width：边框宽度
* border-color：边框颜色
* border-radius：圆角半径 设置为宽度的一半可以实现圆形效果 (border-radius: self.width/2)
* border-top-left-radius：左上角圆角半径
* border-top-right-radius：右上角圆角半径
* border-bottom-left-radius：左下角圆角半径
* border-bottom-right-radius：右下角圆角半径
* clip: 是否裁剪子元素，设置为true可以让子元素超出边界时被裁剪掉
* drop-shadow-blur: 阴影模糊半径
* drop-shadow-color: 阴影颜色
* drop-shadow-offset-x: 阴影水平偏移
* drop-shadow-offset-y: 阴影垂直偏移

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
1. Rectangle是一个容器控件，比如要实现ImageButton，可以用Rectangle包含一个水平布局，水平布局里添加一个Image一个Button，即可实现ImageButton控件

## 示例代码
```
export component MainWindow inherits Window {
    Rectangle {
        width: 200px;
        height: 200px;
        background: #315afd; // 背景颜色 不设置背景颜色则默认为透明
        //background: @linear-gradient(40deg, rgba(255, 0, 0, 1) 0%, rgba(255, 154, 0, 1) 10%, rgba(208, 222, 33, 1) 20%,rgba(79, 220, 74, 1) 30%, rgba(63, 218, 216, 1) 40%, rgba(47, 201, 226, 1) 50%, rgba(28, 127, 238, 1) 60%, rgba(95, 21, 242, 1) 70%, rgba(186, 12, 248, 1) 80%, rgba(251, 7, 217, 1) 90%, rgba(255, 0, 0, 1) 100%); // 背景颜色，使用渐变色
        //border-width: 10px; // 边框宽度
        //border-color: #ff0000; // 边框颜色
        //border-radius: 10px; // 圆角半径
        //border-top-left-radius: 20px; // 左上角圆角半径
        //border-top-right-radius: 30px; // 右上角圆角半径
        //border-bottom-left-radius: 40px; // 左下角圆角半径
        //border-bottom-right-radius: 50px; // 右下角圆角半径
        //border-radius: 100px; // 圆角半径，设置为宽度的一半可以实现圆形效果
        //border-radius: self.width/2;
        //clip: true; // 是否裁剪子元素，设置为true可以让子元素超出边界时被裁剪掉
        //drop-shadow-blur: 10px; // 阴影模糊半径
        //drop-shadow-color: rgba(255, 0, 0, 0.5); // 阴影颜色
        //drop-shadow-offset-x: -15px; // 阴影水平偏移
        //drop-shadow-offset-y: -15px; // 阴影垂直偏移

        /*Rectangle {
            x: -40px;
            y: -40px;
            width: 100px;
            height: 100px;
            background: lightslategray;
        }*/
    }
}
```