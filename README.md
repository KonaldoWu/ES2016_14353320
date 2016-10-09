# 我的DOL配置过程

           --by吴云柯（14353320） using markdown


## 安装一些必要的环境

* sudo apt-get update
![](http://oepww4mce.bkt.clouddn.com/16-10-8/1040597.jpg)
  
* sudo apt-get install ant
![](http://oepww4mce.bkt.clouddn.com/16-10-8/73559168.jpg)
* sudo apt-get install openjdk-7-jdk
![](http://oepww4mce.bkt.clouddn.com/16-10-8/78103112.jpg)




*sudo apt-get install unzip





*![](http://oepww4mce.bkt.clouddn.com/16-10-8/4180726.jpg)


## 下载文件
* sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz
![](http://oepww4mce.bkt.clouddn.com/16-10-8/19660421.jpg)

* sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip
![](http://oepww4mce.bkt.clouddn.com/16-10-8/43284135.jpg)

## 解压文件
* 新建dol的文件夹  // mkdir dol

* 将dolethz.zip解压到 dol文件夹中  //unzip dol_ethz.zip -d dol
![](http://oepww4mce.bkt.clouddn.com/16-10-8/7641868.jpg)
* 解压systemc //tar -zxvf systemc-2.3.1.tgz
![](http://oepww4mce.bkt.clouddn.com/16-10-8/42166868.jpg)

## 编译systemc


* 运行configure
![](http://oepww4mce.bkt.clouddn.com/16-10-8/23357862.jpg)




* 编译





![](http://oepww4mce.bkt.clouddn.com/16-10-8/97223499.jpg)
* 记录当前的工作路径
![](http://oepww4mce.bkt.clouddn.com/16-10-8/80678148.jpg)
![](http://oepww4mce.bkt.clouddn.com/16-10-8/36951402.jpg)
## 编译dol
* 修改build_zip.xml文件
* ![](http://oepww4mce.bkt.clouddn.com/16-10-8/577667.jpg)

* 编译
 ![](http://oepww4mce.bkt.clouddn.com/16-10-8/9927077.jpg)
 
 
 
* run example1



 ![](http://oepww4mce.bkt.clouddn.com/16-10-8/40153012.jpg)
