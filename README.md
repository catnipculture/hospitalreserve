> #### 作者主页：[舒克日记](https://blog.csdn.net/cativen)
>
>  简介：Java领域优质创作者、Java项目、学习资料、技术互助
>
> <b><font color=red>文中获取源码</font></b>

# 项目介绍

一共有管理员、挂号人员、划价人员、医生 四个角色

管理员登录进入本系统操作的功能包括对挂号人员，划价人员，患者，门诊信息，体检信息，药品信息等进行管理。

挂号人员登录进入本系统操作的功能包括新增挂号信息，新增患者信息，管理挂号和患者信息，查看门诊信息，病例信息，以及药品信息等。



划价人员登录进入本系统操作的功能包括为已划价的病例进行取药，查看体检信息，药品信息，医生信息，门诊信息等。

医生登录进入本系统操作的功能包括添加病例信息，管理病例信息，查看挂号信息，患者信息，体检信息，门诊信息等。





# 环境要求



1.运行环境：最好是java jdk1.8,我们在这个平台上运行的。其他版本理论上也可以。 

2.IDE环境：IDEA,Eclipse,Myeclipse都可以。推荐IDEA; 

3.tomcat环境：Tomcat7.x,8.X,9.x版本均可 

4.硬件环境：windows7/8/10 4G内存以上；或者Mac OS; 

5.是否Maven项目：是；查看源码目录中是否包含pom.xml;若包含，则为maven项目，否则为非maven.项目 

6.数据库：MySql5.7/8.0等版本均可；





# 技术栈



运行环境：jdk8 + tomcat9 + mysql5.7 + windows10

服务端技术：SpringBoot + MyBatis + Vue + Bootstrap + jQuery





# 使用说明





1.使用Navicat或者其它工具，在mysql中创建对应sq文件名称的数据库，并导入项目的sql文件； 

2.使用IDEA/Eclipse/MyEclipse导入项目，修改配置，运行项目； 

3.将项目中config-propertiesi配置文件中的数据库配置改为自己的配置，然后运行；





# 运行指导

idea导入源码空间站顶目教程说明(Vindows版)-ssm篇：

http://mtw.so/5MHvZq 

源码地址：[http://www.codegym.top](http://www.codegym.top/)





# 运行截图



![springboot203医疗挂号管理系统0](https://img-blog.csdnimg.cn/img_convert/316fd3b2d1db5008e9b59f136be9e17e.png)

![springboot203医疗挂号管理系统1](https://img-blog.csdnimg.cn/img_convert/f736ec97e87f54873727881a5c6950f8.png)

![springboot203医疗挂号管理系统2](https://img-blog.csdnimg.cn/img_convert/94424672b13816dfa9c6e965ad1d7e84.png)

![springboot203医疗挂号管理系统3](https://img-blog.csdnimg.cn/img_convert/995889c404b92e17401516aeb6f7138c.png)

![springboot203医疗挂号管理系统4](https://img-blog.csdnimg.cn/img_convert/02c8e7107f6d8aeb55ee0b42abb0a2ec.png)

![springboot203医疗挂号管理系统5](https://img-blog.csdnimg.cn/img_convert/fa7338eba69f30747fc9a1de69c701c7.png)

![springboot203医疗挂号管理系统6](https://img-blog.csdnimg.cn/img_convert/4c8f18bc62ef27b646df5cc76c0d41c3.png)

![springboot203医疗挂号管理系统7](https://img-blog.csdnimg.cn/img_convert/54a1694a0c3f42f306532b2ce71c218e.png)

![springboot203医疗挂号管理系统8](https://img-blog.csdnimg.cn/img_convert/790fc4a14ba2118bd854c2e4633782cd.png)

![springboot203医疗挂号管理系统9](https://img-blog.csdnimg.cn/img_convert/ed319eb3156b9924a46c3726fd7ddaf6.png)

![springboot203医疗挂号管理系统10](https://img-blog.csdnimg.cn/img_convert/bb43444aa2f312784d5a723efb2ed3e3.png)

![springboot203医疗挂号管理系统11](https://img-blog.csdnimg.cn/img_convert/48a61fab654c5d167347cb386fc640c5.png)

![springboot203医疗挂号管理系统12](https://img-blog.csdnimg.cn/img_convert/3a3352468c382a783b48071d5c901448.png)

![springboot203医疗挂号管理系统13](https://img-blog.csdnimg.cn/img_convert/5a070e1cb1d2a1818935c9e83e9bbfe1.png)

![springboot203医疗挂号管理系统14](https://img-blog.csdnimg.cn/img_convert/15a4ff058060963ef3758a0f530ed80e.png)

![springboot203医疗挂号管理系统15](https://img-blog.csdnimg.cn/img_convert/8f7f36cecb755905b4f43fa4cdb266c5.png)

![springboot203医疗挂号管理系统16](https://img-blog.csdnimg.cn/img_convert/8c57b32645b79b8e9cdf818489accd9d.png)

![springboot203医疗挂号管理系统17](https://img-blog.csdnimg.cn/img_convert/d054d6925da6f1a299539b332902e870.png)

![springboot203医疗挂号管理系统18](https://img-blog.csdnimg.cn/img_convert/b75d848f2e9f9f4a88c069b62b6c361c.png)



![springboot203医疗挂号管理系统20](https://img-blog.csdnimg.cn/img_convert/f5f9ec960c53f6d2080dec9cb29b50c5.png)

### 代码

```java
    @Override
	public List<HuiyuanVO> selectListVO(Wrapper<HuiyuanEntity> wrapper) {
 		return baseMapper.selectListVO(wrapper);
	}
	
	@Override
	public HuiyuanVO selectVO(Wrapper<HuiyuanEntity> wrapper) {
 		return baseMapper.selectVO(wrapper);
	}
	
	@Override
	public List<HuiyuanView> selectListView(Wrapper<HuiyuanEntity> wrapper) {
		return baseMapper.selectListView(wrapper);
	}

	@Override
	public HuiyuanView selectView(Wrapper<HuiyuanEntity> wrapper) {
		return baseMapper.selectView(wrapper);
	}
```
