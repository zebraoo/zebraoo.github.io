+++
title = 'android相关'
date = 2023-11-15
tags= ['Android']
+++

### 无法下载安装gradle
修改gradle-wrapper.properties文件
替换使用腾讯云镜头
# 腾讯云
distributionUrl=https\://mirrors.cloud.tencent.com/gradle/gradle-6.6.1-bin.zip

# 默认国外
distributionUrl=https\://services.gradle.org/distributions/gradle-6.6.1-bin.zip

下载不了gradle，网上搜出来都是修改settings.gradle文件,配置阿里云镜像，下载依然超时。
要了解settings.gradle文件主要下载的内容

### 设置代理 修改gradle-wrapper.properties文件 
systemProp.http.proxyHost=127.0.0.1
systemProp.http.proxyPort=7890
systemProp.https.proxyHost=127.0.0.1
systemProp.https.proxyPort=7890
