
# shutdown command  

  * 해당 시스템을 종료하거나 재시작  
  * **root권한자**만 실행가능  
  
```
shutdown [option] 시간 [경고메시지]
```

## Options  

#### -r  
시스템 재시작

#### -P  
강제종료  

#### -c  
cancel - 예약된 shutdown 명령어 취소  

## Examples  

#### shutdown 5  

5분 후 종료  

#### shutdown -c  
방금 한 shutdown 명령 취소  

#### shutdown -r 5  
5분 후 재부팅 실행  

#### shutdown -r 22:00  
오후 10시에 재부팅 예약  

#### shutdown -r now  
당장 재부팅  












