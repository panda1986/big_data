### 大数据分析技术汇总

* spark API https://spark.apache.org/docs/2.3.0/api/scala/index.html#org.apache.spark.SparkContext

#### 名词解析
  * spark standalone 单例模式，指的是spark集群独立部署模式，没有用yarn
  * HA 高可用，一般是指某个产品的HA解决方案
  * Hadoop MapReduce 
  * 函数式编程
  * 聚合
  * RDD: 弹性分布式数据集，实际计算是分布在各个节点上的，而RDD的结算过程都是在Driver程序中定义的，所以代码从Driver分发至各计算节点有一个过程，可以分为4步：
       * 在Driver节点上序列化代码
       * 传送至各计算节点
       * 在计算节点上反序列化
       * 执行
   * RDD运算    
       * 所有对RDD的函数调用，虽然代码上看起来是在Driver程序中运行的，但实际计算都不在本地。
       * 每个RDD操作都会被转换成Job分发至集群的执行器进程上运行，即便是单机本地运行模式，也是在单独的执行器进程上运行，与Driver程序隶属于不用的进程
       * 每个Job的执行，都会经历序列化、网络传输、反序列化和运行的过程
       * 禁忌：RDD操作不能嵌套调用，即在RDD操作传入的函数参数的函数体中，不可以出现RDD调用。
   
   
       
