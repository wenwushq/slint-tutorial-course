## MenuBar特有属性
* 无

## 和其他控件共有属性
* 无

## 方法
* 无

## 参考
* [Menu](../控件/Menu.md)
* [MenuItem](../控件/MenuItem.md)
* [MenuSeparator](../控件/MenuSeparator.md)

## 注意
1. 无

## 示例代码
```
export component MainWindow inherits Window {
    MenuBar {
        Menu {
            title: @tr("文件");
            MenuItem {
                title: @tr("新建");
                activated => { file-new(); }
            }
            MenuItem {
                title: @tr("打开");
                activated => { file-open(); }
            }
        }
        Menu {
            title: @tr("编辑");
            MenuItem {
                title: @tr("复制");
                checkable: true;
                checked: true;
            }
            MenuItem {
                title: @tr("粘贴");
            }
            MenuSeparator {}
            Menu {
                title: @tr("查找");
                MenuItem {
                    title: @tr("在文档中查找...");
                }
                MenuItem {
                    title: @tr("查找下一个");
                }
                MenuItem {
                    title: @tr("查找上一个");
                }
            }
        }
    }

    callback file-new();
    callback file-open();
}
```
