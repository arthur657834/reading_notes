进程调度
内存管理
文件系统
网络接口
进程通信



环境初始化
1./etc/profile
2.读取.bash_profile,~/.bash_login,~/.profile第一个存在的文件
3.如果存在~/.bash_profile存在,还会执行~/.bashrc

文件系统故障处理机制
1.事务提交失效机制
2.无重写失效机制
3.日志写失效机制
4.磁盘写失效机制





npm install express@3.* 来安装3.x的最新版本
phantomjs@1.9.8

PV:physccal volume 
vg:volume group
lv:logical volume
pe:physccal extent
le:logical extent
vgda:volume group descriptor area

dstat
iostat
iptraf
mpstat
netstat
netperf
sar
tcptrace
vmstat

badblocks

quotaon
quotaoff
edquota

登录密码设置
/etc/pam.d/system-auth
登录次数设置
/etc/pam.d/login

ssh限制:
/etc/hosts.allow

ssh 登录超时设置
HISTFILESIZE=1000

系统审计
/etc/audit/auditd.conf

auditcrl
aureport
ausearch

logrotate


虚拟监视器结构类型：
宿主模型:os-hosted vmms   (vmware)
超级管理程序模型:hypervisor (esx)
混合:hybrid vmms

#查看filename这个文件是32位或者64位。
file /root/nwjs-v0.19.5-linux-x64/lib/libcups.so.2 

#ldd filename 查看可执行文件filename需要哪些依赖文件。
ldd /root/nwjs-v0.19.5-linux-x64/lib/libcups.so.2 
