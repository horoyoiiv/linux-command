
# systemctl  

* linux에서 **systemd**(init process)로 **서비스**를 관리하기 위한 명령어  

#### 1. unit : systemd에서 자신이 관리하는 서비스를 unit이라고 한다.  


## 1. 서비스 유닛 목록확인  
```
systemctl -t service
```

```
UNIT                                                LOAD   ACTIVE SUB     DESCRIPTION                       
apache2.service                                     loaded active running The Apache HTTP Server            
bluetooth.service                                   loaded active running Bluetooth service                 
docker.service                                      loaded active running Docker Application Container Engine
mosquitto.service                                   loaded active running LSB: mosquitto MQTT v3.1 message br
mysql.service                                       loaded active running MySQL Community Server            
redis-server.service                                loaded active running Advanced key-value store          
...
```

## 2. 서비스 유닉 상태 확인  

```
systemctl status [유닛명]
```

* **enabled** : 부팅 시 자동 시작 설정  
* **vendor preset** : vendor가 그렇게 정해놓음.  

```
$ systemctl status apache2

● apache2.service - The Apache HTTP Server
   Loaded: loaded (/lib/systemd/system/apache2.service; enabled; vendor preset: enabled)
  Drop-In: /lib/systemd/system/apache2.service.d
           └─apache2-systemd.conf
   Active: active (running) since Mon 2020-04-27 23:54:01 KST; 4 days ago
  Process: 23966 ExecReload=/usr/sbin/apachectl graceful (code=exited, status=0/SUCCESS)
 Main PID: 1159 (apache2)
    Tasks: 55 (limit: 4518)
   CGroup: /system.slice/apache2.service
           ├─ 1159 /usr/sbin/apache2 -k start
           ├─23978 /usr/sbin/apache2 -k start
           └─23979 /usr/sbin/apache2 -k start

 4월 29 00:09:58 horoyoii-Aspire-E5-576G systemd[1]: Reloaded The Apache HTTP Server.
 4월 30 08:03:36 horoyoii-Aspire-E5-576G systemd[1]: Reloading The Apache HTTP Server.
 4월 30 08:03:36 horoyoii-Aspire-E5-576G apachectl[23763]: AH00558: apache2: Could not reliably determine the
 4월 30 08:03:36 horoyoii-Aspire-E5-576G systemd[1]: Reloaded The Apache HTTP Server.
 5월 01 12:45:56 horoyoii-Aspire-E5-576G systemd[1]: Reloading The Apache HTTP Server.
 5월 01 12:45:56 horoyoii-Aspire-E5-576G apachectl[28677]: AH00558: apache2: Could not reliably determine the
 5월 01 12:45:56 horoyoii-Aspire-E5-576G systemd[1]: Reloaded The Apache HTTP Server.
 5월 02 15:29:21 horoyoii-Aspire-E5-576G systemd[1]: Reloading The Apache HTTP Server.
 5월 02 15:29:21 horoyoii-Aspire-E5-576G apachectl[23966]: AH00558: apache2: Could not reliably determine the
 5월 02 15:29:21 horoyoii-Aspire-E5-576G systemd[1]: Reloaded The Apache HTTP Server.

```

## 3. 서비스 시작 및 종료   
```
systemctl start [유닛 명]
```
```
systemctl stop [유닛 명]
```

## 4. 서비스 재시작 및 리로드  

```
systemctl restart [유닛 명]
```

* **config file**을 다시 읽어들일 때 사용.  
```
systemctl reload [유닛 명]
```

## 5. 부팅 시 시작하기 기능  

```
systemctl enable [유닛명]
```

* 부팅 시 자동으로 실행하지 마라 **disable**  
```
systemctl disable nginx
```






