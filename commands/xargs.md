

## xargs  

 * 한 프로세스의 출력값을 다른 프로세스의 인자값으로 넘길 때 사용  
 
```
docker ps -aq | xargs docker rm 
```

#### 1. standard input으로 받은 값을 -> commandline parameter로 넘겨준다.  

```
echo hello | echo
```
* 위의 것은 동작하지 아니한다.  
* echo는 commandline parameter를 받아서 출력한다.  
pipe는 한 프로세스의 출력을 standard input을 넘기기에 동작하지 않음.   

```
echo hello | xargs echo
```
* 파이프를 통해 xargs에 "hello"를 standard input으로 넘겨준다.  
xargs는 이 stdin 값을 뒤의 commmand의 parameter로 생성해준다.  

