## Maven Archetype开发

## what is Maven archetype？这里摘自
* https://maven.apache.org/guides/introduction/introduction-to-archetypes.html 官网介绍
```
In short, Archetype is a Maven project templating toolkit. An archetype is defined as an original pattern or model from which all other things of the same kind are made. The name fits as we are trying to provide a system that provides a consistent means of generating Maven projects. Archetype will help authors create Maven project templates for users, and provides users with the means to generate parameterized versions of those project templates.
简而言之，Archetype 是一个 Maven 项目模板工具包。一个原型被定义为一个原始的模式或模型，所有其他同类的东西都是从这个模式或模型制造出来的。这个名字很合适，因为我们正在尝试提供一个系统，它提供了生成 Maven 项目的一致方法。Archetype 将帮助作者为用户创建 Maven 项目模板，并为用户提供生成这些项目模板的参数化版本的方法。
Using archetypes provides a great way to enable developers quickly in a way consistent with best practices employed by your project or organization. Within the Maven project, we use archetypes to try and get our users up and running as quickly as possible by providing a sample project that demonstrates many of the features of Maven, while introducing new users to the best practices employed by Maven. In a matter of seconds, a new user can have a working Maven project to use as a jumping board for investigating more of the features in Maven. We have also tried to make the Archetype mechanism additive, and by that we mean allowing portions of a project to be captured in an archetype so that pieces or aspects of a project can be added to existing projects. A good example of this is the Maven site archetype. If, for example, you have used the quick start archetype to generate a working project, you can then quickly create a site for that project by using the site archetype within that existing project. You can do anything like this with archetypes.
使用原型提供了一种很好的方式，使开发人员能够以与项目或组织所使用的最佳实践一致的方式快速开发。在 Maven 项目中，我们通过提供一个示例项目来展示 Maven 的许多特性，同时向新用户介绍 Maven 所采用的最佳实践，从而使用原型尽可能快地让我们的用户启动并运行。在几秒钟内，一个新用户就可以拥有一个可以工作的 Maven 项目作为跳板，用于研究 Maven 中的更多特性。我们还尝试使原型机制添加，这意味着允许在原型中捕获项目的某些部分，以便可以将项目的某些部分或方面添加到现有项目中。Maven 站点原型就是一个很好的例子。例如，如果使用快速启动原型生成工作项目，那么可以通过使用现有项目中的站点原型快速创建该项目的站点。你可以用原型做任何类似的事情。
```
* 实际上就是通常所说的脚手架，这里是指脚手架的开发。

## Guide to Creating Archetypes
* 可以去看看Maven的官网，按照上面的引导，去创建自己的第一个Maven archetype。

## 记录第一个maven archetype

### First Step: 创建一个Maven工程
* 第一步，是创建一个Maven工程。这个Maven工程就是脚手架，其目的是为了快速创建工程而创建的maven archetype；
    * 可以使用下列方式去创建
        `mvn archetype:generate -DarchetypeGroupId=org.apache.maven.archetypes -DarchetypeArtifactId=maven-archetype-archetype -DarchetypeVersion=1.3`
    * 针对上述做个说明




