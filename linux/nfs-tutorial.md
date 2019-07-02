## 服务搭建
linux如何使用NFS挂载文件系统:[参考](https://www.cnblogs.com/arcer/p/3738522.html)

* apt-get install nfs-kernel-server
* vim /etc/exports 
* /home/xuhao *(rw,sync,no_root_squash,no_subtree_check)
* exportfs -a

## 挂载卸载
	挂载
	mkdir /mnt/nfs
	mount -t nfs 10.193.0.2:/mnt/sdc3-data-500G /mnt/nfs
	卸载
	umount /mnt/nfs