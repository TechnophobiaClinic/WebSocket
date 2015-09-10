# Beacon WebSocket Server

아래와 같은 유형으로 값이 모든 Listener들에게 보내진다.
```sh
B9116851-4A76-46E8-A3A8-xxxxxxxxxxxx:proximity-near
```

아래와 같이 구분하면 된다.
  - 1. 첫번째 부분은 비컨을 읽어 들이는 디바이스 기기를 uuid를 기준으로 ":" 구분한다.
  - 2. 두번째 부분은 비컨의 상태를 proximity, region 으로 나뉘어 "-"로 구분한다.
  - 3. 세번째 부분은 비컨의 상태에 따른 값이 표시된다.
```sh
[1.uuid]:[2.type]-[3.value]
```

### type의 종류
    - proximity
    - region
    
### value의 종류
    - proximity : immediate, near, far, noBeacons
    - region : enter, exit
