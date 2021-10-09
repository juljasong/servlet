### 단축키
- ctrl + alt + M -> Extract Method
- ctrl + o -> 관련 method 자동 생성
- iter + enter -> enhanced for문
- ctrl + shift + t -> Test
- alt + enter
  - static import
  - 변수 자동 생성


### MVC (Model-View-Controller)
- Controller: HTTP 요청을 받아 파라미터를 검증하고, 비즈니스 로직을 실행함. 그리고 뷰에 전달할 결과 데이터를 조회하여 모델에 담음
- Model: 뷰에 출력할 데이터를 담아둠. 뷰가 필요한 데이터를 모두 모델에 담아 전달해주는 덕분에 뷰는 비즈니스 로직이나 데이터 접근을 몰라도 되고, 화면을 렌더링하는 일에 집중할 수 있음
- 뷰: 모델에 담겨있는 데이터를 사용해 화면을 그리는 일에 집중. 여기서는 HTML을 생성하는 부분을 말함
- 참고: 컨트롤러에 비즈니스 로직을 둘 수도 있지만, 이러면 컨트롤러가 너무 많은 역할을 담당하기 때문에 일반적을오 비즈니스 로직은 서비스(Service)라는 계층을 별도로 만들어 처리함. 그리고 컨트롤러는 비즈니스 로직이 있는 서비스를 호출하는 담당.
- 한계
  1. forward의 중복
  2. ViewPath의 중복
  3. 공통 처리 어려움