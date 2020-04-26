#### Quick start  
* 해당 디렉토리 아래에서 "docker-compse" 파일을 찾을 때 사용할 수 있는 명령어.  
```
$ find . -name "*docker-compose*"
```
```
$ find . | grep "docker-compose"
```

## find  

* 파일 및 디렉토리를 검색할 때 사용.  

### 1. $ find  

```
$find 
```
* 아무런 옵션이 없다면 현재 디렉토리 및 **하위 디렉토리**에 있는 모든 **파일** 및 **디렉토리**를 출력.  

### 2. find [path]  
* 대상 디렉토리 및 하위 디렉토리의 모든 파일 및 디렉토리 출력.  
```
$find test
```

```
test
test/hello.cpp
test/hello
```

### 3. find [path] -name [name]  
* 해당 path 아래에서 name과 **정확히 일치하는** 파일 및 디렉토리를 출력  

```
$ find . -name "hello.c"
```

### 4. find [path] -name "*ll*"  
* wild card를 사용하여 해당 문자가 포함된 파일 및 디렉토리를 전부 출력  

```
$ find . -name "*ll*"
```
```
test/hello.c
```

### 5. find [path] -name "*.c"
* 해당 확장자를 가진 모든 파일 탐색 및 출력  
```
$ find . -name "*.c"
```

### 6. find [path] -maxdepth 1  

* 재귀적으로 탐색할 하위 디렉토리의 깊이 지정  

```
find . -maxdepth 1
```
현재 디렉토리의 파일 및 디렉토리만 출력.  





