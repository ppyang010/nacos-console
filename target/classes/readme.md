如果出现报错java.net.UnknownHostException: jmenv.tbsite.net
需要在启动的时候设置启动模式
可以在ide的vm配置增加：-Dnacos.standalone=true
