## PopupWindow特有属性
* close-policy：关闭策略 取值说明：close-on-click（点击即可关闭弹窗）；close-on-click-outside（点击弹窗外部即可关闭弹窗）；no-auto-close（不自动关闭弹窗，需要手动调用popup.close()方法来关闭弹窗）

## 和其他控件共有属性
* x：窗口的x坐标（相对于父窗口）
* y：窗口的y坐标（相对于父窗口）
*  width：窗口固定宽度 例 800px
*  height：窗口固定高度 例 600px

## 方法
*  show()：显示窗口
*  close()：关闭窗口

## 注意


## 示例代码
```
export component MainWindow inherits Window {
    background: #f0f0f0;
    popup := PopupWindow {
        Rectangle {
            height: 100%;
            width: 100%;
            background: yellow;
        }

        x: 20px; //窗口的x坐标 （相对于父窗口MainWindow）
        y: 20px; //窗口的y坐标 （相对于父窗口MainWindow）
        height: 500px;
        width: 500px;
        close-policy: close-on-click; //关闭策略，点击即可关闭弹窗
        //close-policy: close-on-click-outside; //关闭策略，点击弹窗外部即可关闭弹窗
        //close-policy: no-auto-close; //关闭策略，不自动关闭弹窗，需要手动调用popup.close()方法来关闭弹窗
    }

    TouchArea {
        height: 100%;
        width: 100%;
        clicked => {
            popup.show();
        }
    }
}

```
