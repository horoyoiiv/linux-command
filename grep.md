

## grep  

```
grep [option] [pattern] [location]  
```

  * 파일에서 등장하는 특정 pattern 찾아주는 command  
  
## Examples  

```
grep "main" Application.java
```
해당 파일에서 main이 포함된 라인을 출력  
  

#### -n : 라인 번호  
```
grep -n "main" Application.java
```
라인의 번호와 함께 출력
  
#### * : 모든 파일    
```
grep "main" * 
```
현재 디렉토리에서 모든 파일을 대상으로 문자열 탐색  

#### -r : 하위 디렉토리까지  
```
grep -r "main" *
```
현재 디렉토리 뿐만 아니라 서브 디렉토리까지 **재귀적으로** 탐색  




