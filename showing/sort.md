

# sort  

* 파일의 내용을 정렬하여 출력한다.  


#### 1. sort [file 명]  
* 첫번째 열을 기준으로 오름차순 정렬  
```
$ cat kkk.txt 
abcd 134 abe
deav 123 11a
awe 131 awef
mbnnr 213 awef
wanne 123 awmd
cdme 123 awe
kkem 23 a

$ sort kkk.txt 
abcd 134 abe
awe 131 awef
cdme 123 awe
deav 123 11a
kkem 23 a
mbnnr 213 awef
wanne 123 awmd
```

#### 2. sort -r [file 명]  
* 내름차순 정렬  

#### 3. sort -k 2 [file 명]  
* 두번째 열을 기준으로 오름차순  
* 이때, **숫자를 문자열로 취급해버린다.**  
```
$ sort -k 2 kkk.txt 

deav 123 11a
cdme 123 awe
wanne 123 awmd
awe 131 awef
abcd 134 abe
mbnnr 213 awef
kkem 23 a
```

#### 4. sort -k 2 -n [file 명]  
* 문자열을 숫자로 인식하게
```
sort -k 2 -n kkk.txt

kkem 23 a
cdme 123 awe
deav 123 11a
wanne 123 awmd
awe 131 awef
abcd 134 abe
mbnnr 213 awef
```
