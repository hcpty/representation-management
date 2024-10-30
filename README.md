# Readme
Architecture style of World Wide Web app.

### Representation Storage, Processing and Transfer

直到2000年左右，万维网app的架构风格还是Representation Transfer，那个时候的万维网app还不怎么支持资源的在线编辑，仅支持资源的在线浏览，相应的存储架构也比较简单。

到了21世纪，随着移动互联网的兴起，在线编辑开始流行，于是万维网app的架构风格开始逐渐演变成了Representation Processing and Transfer，其中Processing的含义是Viewing and Editing，相应的资源的存储架构也发生了一些变化，于是得到了今天的万维网app架构风格：Representation Storage, Processing and Transfer。

如今，设计和实现一个万维网app一般需要三个步骤：
- 第1步，考虑资源的存储。
- 第2步，考虑资源的加工，为app要加工的各类Representation编写对应的Representation Processor，为app提供Representation Processing服务。
- 第3步，考虑资源的传递，根据对特定的网络传输协议类型的需求，编写支持对应的网络传输协议的Representation Transferor，令其中的Event Handler使用Representation Processing服务并进行接口转换。

### Credits
- [Redundant Array of Independent Database Nodes - Hcpty](https://github.com/hcpty/redundant-array-of-independent-database-nodes)
- [Message Queue Task - Hcpty](https://github.com/hcpty/message-queue-task)
- [Representational State Transfer (REST) Architectural Style - Fielding Dissertation](https://ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm)
