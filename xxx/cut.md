

# cut  
파일의 내용을 **필드** 혹은 **바이트**, **문자**단위로 추출  

## 옵션  

1. **-c** : 문자 기준 추출할 오프셋 지정  

```
ls -al             
합계 24
drwxr-xr-x  6 horoyoii horoyoii 4096  5월  1 19:07 .
drwxr-xr-x 79 horoyoii horoyoii 4096  5월  1 17:17 ..
drwxr-xr-x  2 horoyoii horoyoii 4096  5월  2 15:42 config-server
drwxr-xr-x  2 horoyoii horoyoii 4096  5월  1 19:07 router
drwxr-xr-x  2 horoyoii horoyoii 4096  5월  1 19:20 shard-1
drwxr-xr-x  2 horoyoii horoyoii 4096  5월  1 19:12 shard-2
```
* 첫번째 문자 출력  
```
ls -al | cut -c 1
�
d
d
d
d
d
d
```

* 1~4번째의 문자 출력  
```
ls -al | cut -c 1-4
합�
drwx
drwx
drwx
drwx
drwx
drwx
```
