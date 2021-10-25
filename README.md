# 집주인 몰~래 복덕복덕

## [프로젝트소개]

**세상에 집이 이렇게나 많은데 도대체 내가 살 집은 어디있는걸까?**


여러분들의 발품을 최소한으로 하기 위한 **익명의 자취방 리뷰 사이트!**

인증을 통하여 실제 거주했던 분들만 리뷰 게시글 작성이 가능합니다

가감없는 자취방 리뷰를 참조해보세요



## [개발 환경]

IDE : IntelliJ

Springboot 2.5.6

Project Type : Gradle

JDK11

Dependencies

- Database : H2
- Web / JPA / Security / Thymeleaf / OAuth2 / Mail / Lombok

프로젝트 인원 : 5명

프로젝트 기간 :  4주



#### [DB 설계도](https://github.com/2miri/springboot-final-project/blob/main/DB%20%EC%84%A4%EA%B3%84%EB%8F%84.png)

#### [API명세서](https://github.com/2miri/springboot-final-project/blob/main/API%20%EB%AA%85%EC%84%B8%EC%84%9C.md)

#### [API 화면구성도](https://github.com/2miri/springboot-final-project/blob/main/API%20%ED%99%94%EB%A9%B4%EA%B5%AC%EC%84%B1%EB%8F%84.pdf)



## [본인이 맡았던 기능 소개]

#### 각자 기능을 맡았던 페이지들은 CSS까지 모두 담당하였습니다.

- 웹사이트 이름 & 로고
- 로그인
- 아이디 찾기
- 리뷰페이지 목록 
- 관리자페이지 (승인/거부)



### [프로젝트 시연 영상]

<div>
	<a href="https://www.youtube.com/watch?v=7M-_mYNW3TA" target="_blank"><image width="80%" src="https://img.youtube.com/vi/7M-_mYNW3TA/mqdefault.jpg"></a>	
</div>




### [프로젝트 사용 화면]



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138743974-092edd3d-b269-46ed-af9f-451df2a55d92.jpeg"/>

#### ▲ 메인페이지

검색창은 리뷰 페이지와 동일한 검색결과로 처리됩니다.

인기있는 리뷰글 (회전목마 형식) / 커뮤니티 인기글 / 자취방 꿀팁을 좋아요순으로 보여줍니다.



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138743982-faad155b-b16b-4805-b2c1-edafd329af40.jpeg"/>

#### ▲ 회원 가입



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138743984-75d2cd3a-f0e9-48ac-9231-801059fe3e3f.jpeg"/>

#### ▲ 로그인



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138743987-5084b15c-dfa9-4d0f-8c60-3d749bc9edb0.jpeg"/>

#### ▲ 일반회원 로그인했을 때의 메인 화면

부트스트랩을 이용하여 프로필 바를 구현했습니다.



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138743988-9b876fcf-cd4c-46bc-91ca-7ec0b79c35cc.jpeg"/>

#### ▲ 리뷰글 목록 (기본) 

관리자가 승인한 리뷰글만 보이도록 합니다.

게시글 페이징은 무한스크롤 형식입니다.

하트를 누르면 좋아요 또는 좋아요 취소가 적용됩니다.



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138743989-56cb3cd8-4d7e-460d-b487-f3a8016193f4.jpeg"/>

#### ▲ 리뷰글 목록 (검색 옵션창을 눌렀을 때) 

검색에서 옵션을 누르면  지역, 방형태 등 원하는 리뷰에 관련된 카테고리를 선택 할 수 있습니다.

옵션 / 포토리뷰 / 정렬은 각각의 기능을 누르면 바로 화면이 변환되도록 AJAX로 처리했으며,
	
선택한 카테고리/포토리뷰/정렬 모두 적용된 채 키워드 및 태그로 검색 가능합니다.



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138743991-2e5fb06d-dc00-4976-a992-8b1b01c8e020.jpeg"/>

#### ▲ 리뷰글 읽기 / 수정 / 삭제

지도 API를 이용하여 리뷰에 작성된 주소의 지도를 불러옵니다.

댓글과 대댓글 기능을 구현



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138743993-8f28adfe-8a2b-4fce-a00b-2f47ed77cc06.jpeg"/>

#### ▲ 리뷰글 쓰기 

리뷰에 관련된 사진을 올리면 작성자가 바로 이미지를 보기 또는 삭제 할 수 있습니다.



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138743995-55de97f1-9d6c-4135-84b5-256c2f6600f9.jpeg"/>

#### ▲ 관리자로 로그인했을 때의 메인화면

관리자로 로그인하면 관리자페이지라는 메뉴가 추가적으로 보입니다.



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138743997-1ead7758-b84a-463d-b2b9-9395cb601e5b.jpeg"/>

#### ▲ 관리자페이지

사용자가 리뷰글을 작성하면 바로 리뷰 목록에 게시되는 것이 아니라

승인 대기 상태가 됩니다.

관리자는 승인 대기 상태인 게시물에 승인 / 거부 처리를 하고

승인이 됐을 때만 리뷰 게시판에 글이 보입니다.



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138743998-848e81a3-674e-4c2d-ad04-7981b9cf6795.jpeg"/>

#### ▲ 관리자일때 리뷰 게시물 보기

일반 회원은 보이지 않는 리뷰 작성자가 글을 작성할때 해당 건물에 거주했는지에 관한 인증 파일이 보입니다.

