

# kill  

```
kill [-SIGNAL유형] [PID]  
```

* 해당 프로세스에 **시그널**을 발생시키는 커맨드  

#### 1. signal  

* 시그널이란 커널에 의해 발행되며, 프로세스에 전달된다.  
* 특정 이벤트가 발생했다는 시그널을 비동기적으로 프로세스에 notificiation해주는 것.  
* 인터럽트와의 차이점은 인터럽트는 이것의 처리를 커널이 하지만, 시그널은 프로세스가 직접 처리한다.  


#### 2. 시그널을 받은 프로세스  

* 프로세스가 시그널을 받게 되면, normal flow of execution을 중지하고 사용자에 의해 정의된 signal handler나 default handler를 실행한다.  


#### 3. kill -l
* 시그널 리스트를 확인할 수 있는 옵션  
![스크린샷, 2020-04-24 19-09-13](https://user-images.githubusercontent.com/62331555/80201462-217bd480-865f-11ea-9beb-eb670ed2a5c2.png)  

#### 4. kill -2 10204  

* pid 10204 프로세스에 SIGINT(Interrupt) 시그널을 발생시키는 커맨드  

#### 5. man 7 kill  

* 각 시그널에 대한 상세 설명  






 





