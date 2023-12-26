# Man's Man's Travel

🔔 본 프로젝트는 **삼성 청년 SW 아카데미** 1학기 관통 프로젝트 결과물입니다

## **개요**

- 무모하고 무계획적인 여행을 컨셉으로 국내 관광지 검색 및 추천, 랜덤 여행, 여행 사진 인증 기능을 제공

## 프로젝트 기간

- 2023년 11월 3일 ~ 11월 24일

## 기술 스택

### Front-End

enjoytrip_vuejs_seoul10_team7<br>
├── @ant-design/icons-vue@7.0.1<br>
├── @vitejs/plugin-vue@4.4.1<br>
├── @vueup/vue-quill@1.2.0<br>
├── ant-design-vue@4.0.6<br>
├── axios@1.6.2<br>
├── eslint-plugin-vue@9.18.1<br>
├── eslint@8.53.0<br>
├── exifr@7.1.3<br>
├── jwt-decode@4.0.0<br>
├── pinia-plugin-persistedstate@3.2.0<br>
├── pinia@2.1.7<br>
├── sass@1.69.5<br>
├── vite@4.5.0<br>
├── vue-router@4.2.5<br>
└── vue@3.3.8<br>

### Back-End

enjoytrip_framework_seoul10_team7<br>
├── java(1.8)<br>
├── spring boot(2.7.17)<br>
├── io.spring.dependency-management(1.0.15.RELEASE)<br>
├── org.springframework.boot:spring-boot-starter-web<br>
├── org.mybatis.spring.boot:mybatis-spring-boot-starter:2.3.1<br>
├── org.springframework.boot:spring-boot-starter-validation<br>
├── org.springframework.boot:spring-boot-starter-security<br>
├── io.jsonwebtoken:jjwt-api:0.11.5<br>
│   ├── io.jsonwebtoken:jjwt-impl:0.11.5<br>
│   └── io.jsonwebtoken:jjwt-jackson:0.11.5<br>
├── org.projectlombok:lombok (compileOnly)<br>
├── org.springframework.boot:spring-boot-devtools (developmentOnly)<br>
├── com.h2database:h2 (runtimeOnly)<br>
├── com.mysql:mysql-connector-j (runtimeOnly)<br>
├── org.springframework.boot:spring-boot-starter-test (testImplementation)<br>
├── org.mybatis.spring.boot:mybatis-spring-boot-starter-test:2.3.1 (testImplementation)<br>
├── org.springframework.cloud:spring-cloud-starter-aws:2.2.6.RELEASE<br>
└── com.amazonaws:aws-java-sdk-s3:1.12.593<br>



### DB

└── myBatis(3.5.13)


## 팀원

| 이름   | 구현 기능                                                                                               |
| ------ | ------------------------------------------------------------------------------------------------------- |
| 김은진 | Front-End                                                                     |
|        | 메인 페이지 구현, 여행 페이지 디자인 및 구현, 카카오 API를 이용한 지도 표시, 관광지 검색 및 추천, 마이페이지 구현 |
| 여일구 | Back-End                                                                        |
|        | 로그인 및 회원가입 기능 구현, 관광지 검색 및 랜덤 추천, 관광지 도착 인증 로직, 유저별 레이팅 시스템 디자인 및 구현                             |


## 🔗 API

| 이름              | 메소드 | 설명                   | URI                                                     |
| ----------------- | ------ | ---------------------- | ------------------------------------------------------- |
| 전체 관광지 조회 | GET    | 전체 관광지를 조회 | localhost:8080/attraction?sido={sido}&keyword={keyword} |
| 랭킹 페이지 조회   | GET    | 상위 랭킹 유저를 조회 | localhost:8080/ranking                                 |
| 회원가입           | POST   | 사용자 회원 가입        | localhost:8080/regist                                  |
| 로그인             | POST   | 사용자 로그인          | localhost:8080/login                                   |
| 본인 정보 조회     | GET    | 본인 프로필 조회       | localhost:8080/info                                    |
| 로그아웃           | DELETE | 사용자 로그아웃        | localhost:8080/logout                                  |
| 토큰 재발급       | GET    | JWT 재발급             | localhost:8080/refresh                                 |
| 사용자 정보 조회   | GET    | 사용자 프로필 조회     | localhost:8080/info/{userId}                           |
| 여행 시작         | POST   | 새 여행 시작           | localhost:8080/travel                                  |
| 미해금 지역 조회   | GET    | 미해금된 관광지 조회   | localhost:8080/locked?start={start}&distance={distance} |
| 출발지 조회       | GET    | 출발 가능 관광지 조회 | Localhost:8080/travel/start?sido={sido}&keyword={keyword} |
| 해금 지역 조회     | GET    | 해금된 관광지 조회     | localhost:8080/unlocked?start={start}&distance={distance} |
| 현재 여행 조회     | GET    | 현재 진행 여행 조회   | localhost:8080/profile/travel                          |
| 경유지 반환       | GET    | 인증 가능 경유지 반환 | localhost:8080/profile/travel/{travelId}               |
| 시작지 인증       | POST   | 여행 시작지 인증       | localhost:8080/profile/travel/start                    |
| 경유지 인증       | POST   | 여행 경유지 인증       | localhost:8080/profile/travel/stop                     |
| 도착지 인증       | POST   | 여행 도착지 인증       | localhost:8080/profile/travel/end                      |
| 사진 업로드       | POST   | 프로필 사진 업로드     | localhost:8080/profile/image                           |
| 여행 포기         | PATCH  | 진행 중인 여행 포기    | localhost:8080/profile/surrender                       |



## 🔗 실행 화면

### 🔗 회원가입

![회원가입](https://github.com/Shortudy-10th/tech-for-developer/assets/39663810/1f22fb20-4ce2-4cfc-b4ab-7547d8568de6)

### 🔗 로그인

![로그인](https://github.com/Shortudy-10th/tech-for-developer/assets/39663810/17562152-83a6-42df-bddb-ae61a32cb2b2)

### 🔗 로그아웃

![로그아웃](https://github.com/Shortudy-10th/tech-for-developer/assets/39663810/44b6fbac-1199-45dc-8795-bb10ffdd1866)

### 🔗 마이페이지

![마이페이지1](https://github.com/Shortudy-10th/tech-for-developer/assets/39663810/6e1a87d2-6476-439f-8f19-1a7ccbb38ba7)

![마이페이지2](https://github.com/Shortudy-10th/tech-for-developer/assets/39663810/104f86c6-1902-4f7f-820b-7fd0f9b06a04)

### 🔗 사진 인증

![사진인증1](https://github.com/Shortudy-10th/tech-for-developer/assets/39663810/68786261-d3a9-41cc-979d-d4c5a105f6a1)

![사진인증2](https://github.com/Shortudy-10th/tech-for-developer/assets/39663810/0e17205d-0487-4053-8741-20681ebe4077)

### 🔗 여행계획 생성

![여행계획생성1](https://github.com/Shortudy-10th/tech-for-developer/assets/39663810/f1a269c2-0791-4256-bdb8-993385f4f347)

![여행계획생성2](https://github.com/Shortudy-10th/tech-for-developer/assets/39663810/3166e23a-9c14-4d11-9cf9-df737b25c4fd)

### 🔗 현재 여행 포기

![현재여행 포기1](https://github.com/Shortudy-10th/tech-for-developer/assets/39663810/8a58036b-3f12-41e6-84a7-caf329c241e0)

![현재여행 포기2](https://github.com/Shortudy-10th/tech-for-developer/assets/39663810/9844a64f-6b8f-464a-ab58-d049744e796a)


