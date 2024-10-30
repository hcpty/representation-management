# Readme
Architecture style of World Wide Web app.

### Representation Storage, Processing and Transfer

直到2000年左右，万维网应用的架构还是Representation Transfer，那个时候的万维网应用还不怎么支持资源的在线编辑，仅支持资源的在线浏览，相应的存储架构也比较简单。

到了21世纪，随着移动互联网的兴起，在线编辑开始流行，于是万维网应用的架构开始逐渐演变成了Representation Processing and Transfer，其中Processing的含义是Viewing and Editing，用专业术语说就是Read and Write，一种比较流行的说法是Create/Reade/Update/Delete (CRUD)，相应的资源的存储架构也发生了一些变化，于是得到了今天的万维网架构：Representation Storage, Processing and Transfer。

如今，开发一个万维网应用一般需要三个步骤：
- 第1步，考虑资源的存储。
- 第2步，考虑资源的处理，为应用要加工的各类资源编写对应的Representation Processor，封装成一个library，为应用程序提供Representation Processing服务。
- 第3步，考虑资源的传输，根据对网络传输协议类型的需求，编写支持各种网络传输协议的Representation Transferor，令其使用Representation Processing服务并进行接口转换。

### Credits
- [Representational State Transfer (REST) - Fielding Dissertation](https://ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm)
