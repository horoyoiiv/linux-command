  
  
# vmstat   

[Ref](https://www.linode.com/docs/uptime/monitoring/use-vmstat-to-monitor-system-performance/)  


### 시스템의 상태를 알 수 있다.  
```
$ vmstat

procs -----------memory---------- ---swap-- -----io---- -system-- ------cpu-----
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st
 2  0 798312 416396  32132 734260   37  241   149   342  101  257 24  8 68  0  0
```


### procs  

1. **r** : CPU의 사용을 기다리며 대기하고 있는 task의 수  
2. **b** : **sleep**상태의 프로세스의 수 
**uninterruptible sleep**의 상태 :  


```
procs -----------memory---------- ---swap-- -----io---- -system-- ------cpu-----
 r  b   swpd   free   buff  cache   si   so    bi    bo   in   cs us sy id wa st
 
 1  0 822584 412140  17812 960488    0    0     0     0  801 1254 13  1 86  0  0
 1  0 822584 412276  17812 959624    0    0     0     0  975 1823 13  1 86  0  0

>>mongo-db 실행

 8  0 822584 353612  18624 994960  124    0  4056 28340 3751 10111 25  6 67  2  0
 2  0 830072 161780  18280 996252  232 8256 63981  9328 11635 33083 30 12 55  2  0
 4  0 852700 234132  18028 933532 4556 45924 16460 48036 16705 36297 22  7 67  3  0
```



