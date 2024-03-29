### 2. 그룹 및 계정

#### 2.1. 계정 생성 정책
##### 계정 사용자의 소속 등으로 식별할 수 있는 사용자 계정 생성 규칙을 만든다.

#### 2.2. 그룹 추가
##### 소속 등으로 그룹을 만들고 사용자를 추가한다.
##### 그룹 정보 보기 
```
cat /etc/group
```
##### 그룹 추가하기
```
sudo groupadd -g [GID] [그룹명]
```

#### 2.3. 사용자 추가하기
##### 소속 등으로 그룹을 만들고 사용자를 추가한다.
##### 사용자 추가
```
sudo useradd -g [그룹명/그룹아이디] -k [초기 생성할 파일] -s [쉘 환경] -d [디렉토리] -m [계정명] -c [주석]
```

#### 2.4. 사용자 제거하기
##### 이 작업은 돌이킬 수 없다.
##### -r 옵션을 붙이지 않으면 삭제할 사용자의 디렉토리가 없어지지 않는다.
```
sudo userdel -r [삭제할 사용자]
```

#### 2.5. 사용자별 용량 할당하기
##### 입력
```
sudo edquota [사용자]
```
##### 조회
```
sudo quota -u [사용자]
```
