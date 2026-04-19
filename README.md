<img width="1908" height="868" alt="Pasted image 20260419151005" src="https://github.com/user-attachments/assets/5f9bf2cc-3e00-4562-8805-0764dae5ddfb" /># SSH-PyCharm-SEU-
SSH如何将PyCharm与SEU大数据中心进行连接
# 目的
将PyCharm上编写好的代码直接学校的卡上
# 文档基础
本文档的基础完全基于东南大学大数据计算中心用户手册的第三章智算平台GPU使用
<img width="1908" height="868" alt="Pasted image 20260419151005" src="https://github.com/user-attachments/assets/546fa231-f79f-4d0a-8d49-8b88ee63ce41" />
# 步骤
## 创建镜像
1. 在学校的公共镜像中选择带有ssh功能的镜像
<img width="1890" height="851" alt="Pasted image 20260419151247" src="https://github.com/user-attachments/assets/37b24827-bf84-43f0-9561-58c648da8fea" />
## 模型开发
1. 在模型开发页面中可以看到通过镜像已经成功创建的实例
<img width="1597" height="715" alt="Pasted image 20260419151537" src="https://github.com/user-attachments/assets/65d5c893-1fab-4e28-bd16-2cc1fc05d80b" />
2. 点击启动容器，并通过ssh隧道启动
<img width="1883" height="817" alt="Pasted image 20260419151614" src="https://github.com/user-attachments/assets/a9c1059e-e317-43eb-b7d3-3a7e4a05b357" />

3. 选择你想同步文件的目录
4. 点击查询之后，同步实例的状态（等待分配资源->运行）
5. 点击连接方式，得到右边的东西
<img width="1905" height="849" alt="Pasted image 20260419151736" src="https://github.com/user-attachments/assets/c62f8520-e500-42c2-9023-e06151b00837" />

## PyCharm端连接
1. 只有professional版本可以使用ssh，学生可以在官网免费申请，具体方式可在网上搜索，一大堆教程
2. 使用pycharm打开你的项目文件夹
3. 添加新的解释器
<img width="1902" height="1005" alt="Pasted image 20260419152153" src="https://github.com/user-attachments/assets/44e8cbc2-6d1a-4971-8052-3f9fc1573463" />

4. 选择基于ssh
5. 这里的填写信息完全是基于模型开发中最后一步的右边的信息：主机为xxxx@10.128.202.100；端口为22222,；用户名为个人学号
6. 之后连接成功一直点击下一步
7. 第四步进行项目的配置，选择最基本的就可以
8. 创建即可
# 如何自定义选择学校卡用来同步文件的文件夹
1. 一开始同步的时候，总是会同步到一个tmpt文件夹之后，这样会导致运行的时候选择文件夹的时候存在问题，有点麻烦
2. 点击工具、部署 、配置、映射，将部署路径填为 "/ "即可（前提是根路径要设置好路径）<img width="1900" height="990" alt="Pasted image 20260419152927" src="https://github.com/user-attachments/assets/d4ae0abd-4b9b-40eb-8bd9-160c09adeecd" />
<img width="962" height="832" alt="Pasted image 20260419153117" src="https://github.com/user-attachments/assets/91d623dc-327d-408c-b44d-99fd47cd8ddb" />
<img width="985" height="337" alt="Pasted image 20260419153127" src="https://github.com/user-attachments/assets/f6ef2f4c-1acc-48ce-b6a5-b848428e87b3" />

