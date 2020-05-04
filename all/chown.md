

# chown  

* 파일 혹은 디렉토리의 **소유자 : 그룹**을 바꿀 때 사용  


### $ chown 바꿀 소유자:바꿀 그룹 [대상]  

```
ls -al                              
-rw-r--r--  1 horoyoiiv horoyoiiv   32  4월  6 23:39 README.md
```

```
sudo chown horoyoii:horoyoii README.md
-rw-r--r--  1 horoyoii horoyoii   32  4월  6 23:39 README.md
```
