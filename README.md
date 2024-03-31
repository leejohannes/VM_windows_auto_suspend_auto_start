### VMware Automitic suspend and resume script on Windows
### VMware关机自动挂起和开机自动恢复脚本

实际上无法实现关机的时候真正的执行，因为当执行到这个脚本的嗯时候VMWare的进程已经被Windows结束了。。。

## Win + R, regedit
**\HKEY_USERS\.DEFAULT\Control Panel\Desktop**<br>
**AutoEndTasks=0**

就可以实现关机时候的自动挂起，其实只是VMware被Win关机的自动结束任务给提前结束了


# ~~添加此脚本的方法~~
~~放到任何一个你还能找到的地方。。。当然首先得在你的windows系统中~~
## ~~Win 徽标键 + R~~
~~输入gpedit.msc<br>~~
~~进入到 **Widnows 设置** 然后 **脚本**<br>~~
~~分别手动在启动和关机中添加 **autostart_suspended_vms.bat** / **suspend_all.bat** 这两个脚本<br>~~

---
~~如果你的安装目录不是默认的请自行更改对应的，<br>~~
~~另外启动间隔是60秒，如果你的机器足够快可以设置更短。<br>~~

# ~~How to add script to windows~~
## ~~press win key + r key in~~
~~gpedit.msc<br>~~
~~windows setting script<br>~~
~~add **suspend_all.bat** to shutdown<br>~~
~~**autostart_suspended_vms.bat** to startup<br>~~

For [PVE auto suspend VMs](https://iheld.net/?post=219)
