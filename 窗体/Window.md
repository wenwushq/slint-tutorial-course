# Window特有属性
* title：窗口标题 例 "Slint 窗口示例"
* always-on-top：窗口始终保持在其他窗口之上，默认值为false
* full-screen：窗口占满整个屏幕，默认值为false
* visible：窗口是否可见，默认值为true，设置为false后窗口将隐藏
* background：窗口背景颜色，默认值为#ffffff（白色）
* default-font-family：默认字体，默认值为系统默认字体
* default-font-size：默认字体大小，默认值为12px
* default-font-weight：默认字体粗细，默认值为400（正常）取值范围为100-900，数值越大字体越粗
* icon: 窗口图标，默认值为无图标，**支持png、svg图片** 例 @image-url("assets/icon.png")
* no-frame: 窗口是否有边框和标题栏 默认值为false
* resize-border-width: 调整窗口大小时边框的宽度，默认值为5px

## 和其他控件共有属性
*  width：窗口固定宽度 例 800px
*  height：窗口固定高度 例 600px
*  preferred-width：窗口首选宽度 例 800px
*  preferred-height：窗口首选高度 例 600px
*  min-width： 窗口最小宽度 例 400px
*  min-height：窗口最小高度 例 300px
*  max-width：窗口最大宽度 例 800px
*  max-height：窗口最大高度 例 600px

## 注意：
1. no-frame和full-screen不要同时设置为true，否则窗口不容易关闭掉，造成系统假卡死
1. 设置了width和height属性后，标题栏上的最大化按钮不可用
1. 异形窗口需要设置属性：no-frame: true和background: #00000000