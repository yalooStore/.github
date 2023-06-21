# 🛍️MSA 쇼핑몰 프로젝트

- <a href="https://github.com/yalooStore/yalooStore-shop">API Serve</a>
- <a href="https://github.com/yalooStore/yalooStore-front">Front Serve</a>
- <a href="https://github.com/yalooStore/yalooStore-auth">Auth Serve</a>
- <a href="https://github.com/yalooStore/yalooStore-batch">Batch Serve</a>
- <a href="https://github.com/yalooStore/yalooStore-gateway">Gateway Serve</a>

# 1.Project architecture
![image](https://github.com/yalooStore/.github/assets/81970382/a469c261-2ff1-4221-b220-2de4618ddf4a)

# 2.ERD
![image](https://github.com/yalooStore/.github/assets/81970382/bd76977e-8b3c-4a5a-bf16-ac39626efe87)

# 3.프로젝트 서버별 상세설명
## Shop - API Server
- 클라이언트 요청을 처리하는 api 관련 서버 입니다.
### 회원
- 회원가입
- 회원 수정
- 회원 삭제(기록은 남게)
- 회원 멤버쉽

### 상품
- 상품 추가
- 상품 검색
- 전체 상품 검색(모든 회원용)
- 상세 상품 검색
- 상품 삭제

### 주문


## Front - Client Server
- 클라이언트가 요청을 보낼 수 있는 서버로 이곳에서 front를 담당합니다.


## Api gateway
- 들어온 요청을 api gateway를 통해 처리할 수 있도록 하여 보안성을 올립니다.

## Auth Server
- front 서버에서 들어온 인증, 인가 관련 처리를 이곳 서버에서 처리합니다.

### 회원 인증
- Spring security와 jwt + Redis를 사용한 회원 인증 작업 시행
### 회원 인가


## Batch Server 
- 회원 생일 기점으로 +n일 후 생일 쿠폰 지급 

# Skill tech 
<img src="https://img.shields.io/badge/{내용}-{배경 색깔}?style={스타일}&logo={로고이름}&logoColor={로고 색깔}"/>
<div>
<img src="https://img.shields.io/badge/spring-6DB33F?style=flat&logo=Spring&logoColor=white"/> 
<img src="https://img.shields.io/badge/springBoot-6DB33F?style=flat&logo=Spring boot&logoColor=white"/>
<img src="https://img.shields.io/badge/spring Security-6DB33F?style=flat&logo=Spring Security&logoColor=white"/>
</div>

