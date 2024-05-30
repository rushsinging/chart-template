# 平台组应用Chart 标准模板

## 模板列表

* [单应用版](./app)
* [celery应用版](/celery)
* [base](./base)
* [StatefulSet](./statefulset)
* 多应用版（TODO）

## 使用方法

增加helm repo: `helm repo add platform http://charts-huawei.guokr.net/guokr/platform`

使用的是基本原理是利用helm 在部署时可以用本地`values.yaml` 文件覆盖chart 内文件的方式部署自己的应用这一功能。

[CI/CD工具](https://versioning.guokr.net) 就是利用这个实现的

### Helm 

    helm upgrade -i -f <YOUR_VALUES.yaml> --force <RELEASE_NAME> platform/app --tiller-namespace
### Asgard

    # 完成asgard init 操作
    asgard deploy -r <RELEASE_NAME> -f <YOUR_VALUES.yaml> app

## 引用

* [平台架构组资源索引](https://git.guokr.net/platform/readme)
* [Kubernets 部署工具](https://git.guokr.net/platform/asgard)

# chart-template
