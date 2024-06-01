修改Go程序入口从main.main修改为main.kaiya
runtime/proc.go
注意📢 编译时需要加上--dist-tool参数排除tool的编译才能成功，否则报错runtime.main_main·f: relocation target main.kaiya not defined