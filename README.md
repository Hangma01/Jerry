## :interrobang: 프로젝트 소개
실시간 영화 예매 사이트 (JERRY)

> 기간 : 2024.07.24~2024.08.21
> 
> 팀원 : 5명
>
> 

<br>

## :seedling: 개발 환경
### FrontEnd
- JavaScript, JSP, jQuery


### Backend
- Java, Spring, Mybatis, Apache Tomcat, Oracle


### Collaboration & Tools
- Github, Jira
### ETC
- ProtOne API, OAuth2(Google, Kakao, Naver)
<br><br><br>

## :busts_in_silhouette: 담당 역할
### FrontEnd, BackEnd
  - 영화 예매 페이지
  - 영화 좌석 선택 페이지
  - 영화 결제 페이지 [ PortOne API ]

<br><br><br>

## :dart: 담당 주요 기능

### 1. 영화 예매 페이지
  - 사용자 경험을 높이기 위해 한 Column의 Item 클릭 시 다른 Column의 Item들 중 선택 가능한 Item들은 활성화 그 외는 비 활성화 되는 기능
    
* * *
<img src="https://github.com/user-attachments/assets/ddfc2c1c-92c6-45df-bb2a-df6141f79178" width="600" height="450"/>

* * *
<br><br>


### 2. 영화 좌석 선택 페이지
  - 사용자가 지정한 인원수에 비례하게 좌석 선택 시 시각적으로 선택 완료를 보여줌
  - 실시간 가격 변동 기능
    
* * *
<img src="https://github.com/user-attachments/assets/8c16cbdf-6f9e-452d-9f94-aaa3f7a482bc" width="600" height="450"/>

* * *
<br><br>


### 3. 영화 결제 페이지
  - 쿠폰을 사용하여 할인을 적용할 수 있음
  - 결제 완료 후 이미 예약된 좌석일 경우 환불 처리됨

* * *
<img src="https://github.com/user-attachments/assets/ea58997e-a88c-48af-8cf0-00a8bbf0cc82" width="600" height="450"/>

* * *
<img src="https://github.com/user-attachments/assets/91c1b690-7022-4ac1-a174-1abf02e63fbf" width="600" height="450"/>

* * *

<br><br>


## :gun: 트러블 슈팅

### XML 태그 인식
    XML에서 부등호 사용 시 태그로 인식이 되는 에러가 발생했다.
    이를 해결하기 위해 태그가 있는 쿼리를 CDATA로 감싸 문자열로 치환하여 해결하였다.

### imp_uid
    결제 취소를 하려면 PortOne API 경우 imp_uid가 필수였지만 DB 설계 시 이 부분을 빠트려
    프로젝트 후반부에 급하게 추가함으로써 다시 테스트를 진행해야 했었다. 프로젝트 마무리는 잘 되었지만,
    외부 API 사용 시 문서를 꼼꼼하게 읽어 놓친 부분이 없는지 팀원들과 더블 체크를 하여 수정될 만한 상황이
    발생하지 않도록 해야겠다고 깨달았다.

### 선착순 결제
    영화관 좌석을 선택했을 때 여러 명이 동시에 들어올 수 있어 중복 결제가 발생한다.
    이를 방지하기 위해 결제가 완료된 후에 DB를 확인하여 이미 예약된 좌석인지 체크해
    예약된 좌석이 존재한다면 환불 처리가 진행되도록 했다.
    더 보완할 점은 좌석 선택 시 1명만 결제 페이지로 이동하게 해야 된다.

    
<br>  

    

<br><br><br>

# :receipt: Reference
- 디자인은 CGV, MemaBox. LotteCinema 사이트를 참고하여 만들었으며 현 사이트는 상업적 목적으로 사용하지 않습니다.
