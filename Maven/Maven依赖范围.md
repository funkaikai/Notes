## Maven依赖范围理解

## 摘要
* 主要学习内容来自《Maven实战》


## 内容
* Maven在编译项目时需要用到一套classpath;
    * 在编译项目时，想想都要用到哪些classpath?编译是指将源代码转换成字节码。
* Maven在编译和执行测试时会使用另外一套classpath;
    * 这边能理解的哈，在执行测试的时候，需要加载测试的相关jar依赖。
* 实际在运行maven项目的时候又会使用到另外一套classpath；
    * 为啥实际运行mavne的时候，又会用到另外一套classpath呢？
* 不同的依赖范围就是用来控制依赖与这三种classpath的关系。maven存在以下几种依赖范围：
  * compile:默认的。
