## TimePickerPopup特有属性
* title：时间选择弹出框的标题
* time：默认时间 如：time: { hour: 6, minute: 30, second: 25 };
* close-policy：关闭策略 取值说明：close-on-click（点击即可关闭弹窗）；close-on-click-outside（点击弹窗外部即可关闭弹窗）；no-auto-close（不自动关闭弹窗，需要手动调用popup.close()方法来关闭弹窗）

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
* 无

## 回调
* accepted(date)：当用户点击“确定”按钮时触发
* canceled()：当用户点击“取消”按钮时触发

## 注意
1. 要使用TimePickerPopup组件，必须要导入：import { TimePickerPopup } from "std-widgets.slint";

## 示例代码
```
import { TimePickerPopup, Button} from "std-widgets.slint";

export component MainWindow inherits Window {
    width: 400px;
    height: 600px;

    Button {
        text: "打开 时间选择弹出框";

        clicked => {
            time-picker.show();
        }
    }

    time-picker := TimePickerPopup {
        x: (root.width - self.width) / 2; //水平居中
        y: (root.height - self.height ) / 2; //垂直居中
        close-policy: PopupClosePolicy.no-auto-close; //设置弹出框不自动关闭
        title: "时间选择弹出框"; //时间选择弹出框的标题
        //use-24-hour-format: false; //是否使用24小时制
        //time: { hour: 6, minute: 30, second: 25 }; //默认时间
        
        accepted(date) => { //当用户点击“确定”按钮时触发
            debug("选择的时间: ", date.hour, date.minute, date.second);
        }
        canceled => { //当用户点击“取消”按钮时触发
            time-picker.close();
        }
    }
}
```