# Maven中plugins和pluginManagement的区别

## 摘要
* 在刚学习maven的时候，如果是单模块的话，可能不会注意到这个问题。但是存在父子模块的时候，会存在这样的两个问题：
    * pluginManagement标签 和 plugins标签的区别是什么？
    * dependencyManagement标签 和 dependencys标签的区别是什么？
* 为了彻底搞清楚这两个问题，以及在maven中是否还存在类似的标签？此篇文档做以记录。
## 内容
* 遇到这个问题一定是在存在父子模块的maven项目中，单模块中是不存在这个问题的。
* 先来看maven中 pluginManagement tag 的描述：
    > pluginManagement: is an element that is seen along side plugins. Plugin Management contains plugin elements in much the same way, except that rather than configuring plugin information for this particular project build, it is intended to configure project builds that inherit from this one. However, this only configures plugins that are actually referenced within the plugins element in the children. The children have every right to override pluginManagement definitions.
    > PluginManagement: 是一个可以在侧面插件中看到的元素。Plugin Management 包含插件元素的方式大致相同，只不过它不是为这个特定的项目构建配置插件信息，而是为从这个项目继承的项目构建配置插件信息。但是，这只配置子插件中的 plugins 元素中实际引用的插件。子代完全有权覆盖 pluginManagement 定义。
* maven中没有对 plugins tag做描述。
* 实际上在上述的描述中已经解释了其之间的差别。当项目中存在父子模块时，如果父子模块都需要某个插件。可以在父pom中先声明插件，使用的tag是pluginManagement。这里仅仅是声明的作用，不会引入。当前父项目中也是不能使用这个插件的，其子pom是会去继承的，但是不会引入，也就是说子项目是不能直接使用这个插件的。子项目想使用，只能去在plugins tag中去引入。
* dependencyManagement tag 和 dependencys同理。
## 引用  
*  [stack overflow: What is pluginManagement in Maven's pom.xml?](https://stackoverflow.com/questions/10483180/what-is-pluginmanagement-in-mavens-pom-xml)
* [maven官网plugins描述](https://maven.apache.org/pom.html#Plugins)
* [maven官网Plugin_Management描述](https://maven.apache.org/pom.html#Plugin_Management)