# ✨Brawkurly✨ 

 <br> 
 
 ![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https://github.com/Brawkurly/Brawkurly&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)        
 <br> 
   
## 📌 프로젝트 소개

### 👨‍👩‍👧‍👧 팀원

#### 기획, 디자인, FE  
[![Frontend](https://img.shields.io/badge/Frontend-spy03128-ff69b4.svg?style=flat-square)](https://github.com/spy03128) [![Frontend](https://img.shields.io/badge/Frontend-heogeon0-ff69b4.svg?style=flat-square)](https://github.com/heogeon0)

#### 기획, BE  
[![Backend](https://img.shields.io/badge/Backend-sawol-skyblue.svg?style=flat-square)](https://github.com/sawol) [![author](https://img.shields.io/badge/Backend-workcom0-skyblue.svg?style=flat-square)](https://github.com/workcom0)

### 📅 개발 기간

#### 2022-08-19 ~ 2022-08-24

### 기술 스택 
<div>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=black">
  <img src="https://img.shields.io/badge/react-skyblue?style=for-the-badge&logo=react&logoColor=white">
  <img src="https://img.shields.io/badge/html-red?style=for-the-badge&logo=html&logoColor=black">
  <img src="https://img.shields.io/badge/css-blue?style=for-the-badge&logo=css&logoColor=black">
 </div>
  <div>
  <img src="https://img.shields.io/badge/java-red?style=for-the-badge&logo=java&logoColor=white">  
  <img src="https://img.shields.io/badge/springboot-green?style=for-the-badge&logo=spring&logoColor=white">  
  <img src="https://img.shields.io/badge/springdatajpa-green?style=for-the-badge&logo=spring&logoColor=white">  
  <img src="https://img.shields.io/badge/mysql-yellow?style=for-the-badge&logo=mysql&logoColor=blue">  
  <img src="https://img.shields.io/badge/redis-red?style=for-the-badge&logo=redis&logoColor=black">  
</div> 
 <div>
  <img src="https://img.shields.io/badge/Nginx-green?style=for-the-badge&logo=nginx&logoColor=black">  
  <img src="https://img.shields.io/badge/ubuntu-black?style=for-the-badge&logo=ubuntu&logoColor=red">    
  <img src="https://img.shields.io/badge/aws-orange?style=for-the-badge&logo=aws&logoColor=red">  
  <img src="https://img.shields.io/badge/docker-skyblue?style=for-the-badge&logo=docker&logoColor=white">
 </div>
 
  
<br>
    
 <br> 
   
## 📌 프로젝트 구성

![image](https://user-images.githubusercontent.com/55649302/186349932-c9a60d01-d59d-41d0-a702-d37a2d7f6f83.png)


### 1. 오늘의 판매 현황

- 당일 판매 금액 : 오늘 하루동안 해당 상품의 총 판매 금액입니다.
- 당일 판매 상품 수 : 오늘 하루동안 해당 상품의 총 판매 수입니다.
- 전일 대비 판매 비율 : `오늘 판매수 - 하루 전날의 판매수 / 하루 전날의 판매수 * 100` 입니다.
- 소비자 예약 가격 등록 수 : 오늘 하루동안 해당 상품을 예약한 소비자 수입니다.

### 2. 상품별 소비자 예약 현황

- 해당 상품의 최근 소비자 예약현황 목록입니다.
- 해당 상품의 가격대별 소비자 예약 수입니다.

### 3. 적정 가격

- 현재가 : 현재 마켓컬리에서 판매되는 가격입니다.
- 공급자가 : 공급자의 가격입니다.
- 적정가 : 해당 상품의 가격대 별 소비자 예약 수를 토대로 수익을 계산하여 최대 수익일 경우를 적정가로 설정하고 있습니다.
`(예약 가격 - 공급자 가격) * (예약 수)`

### 4. 상품별 마켓컬리 가격변동

- 7주동안의 마켓컬리에서 해당 상품의 가격변동을 그래프로 표현했습니다.

### 5. 상품별 도매가

- [Karmis](https://www.kamis.or.kr/)에서 제공 받은 API를 토대로 도매가를 보여줍니다.

### 6. 경쟁업체 판매가

- 네이버, 쿠팡, SSG의 해당 상품 가격을 보여줍니다.
- 크롤링을 사용하지 않고, 임의의 값으로 실시간으로 생성하여 보여줍니다.

### 7. 실시간 인기 상품 현황

- 소비자의 예약, 구매 현황을 토대로 인기 상품을 보여줍니다.
  
 <br> 
     
 <br> 
   

## 📌 프로젝트 흐름도

### 1. 소비자 상품 구매

- 소비자가 구매한 데이터는 redis에 저장 되었다가 매일 0시 0분 0초에 mysql로 덤프됩니다.
- redis에 소비자 구매 데이터가 저장되기 때문에 모니터링 시스템에서 빠르게 조회가 가능합니다.

![image](https://user-images.githubusercontent.com/55649302/186343922-bed0dbaf-9284-498e-b92a-6d5889bdf0b0.png)


### 2. 소비자 상품 예약

- 소비자가 예약한 데이터는 redis에 저장 되었다가 매일 0시 0분 0초에 mysql로 덤프됩니다.
- redis에 소비자 예약 데이터가 저장되기 때문에 모니터링 시스템에서 빠르게 조회가 가능합니다.

![image](https://user-images.githubusercontent.com/55649302/186343863-e2c8336c-f1c1-43e0-8765-d4decba4775a.png)


### 3. 관리자 모니터링 시스템

- 도매가 조회를 위한 KAMIS Open API를 사용합니다.
- 오늘 발생한 데이터는 redis에서 조회를 합니다.
- 과거에 발생한 데이터는 MySQL에서 조회를 합니다.

![image](https://user-images.githubusercontent.com/55649302/186348265-dfa42c9d-e4a9-4fe8-b21c-da21c315da8f.png)