인증 파일과 해당 글의 내용을 검토하고 승인 / 거부를 결정합니다.



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138744001-506f0d3f-8ba7-4cd1-9b76-6cea0130a2c5.jpeg"/>

#### ▲ 커뮤니티글 목록

페이징처리를 하였으며, 검색 / 카테고리선택 / 정렬 기능이 있습니다.



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138744004-2bb56136-226f-4559-802f-d21290c9f6c6.jpeg"/>

#### ▲ 커뮤니티글 쓰기



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138744005-2f8860e6-6728-488e-8703-0c06fc6d2efa.jpeg"/>

#### ▲ 마이페이지

개인정보 변경, 내가 쓴 글(리뷰/커뮤니티), 로그아웃, 회원탈퇴



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138744006-3e78b9d1-95eb-465b-8bc1-971744f0e493.jpeg"/>

#### ▲ 비밀번호 변경



<img width="50%" src="https://user-images.githubusercontent.com/83326164/138744009-11a15be9-0f3e-4e5c-a5ab-82153064897c.jpeg"/>

#### ▲ 아이디 찾기





#### 

### [팀프로젝트를 하면서]

#### 만족스러운 점

1. 내가 맡은 페이지의 기능 그대로 구현하기
2. 팀 회의를 하며 각각의 페이지를 정해진 기한내에 완수하기

이 두가지를  중요하게 생각하며 프로젝트를 시작했는데,  이것을 이룬것이 가장 만족스럽다.



#### 힘들었던 점

1. 여러 카테고리 중복 적용

   카테고리 갯수가 많지 않고  단일 선택이라면 레파지토리에서 findAllBy@ 이런식으로 간단하게 DB상에 검색이 가능하게 하면 되지만, 집 이라는 매개체의 특성상 방크기,건물,계약 등등 카테고리가 많고

   findAllBy@and@and@and... 이런식으로 하기에는 너무 길고

   가장 중요한건 사용자가 어떤 카테고리를 누를지 모르는데 총 22개의 카테고리를 경우의 수 별로 모두 메서드를 만들 수가 없었다.

   그러다 Spring Data JPA의 Specification을 알게 되었다.

   이 객체를 통해서 검색 조건을 추상화 할 수 있고, 리턴 자료형을 Specification<@>으로 두는 메서드를 만들고 해당 메서드 내부에서는 list와 switch문 그리고 자료형 Predicate를 이용해 알맞는 검색조건에 추가하는 방식으로 구현했다.

   Specifications을 사용하면 두개 이상의 specfication을 and나 or등으로 조합 할 수 있다.

    이것을 이용하여 레파지토리에서 findAll 메서드의 매개변수로 넣어주기만 하면 된다.

   예. findAll(**Specification<Review>** spec)

   

2. AJAX

   AJAX를 진행할 때 이미지나 a태그를 교체하는 등의 간단하게 바꾸는 것은 어렵지 않았지만, 

   무한스크롤을 할 때 페이징 처리를 하고 그 페이지에 해당되는 내용들의 게시물 목록을 불러와야 할 때 구글링을 아무리 해봐도 JSON으로 데이터를 넘기고 받아서 "<div>" + data + "</div>" 이런식으로 모두 하나하나 타이핑을 해야하는 방법이 대다수였다.

   게시글에 부트스트랩도 입혀야해서 모두 작성하기에는 너무 길고 비효율적이라 생각하였고, 나는 이미 만들어둔 게시판 목록의 div내의 thymeleaf양식을 그대로 쓰고 해당되는 data만 바꾸길 원했다.

   구글링, 유튜브, 까페 등 여러 곳에서 될 것같은 것들을 긁어모아 

   Json이 아닌 ModelAndView로 넘기면 된다는 것을 찾고, 해당되는 게시글들의 페이징의 내용들을 담당하는 div를 통째로 복사하여 html파일을 따로 만든 후에 스크롤을 내릴때마다 append해주었다.

   

3. 타임리프

   타임리프는 에러가 발생하면 어느 부분에서 에러가 났는지 정확히 메세지가 나오지 않을 때가 대부분이라 문법의 어떤 부분에서 에러가 났는지를 몰라서 문법을 모두 하나하나 보느라 굉장히 고생했다.

   

#### 아쉬운 점

부트스트랩을 사용하여 더 예쁘고 트랜디하게 꾸미고 싶었는데

깔끔하게 꾸미는 것만으로도 시간이 많이 소요되어 아쉽다.

마감을 지키지 못하고 맡은 기능을 거의 구현하지 못한 사람이 있어서

급하게 다른 팀원들이 나눠서 맡았는데 시간이 너무 촉박했다.

처음 사이트를 만들자고 계획했던 전체적인 그림에서 빠진 기능들이 많아서 아쉽다



#### 느낀 점



미니프로젝트 때에는 겹치는 부분이 없어서 느끼지 못했는데

팀프로젝트는 나만 열심히 한다고 되는 게 아니란 걸 깨달았다.

팀원들과 조율과 협업이 굉장히 중요하고 서로의 진도를 꼭 체크해야한다고 느꼈다.

그래도 결국 프로그래머는 자기 자신과의 싸움이다

내가 맡은 기능을 해내지 못하고 기능 구현을 줄이거나 바꿔버리면

너무 자존심 상할 것 같아서 진짜 열심히했고 내가 원래 맡았던 기능들은 모두 해내서 뿌듯하다.

