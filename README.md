# teamate

# hyperledger fabric sample 

## pre-condition

* curl, docker, docker-compose, go, nodejs, python 
* hyperledger fabric-docker images are installed
* GOPATH are configured
* hyperledger bineries are installed (cryptogen, configtxgen ... etcs)

# -network

## 1. generating crypto-config directory, genesis.block, channel and anchor peer transactions

cd network

./generate.sh

## 2. starting the network, create channel and join 

./start.sh

# -chaincode

## 3. chaincode install, instsantiate and test(invoke, query, invoke)

./cc_tea.sh instantiate v1.0

# -prototype

cd ../prototype

## 4. nodejs module install

npm install

## 5. certification works

node enrollAdmin.js

node registerUser.js

## 6. server start

node server.js

## 7. open web browser and connect to localhost:8080

## 8. prototype 사이트 구조

![sitemap](https://user-images.githubusercontent.com/65117718/89747293-21fa8700-daf9-11ea-986e-08b9b27c8e1b.png)

## -web_template

#### 1.teamate/network 이동

```shell
cd temate/network
```

#### 2. ./teardown.sh 실행을 통해 container 제거

```shell
./teardown.sh
```



#### 3. 네트워크 실행

```shell
./start.sh
```

#### 4. chaincode 인스톨

```shell
./cc_tea.sh instantiate v1.0
```

#### 5. web_template로 이동 후 npm 을 이용한 라이브러리 설치

```shell
cd ..&& cd web_template && npm install
```

#### 6. enrollAdmin.js를 통한 adminID등록

##### 	web_template 폴더 안에 wallet폴더가 존재하면 삭제 후 실행

```shell
node enrollAdimin.js
```

#### 7. registerUser.js를 통한 user등록

```shell
node registerUser.js
```

#### 8. Server실행

```shell
node server.js
```

#### 9.
![tt](https://user-images.githubusercontent.com/65117718/89754255-2a14ef80-db16-11ea-9bb4-fc623f9f69c3.png)

