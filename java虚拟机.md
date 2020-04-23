
###### 现在的jvm 配置
Xmn1024m -Xms4096m -Xmx4096m -XX:PermSize=64M -XX:MaxPermSize=128M

###### gc
使用命令:  java -XX:+PrintCommandLineFlags -version
-XX:InitialHeapSize=2107937728 -XX:MaxHeapSize=32210157568 -XX:+PrintCommandLineFlags -XX:+UseCompressedClassPointers 
-XX:+UseCompressedOops 
-XX:+UseParallelGC 
java version "1.8.0_111"
Java(TM) SE Runtime Environment (build 1.8.0_111-b14)
Java HotSpot(TM) 64-Bit Server VM (build 25.111-b14, mixed mode)
