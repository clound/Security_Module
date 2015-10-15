## Linux 内核安全模块
    自己编写小的内核模块然后编译进内核,grub 启动后查看新的内核情况,看是否成功.(上传截屏的PDF文件)
    先了解inode_create,inode_permission,task_create在内核中的调用位置.
    关键在security.h的security_operations结构体中定义了相关的钩子函数.
##编译内核
    1. make mrproper
    2. make -O=***(内核路径) menuconfig
    3. make -O=***
    4. sudo make -O=*** modules_install install
    5. sudo update-grub
