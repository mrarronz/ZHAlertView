# ZHAlertView

一个非常简单的自定义alertView，支持横竖屏，自定义主题颜色

竖屏显示

![image](https://github.com/mrarronz/ZHAlertView/raw/master/screenshot/portrait.gif)

横屏显示

![image](https://github.com/mrarronz/ZHAlertView/raw/master/screenshot/landscape.gif)


##使用方法

与系统UIAlertView类似的调用方法：

```objective-c
ZHAlertView *alert = [[ZHAlertView alloc] initWithTitle:@"提示啦啦啦啦啦啦啦"
                                                    message:@"您确定要删除吗？删除后将无法恢复"
                                                   delegate:self
                                          cancelButtonTitle:@"确定"
                                           otherButtonTitle:nil];
[alert show];
```

##问题

这个demo project是根据项目里web版的样式写着玩的，没有做太多扩展。
1、只支持最多两个button的情况，且样式比较固定
2、代码中动画非常简单，使用了iOS7的spring动画，基于UIKit。同时用到Masonry简化autolayout代码，动画使用了transform。在iOS7中transform的动画和autolayout混用会出现问题，iOS8+应该是正常的，iOS9测试运行正常，因此这个demo project基于iOS8以上系统构建。
