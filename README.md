# NeShellVariable Shell之变量的定义及使用

## 一、概念
### 1.1 shell命令
shell可执行文件必须以`#!/bin/bash`开头
```bash
# 该方式不需要权限
/bin/bash demo.sh
# 该方式需要权限
chmod 777 demo.sh
./demo.sh 
```
实操：  
![image](https://github.com/tianyalu/NeShellVariable/blob/master/show/bin_bash.png)
### 1.2 变量
#### 1.2.1 局部变量
注意：变量定义“=”两边不能有空格
```bash
# 局部变量
A=10
echo $A
```
实操：  
![image](https://github.com/tianyalu/NeShellVariable/blob/master/show/local_variable.png)  
#### 1.2.2 系统环境变量

形式 | 说明
--   | --
$0   | 当前程序的名称
$n   | 程序的输入参数 n=1 第一个参数 n2:第二个参数 1..n
$*   | 所有的输入参数
$#   | 输入参数的个数
$?   | 命令执行的状态，一般返回0，代表成功

```bash
# 系统环境变量
echo $PWD  # 当前路径
echo $0 # 当前程序名称
echo $1 # 第一个参数
echo $2 # 第二个参数
echo "this \$? is $?" # 命令执行的状态：成功0 或者失败
echo "this \*? is $*" # 所有的输入参数
echo "this \#? is $#" # 输入参数的个数
```
实操：  
![image](https://github.com/tianyalu/NeShellVariable/blob/master/show/system_variable.png)  


