
# 资源管理

"`资源管理`"是指可以将任意文件/目录打包为`Golang`源码文件，并且编译到可执行文件中，随着可执行文件发布。资源文件在程序启动时将会自解压释放到内存中，供程序只读访问，可以将它当做基于内存的文件管理器。同时，`GF`的资源管理特性也支持将文件/目录打包为独立的二进制资源文件使用。由于资源文件在程序运行时是基于内存的文件操作，没有磁盘IO的开销，因此其文件操作效率非常高。


资源管理特性由`gres`模块实现，该模块具有以下特点：
1. 可将任意的文件/目录打包为`Go`文件，支持自定义加解密；
1. 打包的`Go`文件/资源文件自动压缩，常见`css/js`等文件可达到`50~90%`的压缩率；
1. 资源管理器内容完全基于内存，并且内容只读，无法动态修改；
1. 资源管理器默认整合支持到了`WebServer`、配置管理、模板引擎模块中；
1. 任意文件如网站静态文件、配置文件等可编译到二进制文件中，也可编译到发布的可执行文件中；
1. 开发者可只需编译发布一个可执行文件，除了方便了软件分发，也为保护软件知识产权内容提供了可能；


**使用方式**：
```go
import "github.com/gogf/gf/os/gres"
```

**接口文档**： 

https://godoc.org/github.com/gogf/gf/os/gres



