# kubernetes-example
一些kubernetes的部署例子：zookeeper activemq HPA ELK wordpress Redis RBAC ...

## Background ##



## zookeeper with activemq ## 
这里参考了官方的zookeeper集群的部署，并完成与activemq的结合；使用了statefulset与headless service部署了zookeeper与activemq，使用sed命令与configmap资源对象完成了配置文件的修改；<br>
1.配置pv<br>
```kubectl apply -f pv.yaml```
<br>
2.配置configmap（zoo.cfg）<br>
```kubectl create configmap zk-cm2 --from-file=zoo.cfg```
<br>
3.部署zookeeper<br>
```kubectl apply -f zookeeper-my.yaml```
<br>
4.部署activemq<br>
```kubectl apply -f activemq.yaml```
<br>

## Redis ##


## RBAC example ##


## ELK example ##


## wordpress ##

## Other ##
