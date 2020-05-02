# linux-command
linux command 를 모아보자!

```
history | awk '{a[$2]++}END{for(i in a){print a[i] " " i}}' | sort -nr | head -10
```


## Basics  
[1. env, export](/basics.md) : 환경변수  
[2. man hier](/basic/dir.md) : **리눅스의 파일 시스템 구조**(정리 중)      
[3. printenv, set](/basic/printenv.md) : 환경변수, 쉘 변수   
[4. char* getenv(char*)](/basic/read.md) : shell scirpt 혹은 c 코드에서 환경변수 읽기  


## Simple as possible  

[1. xargs](/commands/xargs.md) : std input이 아닌, command-line parameter로 넘겨줄려면?   
[2. less](/showing/less.md) : 한 화면에 다 담기지 않고, 마우스 스크롤까지 먹통이라면...  
[3. sort](showing/sort.md) : 파일을 행 단위로 정렬할 때. (기준은 열)  
4. head -n : 상위 n행만을 출력   
5. tail -n : 하위 n행만을 출력  

## XXX  
[1.awk](/xxx/awk) : 행 단위 처리  
[2.cut](/xxx/cut.md) : 파일의 내용을 **cut**하여 출력  

## 탐색  
[1. find](/search/find.md) : 파일 및 디렉토리 이름을 탐색한다.  

## 상태  

[1. top](/status/top.md) : 각 프로세스의 CPU점유율에 대한 실시간 모니터링.  
[2. ulimit](/status/ulimit.md) : 각 프로세스에 대한 제약사항(열 수 있는 파일의 수)  

## 프로세스  
[1.kill](/process/kill.md) : 해당 프로세스에 시그널을 보내고자 한다면?  



## 권한  
[1. chmod](/권한.md)  

## 파일 및 디렉토리 관련  
[1.ln](/ln.md)  


## 네트워크  

1. fuser -k 3000/tcp : 해당 포트를 가진 프로세스 종료  

## ETC  
[1. wget](/etc/wget.md) : web get? 네트워크를 통해 데이터를 로컬에 다운로드 받자...!  
2. history : 내가 무슨 커맨드를 쳤더라?  


