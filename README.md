## 一、NBU物理架构

NBU主要由四个部分硬件组成：Master Server、OPS报表服务器、虚拟带库和物理带库。

## 二、背景

数据备份对生产来说很重要，关键时候能起到大作用，可以将生产因为各种原因导致数据丢失的风险降到最低。NBU就是进行数据备份及恢复的系统。既然数据备份这么重要，每天也需要对备份的执行情况进行监控，本文介绍的就是如何在报表服务器上配置邮件通知。

## 三、邮件配置

### 1.登陆报表服务器

登陆地址：https://172.16.xx.xx，用户名为admin

![image-20210811163053747](https://i.loli.net/2021/08/11/kXAwLnIxmBjiU9C.png)

### 2.新增邮件收件人

点击‘Add’新增邮件收件人

![image-20210811163302754](https://i.loli.net/2021/08/11/HyR52K36MoT8194.png)

收件人信息如图：

![image-20210811163504107](https://i.loli.net/2021/08/11/OYrLcDwCgMlAmou.png)

### 3.配置邮件服务器

![image-20210811163902330](https://i.loli.net/2021/08/11/P6q4xsjNDgZHFW2.png)

如图填写邮件服务器信息，主要有邮件服务器的ip地址、端口和发件人

### 4.配置报告模板

![image-20210811164006392](https://i.loli.net/2021/08/11/pgeRF5ELYx6bmrM.png)

这里已经有了两个模板，就省略配置步骤

### 5.配置发送策略

![image-20210811164147041](https://i.loli.net/2021/08/11/OtKMfkuvlj4ynN5.png)

选中‘job_all’然后‘Edit’

![image-20210811164317085](https://i.loli.net/2021/08/11/1eETMvs53XiOtmL.png)

next

![image-20210811164352425](https://i.loli.net/2021/08/11/3ePGsdVSkI6bwHN.png)

next

![image-20210811164518965](https://i.loli.net/2021/08/11/uplInOeNhXkTQo8.png)

配置邮件接收人和抄送对象，这些发送对象列表都为之前的新增邮件收件人

![image-20210811164733907](https://i.loli.net/2021/08/11/rMiWfJkwQ83I2sU.png)

选择报告发送模板，继续next并save，完成发送策略配置。

### 6.配置发送时间

![image-20210811164856018](https://i.loli.net/2021/08/11/GQU93rJNpCbBW8Y.png)



发送时间配置选择很丰富，这里是每天8:30发送一次

![image-20210811164954829](https://i.loli.net/2021/08/11/DU6xlEMC9Wf8Rd3.png)

## 四、效果展示

有见效果展示如图：

![image-20210811165145356](https://i.loli.net/2021/08/11/KrtZFqNTz7lMOma.png)

![image-20210811165215577](https://i.loli.net/2021/08/11/y3dZb95BLYe8JEo.png)

![image-20210811165300254](https://i.loli.net/2021/08/11/B6EJcfdwejvYCIa.png)

