### CMake概述

CMake是一个项目构建工具，并且是跨平台的。关于项目构建工具还有Make，大多数IDE软件都集成了Make，如VS的nmake、Linux下的GNU Make、Qt的qmake等。但是，makefile文件通常依赖于当前的编译平台，而且编写makefile文件工作量较大，解决依赖关系时也比较复杂。

CMake允许开发者指定整个工程的编译流程，再根据编译平台，**自动生成本地化的Makefile文件和工程文件**，最后只需要根据自动生成的makefile文件`make`编译即可。可以把CMake看作自动生成makefile文件的工作。

Make和CMake的编译流程：

Make：项目源码 --> 手动编写Makefile文件 --> Makefile文件 --> 执行make命令 --> 生成目标文件。

CMake：项目源码 --> CMakeLists.txt文件 --> 执行cmake命令生成Makefile文件 --> Makefile文件 --> 执行make命令 --> 生成目标文件。
