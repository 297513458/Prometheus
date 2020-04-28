# k8的监控
**这里是k8s安装监控的yml文件和线上的模板(json文件)**
## 第一步
**安装nfs或使用其他nfs**
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
