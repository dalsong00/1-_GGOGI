# GGOGI 🥩

---

## 1️⃣ 팀 소개

### 1-1. 프로젝트 Front-end/Back-end 소개

마켓컬리 프로젝트

### 1-2. 개발 인원 및 기간

- 개발기간 : 2023/1/2 ~ 2023/1/13
- 개발 인원 : 프론트엔드 3명, 백엔드 2명
  - 프론트 엔드 : 박예솔, 윤지수, 하평안
  - 백엔드 : 김승수, 김용신
- [백엔드 github 링](https://github.com/wecode-bootcamp-korea/41-1st-GGogi-backend)

### 1-3. 프로젝트 선정이유

많은 사람들이 사용하는 사이트로써 다양한 제품을 고객관점에서 유저 친화적인 UI로 표현하고 마켓컬리의 브랜드 가치를 이해하고 유저 중심적 사고를 체험할 수 있는 좋은 기회라 생각하여 선정하게 되었습니다.

---

## 2️⃣ 서비스 소개

### 2-1. 서비스 타이틀 및 간단 소개

- 높은 기준으로 선별된 품질의 제품을 낮은 가격, 제품 특성을 살린 가장 좋은 상태로 고객에게 빠른 시간내로 배송, 지속가능한 유통과정을 만드는 것

### 2-2. 서비스 목표

- 고객에게 최선의 가격으로 최상의 품질의 식품 제공

---

## 3️⃣ 구현기능 분석

### 3-1. 기술 스택

- `FrontEnd`: React, Javascript, Sass, Git
- `BackEnd`: Javascript, Express, TypeORM, Node.js, Git

### 3-2. 필수 구현 사항

1. 로그인 페이지
2. 회원가입 페이지
   - 회원가입 완료 알람
3. 전체 상품 페이지
   - 필터 사이드바
   - 페이지 네이션
4. 메인 페이지
   - 슬라이드 상품
5. 상품 상세 페이지
   - 상품 설명
   - 상세 정보
6. 마이페이지
   - 적립금
   - 장바구니
   - 개인정보 수정
7. 결제 페이지
8. nav
9. footer

### 3-3. 세부 구현 사항(개인)

1. 로그인
![로그인](https://user-images.githubusercontent.com/114578990/213405434-aafb113a-8a6e-4d78-83d2-6f3dedfdaef1.gif)

   - 백엔드와 POST 메서드로 통신 : result.message 결과에 따라 안내 메세지 띄우기
   - 로컬스트리지에 토큰 저장

2. 회원가입
![회원가입_오류](https://user-images.githubusercontent.com/114578990/213405480-86394c95-350e-434e-8213-041490fb9169.gif)

   - 백엔드와 POST 메서드로 통신
    : 유효성 검사 규칙을 충족하지 못할 경우 result.message에 따라 안내 메세지 띄우기 
    (이메일 중복검사, 이메일과 비밀번호 형식, 빈칸 유무)
  
3. 장바구니
![장바구니_결제](https://user-images.githubusercontent.com/114578990/213405530-45fbd2c7-5647-4b3f-8b7d-78bb53f50d9d.gif)

   - GET 매서드로 메인 및 상세 페이지에서 담은 품목들을 장바구니 화면에서 보여주기
   - DELETE 매서드로 서버에서 품목을 삭제, filter() 활용하여 삭제한 품목을 제외하고 다시 cartList에 아이템 담아주기
   - PATCH 매서드로 주문하기 버튼을 눌렀을 때 변경된 품목의 cartId와 productId, quantity 데이터 서버로 보내주기

4. 결제
   - POST 매서드로 총 합계와 장바구니에 담긴 항목의 cartId, productId, quantity, price 서버로 보내주기

### 회고록
- ![회고록 링크](https://dalsong-00.tistory.com/36)
### Reference

이 프로젝트는 마켓컬리 사이트를 참조하여 학습목적으로 만들었습니다.
실무수준의 프로젝트이지만 학습용으로 만들었기 때문에 이 코드를 활용하여 이득을 취하거나 무단 배포할 경우 법적으로 문제될 수 있습니다.
이 프로젝트에서 사용하고 있는 사진 대부분은 위코드에서 구매한 것이므로 해당 프로젝트 외부인이 사용할 수 없습니다.
