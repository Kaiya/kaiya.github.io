Go程序启动过程
大致的调用流程是
rt0_amd64_linux -> rt0_go -> runtime.newproc -> runtime.main -> main.main
rt0_go中调用runtime.newproc时将runtime.main的地址作为参数传给runtime.newproc

从newproc的注释得知，编译器会将用户的go func(){}语句编译成对newproc的调用（即生成类似rt0_go中调用newproc类似的汇编代码）