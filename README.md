# Readme
Architecture style of World Wide Web.

### Representation Storage, Management and Transfer

直到2000年左右，万维网的架构还是Representation Transfer and Viewing，那个时候的万维网还不怎么支持资源的在线编辑，只支持资源的在线浏览。

到了21世纪，随着移动互联网的兴起，在线编辑开始流行，于是万维网的架构开始逐渐演变成了Representation Transfer and Management，其中Management的含义是Viewing and Editing，用专业术语说就是Read and Write，一种比较流行的说法是Create/Reade/Update/Delete (CRUD)，相应的资源的存储架构也发生了一些变化，于是得到了今天的万维网架构：Representation Storage, Management and Transfer。

如今，开发一个万维网应用一般需要三个步骤：
- 第1步，考虑资源的存储。
- 第2步，考虑资源的管理，为应用要管理的各类资源编写对应的Representation Manager，封装成一个library，并基于这个library，建立和运行独立的service，为使用多种网络协议的应用程序提供Representation Management服务。
- 第3步，考虑资源的传输，按照需求，编写支持多种网络协议的Representation Transferor，令其使用Representation Management服务并进行接口转换。

### Credits
- [Representational State Transfer (REST) - Fielding Dissertation](https://ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm)
- [Reactor pattern - Wikipedia](https://en.wikipedia.org/wiki/Reactor_pattern)
