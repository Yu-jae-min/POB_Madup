# Madup

날짜별 데이터를 집계하여 데이터 시각화를 통해 차트로 확인할 수 있습니다.

<br />

## 🎉 **배포 주소**

- [https://madup7b.netlify.app/](https://madup7b.netlify.app/)

<br />

## 👬 **팀원**

- 프론트엔드 5명

<br>

## 📅 **개발 기간**

- 2022년 05월 23일 ~ 2022년 05월 26일

<br />

## 🔧 **기술스택**

- Typescript, React, SASS, recoil

<br />

## 💻 **설치 및 실행 방법**

1. yarn 설치

```
 npm i yarn
```

2. repository 클론

```
git clone https://github.com/Yu-jae-min/POB_Madup.git
```

3. dependencies 설치

```
yarn install
```

4. 실행

```
yarn start
```

## 📒 **구현 목록**

|                                                    대시보드(광고관리)                                                    |                                                 대시보드(매체현황)                                                 |                                                 광고관리(통합광고)                                                 |
| :----------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------: |
| ![광고관리](https://user-images.githubusercontent.com/85284246/172768213-f46ef85a-275a-411f-9974-65a3cde39c5e.png) | ![매체현황](https://user-images.githubusercontent.com/85284246/172768225-566def1b-ce7d-40cf-a00c-9ee153aa9e1a.png) | ![통합광고](https://user-images.githubusercontent.com/85284246/172768229-c6f6e4d3-1946-4a16-a7dd-f2179f0dbe1d.png) |

<br />

### # **공통**

- [x] recoil을 통한 날짜 데이터 상태 관리

<br />

### # **사이드바**

![ezgif com-gif-maker](https://user-images.githubusercontent.com/90893364/170345542-faa94bd2-82a6-44ae-a68d-36d65953f17a.gif)

- [x] react-router-dom의 NavLink를 이용하여, 버튼 클릭 시 활성화 된 메뉴 스타일 지정 및 페이지 이동

- [x] 임의로 지정한 시간동안 로딩화면 표시(500ms)

- [x] 유지되어야 하는 값들을 recoil을 통해 관리

<br />

### # **대시보드 / 캘린더**

![ezgif com-gif-maker (1)](https://user-images.githubusercontent.com/90893364/170346268-7a41d2dd-9eb1-4168-86bf-2121f78f6c48.gif)

- [x] react-date-range 라이브러리를 사용한 캘린더 구현

- [x] 2월 1일부터 4월 20일까지로 선택범위 제한

- [x] recoil을 이용한 startDate와 endDate 상태값 저장

<br />

### # **대시보드 / 통합 광고 현황**

![ezgif com-gif-maker (2)](https://user-images.githubusercontent.com/90893364/170346915-90e80781-ee1a-422d-8024-6ef47999aae2.gif)

<br />

![ezgif com-gif-maker (5)](https://user-images.githubusercontent.com/90893364/170403958-ebbe048e-80d7-4b14-97e2-4efa991eebbf.gif)

- [x] 선택날짜 범위의 총계 및 이전 선택 날짜 범위 비교하여 증감분 구현

- [x] 첫번째 드롭다운에서 선택한 지표를 두번째 드롭 다운에서 선택할 수 없으며, 두번째 드롭다운 선택은 옵션

- [x] 지표 별로 단위(%, 원) 등 변경 표시, 2가지 드롭 다운이 모두 선택될 경우, 그래프를 Hover 시 2가지의 그래프의 툴팁 값들의 수직으로 점선이 그려짐

- [x] 그래프 선 위에 Hover 시 그 위치에 맞는 툴팁(값)이 박스 행태로 보여짐

- [x] 오른쪽 드롭다운에 일별, 주간으로 선택이 가능하고, 그에 맞게 x축 값과 그래프 값이 정렬됨

<br />

### # **대시보드 / 매체현황 (담당 기능)**

![ezgif com-gif-maker (3)](https://user-images.githubusercontent.com/90893364/170347800-36d499b3-49a8-4aef-832f-1c6741a5517d.gif)

- [x] 선택 날짜에 따른 데이터 집계와 총계를 나타내는 테이블 구현

  - [x] 전체 데이터 중 각 회사별 데이터를 구분하여 집계하는 로직 구현

  - [x] 구분된 각 회사별 데이터를 총합하는 총계 로직 구현

  - [x] `toLocaleString` 을 사용해서 자릿수 구분 기호 표기

- [x] 선택 날짜에 따른 victory.js를 활용한 데이터 시각화 차트 구현

  - [x] lodash 라이브러리의 cloneDeep 을 활용한 깊은 복사와 forEach 메소드를 활용한 데이터 총계 로직 구현

  - [x] 차트 막대는 날짜 데이터를 percent로 변환하여 최대 크기를 동일하게 유지

  - [x] 차트에 마우스 오버 시 tooltip 생성, tooltip에는 각각의 데이터를 삽입

<br />

### # **광고 관리**

![ezgif com-gif-maker (4)](https://user-images.githubusercontent.com/90893364/170349089-fdf9dc91-e6e3-4cde-98a4-802bea858fa3.gif)

- [x] 받아온 데이터의 status 값에 따라 '전체광고', '진행중인광고', '중지광고'로 구분해서 표시, 선택한 드롭다운 값은 recoil에 저장

- [x] adType 값(web,app)에 따라 광고 제목 앞에 prefix(앱광고, 앱광고) 설정

- [x] endDate 값이 null이 아니면, 광고 생성일 옆에 광고 종료일 추가 삽입

- [x] `budget`의 값을 각각 1,000과 10,000으로 나누어 몫의 크기와 나머지의 유무에 따라서 화폐 표시 단위를 결정

- [x] 각 값을 10,000으로 나누어 나머지는 버림하고 `toLocaleString` 을 사용해서 자릿수 구분 기호 표기

<br />
