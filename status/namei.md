

# namei  

* **루트 디렉토리**부터 **명시된 디렉토리, 파일**까지의 권한 등 정보를 한번에 볼 수 있다.  


## 옵션  

**-o** : 소유자, 소유 그룹 정보 함께 출력  
**-m** : 권한까지 함께 출력  


## 예제  
```
namei ~/Desktop/mysource/hello.html 
f: /home/horoyoii/Desktop/mysource/hello.html

d /
 d home
 d horoyoii
 d Desktop
 d mysource
 - hello.html
```

* 권한 - 소유자 함께 출력  
```
namei -om ~/Desktop/mysource/hello.html

f: /home/horoyoii/Desktop/mysource/hello.html
 drwxr-xr-x root     root     /
 drwxr-xr-x root     root     home
 drwxr-xr-x horoyoii horoyoii horoyoii
 drwxr-xr-x horoyoii horoyoii Desktop
 drwxr-xr-x horoyoii horoyoii mysource
 -rw-r--r-- horoyoii horoyoii hello.html
```
