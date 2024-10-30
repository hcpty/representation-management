# Readme
An app architecture.

万维网应用的本质是Representation Management。由于又涉及到资源的传输，所以又包含Representation Transfer的部分。

Representation Manager负责manage资源，而Representation Transferer负责transfer资源，两者都对资源进行操作，但两者的职责截然不同。

- 首先考虑资源的存储。
- 然后针对不同的资源类型编写不同的Representation Manager类。
- 然后


各种应用的本质就是Representation Management和Representation Transfer。各种的本质是进行接口转换。职责分开。

对Database的操作是重IO的，而并发对重IO的操作。拆分，按资源粒度拆分，而非并发。尽量独占执行，适当并发，避免过度并发。

针对各种资源类型编写库，方便程序调用，主动的Representation Manager和被动的Representation。通过MQ为各种提供服务，不必和特定的协议绑定关系，协议只需要执行接口转换。

### Credits
- [Representational State Transfer (REST) - Fielding Dissertation](https://ics.uci.edu/~fielding/pubs/dissertation/rest_arch_style.htm)
- [Reactor pattern - Wikipedia](https://en.wikipedia.org/wiki/Reactor_pattern)
