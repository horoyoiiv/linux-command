[Ref](https://leeeeye321.tistory.com/82)  

# printenv  
* print environment variable  
* 환경변수를 출력헌다.  

```
$ printenv
...
혹은  
```
$ env
```

LANG=ko_KR.UTF-8
PWD=/
...
USER=horoyoii
OLDPWD=/home/horoyoii/Desktop/shell
GOROOT=/usr/local/go
GOPATH=/home/horoyoii/go
```

## 1. 환경변수 세팅  

* **export**를 통해 환경변수를 등록할 수 있다.  
* 이는 자식 프로세스에게 물려준다.  
```
export apple=pie
```
* 또한 아래와 같이 환경변수 출력을 통해 보인다.  
```
$printenv
```

* 하지만 다른 shell을 켜면 그곳에서는 등록되지 않는다.  

## 2. 쉘 변수  
* 해당 **쉘에서만 사용되는 변수**이다.  

* set 명령어는 환경변수와 쉘변수 모두를 출력한다.  
```
$ set 
```

* 환경변수를 등록할 때는  
```
export apple=pie
```
* 쉘변수를 등록할 때는  
```
apple=pie
```


#### 예제  
* 이동경로 지정지 편하게 하려면  

```
$ mycpproom=~/Desktop/cpp // 쉘변수 등록
$ cd mycpproom            // 쉘변수로 cd에 사용
```

#### 자식 쉘  

```
$ test=hello
$ set | grep test
test=hello

$ /bin/zsh            // 자식 쉘로 이동
$ set | grep test
x
$ exit                // 부모 쉘로 돌아감
```






