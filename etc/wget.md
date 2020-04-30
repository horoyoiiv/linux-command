

# wget  

* web get의 약자로, 네트워크를 통해 데이터를 다운로드 받을 수 있다.  
* HTTP, HTTPS, FTP를 지원한다.  
* 

```
wget [option] [url]
```  

#### 1. 기본 사용법  
```
wget https://www.ebi.ac.uk/~zerbino/velvet/velvet_1.2.10.tgz
```

#### 2. 파일명 지정  
* [wget을 실행한 디렉토리]에 [지정된 파일명]으로 저장된다.  
* 웹 브라우저의 [이미지 주소 복사]로 나오는 URL에 대해서 적용한 예제.  
```
wget -O my-image.png https://blogfiles.pstatic.net/MjAyMDA0MjdfMjM2/MDAxNTg3OTQwODEwNDQ0.KJ4QfD9ayS_wQxLQz87yI5QUSpej4joJCWnodHUsVyEg.Pf6agRmhkpGU7Ari_sHqcr85HvymKEJISKLYzNa3aiog.PNG.demonic3540/image.png
```

#### 3. --tries=횟수  
* 통신 장애 등으로 네트워크가 불안정 시, 최대 다운로드 시도 횟수  

```
wget --tries=10 https://www.ebi.ac.uk/~zerbino/velvet/velvet_1.2.10.tgz
```

