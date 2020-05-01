

* docker의 경우 환경변수를 commandline에 넘겨줌으로써 사용자의 인풋에 따라 작업을 처리할 수 있다.  


#### 1. 환경변수를 등록  

```
$ export apple=good
```

#### 2. shell script에서 사용  
* 아래와 같이 $을 통해 환경변수 그대로 사용 가능  
```
#! /bin/zsh

echo $apple
```

#### 2. c언어에서 환경변수 읽어오기  
* **getenv**
```c
#include<stdio.h>
#include<stdlib.h>

int main(void){
    printf("Helll\n");
    
    printf("apple is : %s\n", getenv("APPLE"));
    printf("pwd is : %s\n", getenv("PWD"));
    return 0;
}
```
