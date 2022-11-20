1.
如果出现报错java.net.UnknownHostException: jmenv.tbsite.net
需要在启动的时候设置启动模式
可以在ide的vm配置增加：-Dnacos.standalone=true

也可以在main方法中通过环境变量的形式 设置 单机启动
System.setProperty("nacos.standalone", "true");

解释 https://github.com/alibaba/nacos/issues/2902

2.
修改 console/pom.xml
由于不在使用 nacos bom 管理，需要给所有依赖坐标增加版本号

由于 nacos-config /nacos-naming 等包没有上传至中央参考 无法下载到，groupId 变更为 com.pig4cloud.nacos 即可下载

参考文章: https://juejin.cn/post/6875564595080069133