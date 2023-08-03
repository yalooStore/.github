# 🛍️MSA를 이용한 쇼핑몰 프로젝트 (Yaloo Store)
### 서버
- <a href="https://github.com/yalooStore/yalooStore-shop">API Server</a>
- <a href="https://github.com/yalooStore/yalooStore-front">Front Server</a>
- <a href="https://github.com/yalooStore/yalooStore-auth">Auth Server</a>
- <a href="https://github.com/yalooStore/yalooStore-batch">Batch Server</a>
- <a href="https://github.com/yalooStore/yalooStore-gateway">Gateway Server</a>

### 공통 코드 모듈화
- <a href="https://github.com/yalooStore/yalooStore-common-utils">Common Utils</a>

### API Docs
- <a href="https://yeomyaloo.github.io/yalooStore_API_document.github.io/">API Docs</a> 

## Project architecture
![image](https://github.com/yalooStore/.github/assets/81970382/cc7560f2-0f80-40c8-a060-97dc26d73b27)

## ERD
![image](https://github.com/yalooStore/.github/assets/81970382/cc9000d5-516d-422e-b208-490323b73fb2)

## Features
### Shop - API Server
- 클라이언트 요청을 처리하는 api 관련 서버 입니다.
#### 회원
- 회원가입
- 회원 수정
- 회원 삭제(기록은 남게)
- 회원 멤버쉽

#### 상품
- 상품 추가
- 상품 검색
- 전체 상품 검색(모든 회원용)
- 상세 상품 검색
- 상품 삭제

#### 주문


### FE-Server
클라이언트가 요청을 보낼 수 있는 서버로 이곳에서 front를 담당합니다.
#### 회원 관리
- 회원 가입
- 회원 수정
- 회원 삭제
- 회원 로그인
- 회원 로그아웃
#### 인증, 인가
- 인증/인가 서버에게 발급 받은 JWT 토큰 재발급 요청
- RestTemplate 사용 시 Header에 회원 인증정보를 추가(Authorization: Bearer JWT AccessToken)
- 권한별 접근 페이지 구분
#### 장바구니
- 레디스, 쿠키를 사용
- 장바구니 저장
- 회원, 비회원을 구분하여 장바구니 저장
- 장바구니 수정
- 장바구니 삭제
- 장바구니 내의 상품 만료기간 설정으로 자동 삭제
- 회원, 비회원의 장바구니 만료 시간을 다르게 설정
#### 상품
- 전체 상품 출력
- 타입별 상품 출력
- 상품 검색
- 최근 본 상품
- 최근 본 상품 삭제


### Api gateway
- 들어온 요청을 api gateway를 통해 처리할 수 있도록 하여 보안성을 올립니다.

### Auth Server
- front 서버에서 들어온 인증, 인가 관련 처리를 이곳 서버에서 처리합니다.
- spring security를 사용한 인증, 인가 작업을 진행합니다. 
#### 회원 인증
- 인증 작업을 진행하고 해당 회원의 인증이 완료되었다면 jwt를 발급합니다.
- jwt를 accessToken으로 사용해서 세션 대신 상태 유지를 지속해줍니다.
- jwt을 이용한 상태 유지를 위해서 해당 작업에 redis를 사용해 정보를 저장합니다.
#### 회원 인가
- 회원 정보에 따른 회원 역할에 따라서 다른 페이지를 보여줄 수 있게 구성합니다.

  
### Batch Server + spring shceduler
- 회원 생일 기점으로 +n일 후 생일 쿠폰 지급
- 회원 로그인 정보를 가져와 해당 회원이 현 시점 기준으로 1년간 로그인하지 않았다면 휴먼회원으로 상태 변경

## Skill tech 
<img src="https://img.shields.io/badge/{내용}-{배경 색깔}?style={스타일}&logo={로고이름}&logoColor={로고 색깔}"/>
<div>
<img src="https://img.shields.io/badge/spring-6DB33F?style=flat&logo=Spring&logoColor=white"/> 
<img src="https://img.shields.io/badge/springBoot-6DB33F?style=flat&logo=Spring boot&logoColor=white"/>
<img src="https://img.shields.io/badge/spring Security-6DB33F?style=flat&logo=Spring Security&logoColor=white"/>
</div>

