
首先为了提高处理速度，处理器不会直接和内存进行同学，而是先将内存里的数据读取到内部缓存（L1，L2等）中再进行操作，然后为了避免缓存不一致的情况，多处理器
之间会有一个缓存一致性协议，他们通过嗅探技术得知该缓存对应的内存地址被修改，就会将自己缓存的数据设置为无效，当需要再次修改这个数据时，会再从内存中取出。

volatile利用了这个特性：
被volatile修饰的数据会执行一条带有lock前缀的命令，这个命令会引发两件事情：
1，将当前处理器缓存行的数据协会到系统内存中
2，有了1的操作，再根据最上面的原理，就会使得被volatile修饰的共享数据能被准确和一致的更新
