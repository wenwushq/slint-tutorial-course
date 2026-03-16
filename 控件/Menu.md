## Menu特有属性
* title：菜单名称 例 "文件" 默认值为""
* enabled：菜单是否可用
* icon: 图标，默认值为无图标，**支持png、svg图片** 例 @image-url("assets/icon.png")

## 示例代码
```
Menu {
    MenuItem {
        title: @tr("Cut");
        activated => { debug("Cut"); }
        icon: @image-url("./assets/cut.png");
        checkable: true;
        checked: true;
    }
}
```