将pahomqtt这个整个目录拷贝到你的项目中
这个目录的BUILD.gn文件已经写好默认会在pahomqtt目录中生成pahomqtt_static静态库

要使用相关函数应用头文件即可,你应该在更上层的BUILD.gn文件中将这个库添加进去,类似于这样的地方
```c++
lite_component("app") {
    features = [
        "pahomqtt:pahomqtt_static",
    ]
}
```