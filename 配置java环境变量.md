1.检查本地jdk

```
java -version
//查看java位置
which java
结果：/usr/bin/java
```

```
//显示java指令文件属性(可以看到实际java位置)
ls -l /usr/bin/java
//cd 实际java位置
cd /Library/Java/JavaVirtualMachines/versions.jdk/current/Home
//执行./java_home
/Library/Java/JavaVirtualMachines/jdk1.8.0_171.jdk/Contents/Home
```

2.设置java_home

```
vim ~/.bash_profile
//键盘输入i表示编辑
//编辑完后，按esc键退出编辑状态
//输入:wq命令，保存
//命令立即生效
source ~/.bash_profile
```

```
//添加内容
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_171.jdk/Contents/Home
export PATH=$JAVA_HOME/bin:$PATH
```

3.不同终端环境下，设置环境变量区别

```
在bash环境下文件是.bash_profile

在zsh环境下文件是.zshrc
```

