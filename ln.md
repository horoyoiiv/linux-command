

# ln  

**링크**란 윈도우의 바로가기와 유사하다.  

## Inode  

링크 전에 Inode를 이해해야 한다.  
[Inode 란?](https://blog.naver.com/bbaroo27/100183681724)  

linux에서 파일과 디렉토리마다 하나씩 생성된다.  

#### 1. 파일 시스템이 파일을 관리하기 위한 자료구조  
Inode는 **파일 시스템**이 파일을 관리하기 위하여 사용하는 자료구조다.  
파일 시스템 : 윈도우의 FAT, 리눅스의 ext2 ext4  

Inode에는 파일의 소유권자, 물리적인 파일의 디스크 위치, 링크의 수 등등이 저장  

#### 2. ls -i 옵션  

```
ls -i 
```
  
-i 옵션을 통해 inode number를 확인할 수 있다.  
```
2111359 -rw-rw-r-- 1 horoyoii horoyoii 24  4월 20 02:21 hello_1.txt
2097172 -rwx------ 1 horoyoii horoyoii 10  4월 20 02:17 hello_2.txt
2111357 lrwxrwxrwx 1 horoyoii horoyoii 11  4월 20 02:19 hello_s.txt -> hello_1.txt
```



## link  
[link for LINK](https://jybaek.tistory.com/578)  


#### 1. hard link  

```
ln [소스파일] [생성할 파일 명]
```
hard link로 파일 생성 시 **동일한 inode**을 가르킨다.  

inode의 number가 동일하다.  
inode field가 3이다.  
```
2111357 -rw-rw-r-- 3 horoyoii horoyoii 10  4월 20 02:30 hello.txt
2111357 -rw-rw-r-- 3 horoyoii horoyoii 10  4월 20 02:30 hello_2.txt
2111357 -rw-rw-r-- 3 horoyoii horoyoii 10  4월 20 02:30 hello_3.txt
```


#### 2. symbolic link  

symbolic link는 inode가 아닌, **파일 이름 그 자체**를 가르킨다.  
그렇기에 새로운 inode가 생성된다.  

```
ln -s [소스파일, 디렉토리]  [생성할 파일, 디렉토리 명 ]
```

```
2111357 -rw-rw-r-- 3 horoyoii horoyoii 10  4월 20 02:30 hello.txt
2111357 -rw-rw-r-- 3 horoyoii horoyoii 10  4월 20 02:30 hello_2.txt
2111357 -rw-rw-r-- 3 horoyoii horoyoii 10  4월 20 02:30 hello_3.txt
2097172 lrwxrwxrwx 1 horoyoii horoyoii  9  4월 20 02:37 s_hello.txt -> hello.txt
```

타입은 l 이다.  
<s_hello.txt -> hello.txt> 이 파일은 hello.txt 파일 명을 가진 파일을 가르킨다는 의미다.   
그렇기에 hello.txt 파일을 삭제하면 해당 파일의 이름을 가진 파일이 없기 때문에 오류  
하지만 동일한 파일의 이름을 가진 파일을 다시 생성하면 이번ㅇ네 그것을 가르키게 되는 것이다..!  











