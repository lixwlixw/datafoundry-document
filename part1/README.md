#DF安装 <br/>

##主机方案 <br>

master*3  etcd*3  node*2  lb*1（每台master机器上同时搭master和etcd）<br>
master负责整个集群调度编排资源管理 <br>
master1 <br>
master2 <br>
master3 <br>
etcd负责集群信息存储 k/v (master和etcd可以装在一起) <br>
etcd1 <br>
etcd2 <br>
etcd3 <br>
lb负责master的load balance（单master方案不需要lb）<br>
loadbalance <br>
node负责执行任务 <br>
node1 <br>
node2 <br>
ansible负责跑安装集群的ansible-playbook,统一配置集群等（三台master任选一台）<br>
master1 <br>
集群外一台机器单独使用部署本地的docker镜像仓库registry，以及service-broker的etcd <br>
dockerregistry <br>
