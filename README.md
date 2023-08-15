# React Server Components Demo 


## 本地启动

  ```
  npm install
  npm start
  ```

打开 http://localhost:4000.


## Notes about this app

这个演示应用程序是一个名为React Notes的便条应用程序。它由几个主要部分组成：

- 它使用了一个Webpack插件（未在此存储库中定义），该插件允许我们只在构建构件中包含客户端组件
- 一个Express服务器，它：
  - 提供应用程序中使用的API请求
  - 将Server Components渲染成我们可以在客户端上读取的特殊格式
- 一个React应用程序，其中包含用于构建React Notes的Server和Client组件

这个演示是建立在我们的Webpack插件之上的，但这不是我们在稳定后使用Server Components的设想方式。它们旨在用于支持服务器渲染的框架，例如Next.js。这只是一个早期的演示 - 真正的集成将在接下来的几个月中开发。在[公告文章](https://reactjs.org/server-components)中了解更多信息。

### 有趣的尝试

- 在侧边栏中将鼠标悬停在便条上并单击展开/折叠切换，尝试展开便条。然后创建或删除一个便条。展开的便条会发生什么变化？
- 在编辑时更改一个便条的标题，并观察侧边栏中对现有项目的编辑动画效果。如果您编辑列表中间的一个便条会发生什么?
- 搜索任何标题。在搜索输入框中仍然有搜索文本的情况下，创建一个标题与搜索文本匹配的新便条。会发生什么?
- 在慢速3G网络环境下进行搜索，观察内嵌的加载指示器.
- 在两个便条之间来回切换。观察下次再切换它们时我们不会发送新的请求.
- 取消NoteServer.js和/或NoteList.server.js中的fetch('http://localhost:4000/sleep/....')调用的注释，引入人为延迟，触发Suspense效果.
