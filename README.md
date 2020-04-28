# k8的监控
**这里是k8s安装监控的yml文件和线上的模板(json文件)**
## 第一步
**安装nfs或使用其他nfs** 
**centos里运行:yum install -y rpcbind nfs-utils**  
**需要配置可加载的目录/nfs/prometheus/data,/nfs/grafana/data并配置k8s里的prometheus和grafana应用有权限加载和可以读写这些目录,就是 showmount -e 显示/nfs/grafana/data    172.0.0.0/8
/nfs/prometheus/data 172.0.0.0/8
   同时修改prometheus.yaml和grafana.yaml里的nfs的ip为真实的nfs的ip(目前写172.16.62.158)**
## 第二步 
**安装namespace.yaml或执行kubectl apply -f namespace.yaml**
## 第三步 
**在k8s里页面运行node-exporter.yaml或执行kubectl apply -f node-exporter.yaml**
## 第四步 
**在k8s里页面运行prometheus.yaml或执行kubectl apply -f prometheus.yaml**
## 第五步 
**在k8s里页面运行grafana.yaml或执行kubectl apply -f grafana.yaml**
## 第六步 
**配置nginx指向Grafana的service**
## 第七步 
**配置Grafana的数据源指向prometheus(本例是:http://prometheus-service.arms-prom:9090)**
## 第八步 
**配置Grafana的显示模板(就是json文件部分)**
