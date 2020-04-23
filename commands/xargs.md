

## xargs  

 * 한 프로세스의 출력값을 다른 프로세스의 인자값으로 넘길 때 사용  
 
```
docker ps -aq | xargs docker rm 
```
