## Image特有属性
* source：图像源 例 @image-url("assets/Slint.png")
* colorize：以给定的颜色着色图像
* horizontal-alignment：水平对齐方式，取值center（居中）left（靠左）right（靠右）
* vertical-alignment：垂直对齐方式，取值center（居中）top（靠上）bottom（靠下）
* horizontal-tiling：图像水平平铺方式 取值 none（平铺，默认值）repeat（重复）round（重复并放大或缩小，以使图像完整显示）
* vertical-tiling：图像垂直平铺方式 取值 none（平铺，默认值）repeat（重复）round（重复并放大或缩小，以使图像完整显示）
* image-fit：图像填充方式 取值 fill（默认值，拉伸填充组件，可能会改变宽高比）contain（适应组件，保持宽高比）cover（覆盖组件，保持宽高比，可能会裁剪图像）preserve（适应组件，保持宽高比，可能会留空白）
* image-rendering：图像渲染方式（针对位图）smooth（默认值，平滑方式，适合缩小位图图像时保持清晰度） pixelated（以像素化的方式渲染图像，适合放大位图图像时保持清晰度）
* source-clip-x: 从图像的左边开始裁剪
* source-clip-y: 从图像的顶部开始裁剪
* source-clip-width: 图像裁剪宽度source.width - source-clip-x
* source-clip-height: 图像裁剪高度source.height - source-clip-y
* transform-origin: 旋转中心点的位置 例{x: 100px, y: 100px}
* transform-rotation: 旋转图像，单位可以是deg（度）或rad（弧度）例：45deg

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
无

## 示例代码
```
export component MainWindow inherits Window {
    width: 400px;
    height: 500px;
    
    Image {
        x: 100px;
        y: 0px;
        width: 200px;
        height: 200px;
        source: @image-url("assets/Slint.png");// 编译时就需要确认图片路径存在，否则会报错
        colorize: #ff0000; // 以给定的颜色着色图像
        //image-rendering: pixelated; // 使用像素化的方式渲染图像，适合放大位图图像时保持清晰度
        //image-rendering: smooth; // 使用平滑的方式渲染图像，适合缩小位图图像时保持清晰度
    }
    Image {
        x: 100px;
        y: 200px;
        width: 200px;
        height: 200px;
        source: @image-url("assets/Slint.svg");
        //colorize: #ff0000; // 以给定的颜色着色图像
        //horizontal-tiling: none; // 水平平铺图像
        //vertical-tiling: none; // 垂直平铺图像
        //horizontal-tiling: repeat; // 水平平铺图像
        //vertical-tiling: repeat; // 垂直平铺图像
        //horizontal-tiling: round; // 水平平铺图像
        //vertical-tiling: round; // 垂直平铺图像
        //image-fit: fill; // 图像拉伸以填充组件，可能会改变宽高比
        //image-fit: contain; // 图像适应组件，保持宽高比
        //image-fit: cover; // 图像覆盖组件，保持宽高比，可能会裁剪图像
        //image-fit: preserve; // 图像适应组件，保持宽高比，可能会留空白
        //image-rendering: pixelated; // 使用像素化的方式渲染图像，适合放大位图图像时保持清晰度
        //transform-origin: {x: 100px, y: 100px}; // 旋转中心点的位置
        //transform-rotation: 45deg; // 旋转图像，单位可以是deg（度）或rad（弧度）
    }

    /*VerticalLayout {
        spacing: 10px;
        Image{
            source: @image-url("assets/Slint.svg");
            horizontal-alignment: center;
            vertical-alignment: center;
        }
        Image{
            source: @image-url("assets/Slint.svg");
            horizontal-alignment: left;
            vertical-alignment: top;
        }
        Image{
            source: @image-url("assets/Slint.svg");
             horizontal-alignment: right;
            vertical-alignment: bottom;
        }
    }*/

    /*Image {
        source: @image-url("assets/Slint.svg");
        source-clip-x: 10; // 从图像的左边开始裁剪
        source-clip-y: 10; // 从图像的顶部开始裁剪
        //source-clip-width: 15; // source.width - source-clip-x;
        //source-clip-height: 15; // source.height - source-clip-y;
    }*/
}
```