# 青云四方支付系统

**青云四方支付系统-链接资金的利器**

## 1.运营端

### 1.1 登录界面

![image](https://github.com/user-attachments/assets/a8f21cd0-a761-4caf-b77e-fb77e9e18d2d)


### 1.2 运营后台界面

![image](https://github.com/user-attachments/assets/31ddaa3e-46ec-4592-93a5-4eee59582e61)


**运营后台主要包括**

### 1.商户管理

​	商户管理主要用来，创建商户，也就是开户，配置产品费率，以及配置产品对应跑的通道，中间有利润差，才是我们盈利的根本。

#### 1.1 商户列表
![image](https://github.com/user-attachments/assets/842f1e8e-f9c7-426b-b118-be9704d3e93f)


#### 1.2 应用列表

![image](https://github.com/user-attachments/assets/02f867c9-a0e2-4b0b-b02a-98d5c442db99)


#### 1.2.3 产品列表

![image](https://github.com/user-attachments/assets/b4c8016b-8966-4f86-a6a3-0bd68b7cde77)


**产品配置通道**<span style="color:red;font-weight:bold;backgroud:yellow">（一个产品可以配置多个通道，这里就是运营人员需要重点关注的点）</span>

![image](https://github.com/user-attachments/assets/2f2a2d97-f65c-4b6e-8ece-aa19fa30b8cd)


### 1.2.4 商户下单测试界面

商户下单测试可以快速通过不同商户，选择不同的产品，以及不同的通道，来进行**测试**或者**正式下单**，可以帮助大家快速获取下单的结果。

这里既可以<span style="color:red">针对商户对接</span>，测试；也可以<span style="color:red">针对通道对接</span>，测试。

![image](https://github.com/user-attachments/assets/9169e8fb-d300-4ed4-b380-ea44497ecd99)


### 2.订单管理

订单列表，可以实时查看当前系统订单情况。

1.可以查看每个商户，每个产品，每个通道，商户费率，通道费率，平台成本，平台利润，支付状态，回调状态，补单状态等。

![image](https://github.com/user-attachments/assets/0aa0dbf0-df7c-4d82-bf51-86ebf3904b25)


2.打开实时统计，可以查看当前商户或产品或通道的统计情况

![image](https://github.com/user-attachments/assets/390f17b1-7dd8-4f6c-8670-189448172cf7)


3.当供应商已经明确支付成功（有时金额不对的情况下），但没有回调成功时，可以通过人工补单操作，此时可以在备注信息中**说明情况**。**补单密码是跟系统分开的**。补单并不会修改订单金额，只是会将系统订单状态从支付中，改为已支付。补单有些情况需要跟商户沟通，是否需要进行补单。**补单的目的，除了改变系统状态之外，也会向商户发起回调通知。**

![image](https://github.com/user-attachments/assets/5d4bbcc0-f5ad-4623-b55c-05cbe402e49a)

![image](https://github.com/user-attachments/assets/5671431f-3949-4238-852f-40c94ed30872)



### 3.支付配置
#### 3.1 供应商管理

​      这里主要是用来对接通道的配置。开发这块的目的是为了：**存在有优势的通道，需要我们去对接通道，但是，往往技术人员响应不及时，导致我们运营团队错失了很多赚钱的机会**。那我们想：**如果对接通道，不需要技术参与，我们运营人员能够自己对接，那该多好呀**。在此应用场景下，供应商管理对接，就由此而生。
![image](https://github.com/user-attachments/assets/9eb1b2e1-9397-4fab-8c5d-672724a40189)

**参数映射配置：**

**第一步，供应商提供信息**。包括（供应商开我们，开的户，密钥，下单地址，查单地址，等信息），具体还得看供应商的接口文档。
![image](https://github.com/user-attachments/assets/1c419628-59f8-41f8-bc37-ea2325681b52)
**第二步：映射配置**。包括**下单**、**查单**、**回调**，这三部分。下单包含，请求参数，返回参数配置；查单也一样，回调只有接收参数配置，而且每个配置都有说明。**前期需要我们技术支持一下**，带着一起配置几个通道方，以后运营人员就可以自己配置了。
![image](https://github.com/user-attachments/assets/9c22274e-a476-4052-8c70-91d2a1dd8f7d)
![image](https://github.com/user-attachments/assets/5b755c21-e912-4485-9dc2-892d12c5fc74)
![image](https://github.com/user-attachments/assets/4aaa5cd4-4de5-4667-88f1-9fe4b99b2cb8)
#### 3.2 通道管理

​    上述通过供应商对接后，我们需要将供应商提供的通道信息添加进来即可。选择指定的供应商，供应商提供的通道编码、通道名称、通道费率、收款类型（分为固定额度只能是指定的额度，比如：30|50|100|200和浮动额度，区间范围比如：1-9999）、是否启用。这里加了一个**回收站**：**主要是方便管理，只展示有用的通道**。暂时不需要的可以进行回收操作，到回收站中的通道管理进行查看。
![image](https://github.com/user-attachments/assets/ee876fe0-ca5c-40f7-8734-b288f9d13fa3)
![image](https://github.com/user-attachments/assets/38aaceec-cc0c-4ad4-8441-77fc6465267e)
#### 3.3 产品管理

​	**产品**，在四方系统可以认为是一个**大通道**，我们给到商户的产品编码（也可以叫通道编码）和产品名称（也可以叫通道名称）。也就是**对外推广和营销**的大通道。这里由我们运营人员自定义一套产品（大通道）规则。

​	可以提前自定义好，产品编码（大通道编码）和产品名称（大通道名称）。
![image](https://github.com/user-attachments/assets/4c066eeb-db7b-46b7-b680-1453c897b395)


### 4.机器人管理



### 5.回收站管理



### 6.结算管理



### 7.系统配置






## 请联系飞机：<a href="https://t.me/AXPay06" target="_blank">商务合作</a>

## 有什么需求，您也可以直接在Issues中，进行提交。感谢！！！





