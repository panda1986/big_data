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
