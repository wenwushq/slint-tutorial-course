## ContextMenuArea特有属性
* enabled：是否可用，默认值为true

## 和其他控件共有属性
* width：窗口固定宽度 例 800px
* height：窗口固定高度 例 600px

## 方法
* show(Point)：在Point位置上显示菜单
* hide()：隐藏菜单

## 参考
* [Menu](./../控件/Menu.md)
* [MenuItem](./../控件/MenuItem.md)
* [MenuSeparator](./../控件/MenuSeparator.md)

## 注意
1. ContextMenuAre为非可视化窗体，必须要且只有一个Menu子组件，否则编译会出错

## 示例代码
```
export component MainWindow inherits Window {
    ContextMenuArea {
        enabled: true;
        Menu {
            MenuItem {
                title: @tr("Cut");
                activated => { debug("Cut"); }
                icon: @image-url("./assets/cut.png");
                checkable: true;
                checked: true;
            }
            MenuItem {
                title: @tr("Copy");
                activated => { debug("Copy"); }
                icon: @image-url("./assets/copy.png");
                checkable: true;
                checked: false;
            }
            MenuItem {
                title: @tr("Paste");
                activated => { debug("Paste"); }
                icon: @image-url("./assets/paste.png");
            }
            MenuSeparator {}
            Menu {
                title: @tr("Find");
                MenuItem {
                    title: @tr("Find Next");
                }
                MenuItem {
                    title: @tr("Find Previous");
                }
            }
        }
    }
}
```
