
# brctl  

* 리눅스에서 브릿지 정보를 확인할 수 있다.  

```
$ brctl show  

bridge name	        bridge id		        STP enabled	    interfaces

br-01725bfbcd71		8000.0242502fe9ab	      no		  
br-08c05a0146fe		8000.0242e4e28b83	      no		
br-143223d9285d		8000.02420d5206af	      no		
br-3ee0860c9973		8000.0242c134f63d	      no		
br-92d325b10472		8000.024254486fcb	      no		
br-b3f94a7f5c73		8000.024254a58ac6	      no		
docker0		        8000.0242577ecbc4	      no		        veth013d567
							                                          veth76c2fb6
```

## 브릿지  

* 브릿지란 **L2**에서 동작하며 **Mac Address**를 기반으로 데이터를 전송한다.  
* 브릿지 장비는 컴퓨터의 **Mac address 와 (물리적) 포트**를 연결하여 매핑 테이블을 구성한 후 포워딩을 수행한다.

![스크린샷, 2020-05-04 17-21-24](https://user-images.githubusercontent.com/62331555/80947731-b931ad80-8e2b-11ea-82f2-cec9aa3522d8.png)  

![스크린샷, 2020-05-04 17-21-05](https://user-images.githubusercontent.com/62331555/80947742-bafb7100-8e2b-11ea-8592-0afe6744f136.png)  

* Mac address는 **NIC**에 할당되는 고유한 값이며, 제조사에 의해 부여된다.  
* NIC도 하나의 장비이기에 하나의 파일로 취급되며, 이때 **eth0**와 같이 표현된다.  
* 리눅스는 자신에게 장착된 디바이스(NIC)를 /dev/eth0라는 파일로 관리한다.  








