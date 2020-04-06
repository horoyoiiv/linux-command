

# seq  

 * 리눅스에서 반복문 돌릴 때 사용  
 
 
#### seq 10  
* 1 부터 10 까지 출력

#### seq 2 23
* 2부터 23까지 출력  

#### seq 1 2 10  
* 1부터 10까지 2씩 증가하면 출력  

#### seq 10 -2 1  
* 10부터 1까지 2씩 감소하며 출력  


## Example  



```
for i in `seq 10`
do
   echo "$i"
done
```

```
1
2
3
4
5
6
7
8
9
10
```








[Ref](https://www.snoopybox.co.kr/1680)  
