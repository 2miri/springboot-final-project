## 메인 페이지

- 로고 클릭 - 메인 페이지로

  - 요청 url : https://bokduck.com

  - 요청 방식 : GET

  - 응답 타입 : text/html

  - 디렉토리 : index.html

    

- 로그아웃 버튼 클릭 - 로그인 후 가능

  - 요청 url : https://bokduck.com/logout

  - 요청 방식 : POST

  - 응답 타입 : text/html

  - 디렉토리 : member/logout.html

    


  ## 회원가입 ("/signup")

- 회원가입 버튼 클릭 - 회원가입 페이지로 넘어감

  - 요청 url : https://bodcuk.com/signup

  - 요청 방식 : GET

  - 응답 타입 : text/html

  - 디렉토리 : member/signup.html

    

- 회원가입 페이지에서 폼을 입력한 후 '회원가입' 버튼을 눌렀을 때 - AJAX

  - 요청 url : "https://www.bokduck.com/signup"

  - 요청 방식 :  POST

  - 요청 파라미터  

    - username : 아이디
    - password :  비밀번호
    - tel : 핸드폰 번호
    - nickname :  닉네임
    - userAddress : 주소
    
  - 응답 타입 :  application/json

  - 응답 구조

    - result : "success" 혹은 "fail" (string)

    - 성공 :  index.html

    - 실패 : alert("회원가입에 실패하였습니다")->/member/signup.html

      

## 로그인 

- 로그인 버튼 클릭 - 로그인 페이지로 넘어감

  - 요청 url : https://bokduck.com/login

  - 요청 방식 : GET

  - 응답 타입 : text/html

  - 디렉토리  : member/login.html

  

- 로그인을 시도했을 때 

  - 요청 url : https://www.bokduck.com/login
  - 요청 방식 : POST

  - 응답 형식 : text/html

  - 요청 파라미터

    - username : 사용자 아이디(이메일)
    - password : 사용자 비밀번호

  - 디렉토리

    - 실패 : member/login.html - 로그인 페이지 그대로

    - 성공 : index.html - 메인 페이지로 돌아감

  


​           

- 네이버 로그인
- 요청 url : https://www.bokduck.com/login/oauth2/code/naver
  
- 요청 방식 : GET
  
- 응답 형식 :  text/html
  
- 응답 구조 
  
  - 성공 : index.html  


​           

- 카카오 로그인 

  - 요청 url : https://www.bokduck.com/login/oauth2/code/kakao

  - 요청 방식 : GET

  - 응답 형식 :text/html

  - 응답 구조 

    - 성공 : index.html 

      

- 구글 로그인

  - 요청 url :  https://www.bokduck.com/login/oauth2/code/google
  - 요청 방식 : GET
  - 응답 형식 : text/html
  - 응답 구조 
    - 성공 : index.html  

  

- 아이디 찾기 버튼 누름  

  - 요청 url : https://www.bokduck.com/idsearch
  - 요청 방식 : GET
  - 응답방식 : text/html
  - 디렉토리 : member/idsearch.html

  

- 아이디 찾기  - 핸드폰 인증 (핸드폰 인증 api 사용 -> 사이트로 넘어가기) 
  - 요청 url : https://www.bokduck.com/id/search ** api 사이트로 넘어가야 함.

  - 요청 방식 : POST

  - 요청 파라미터

  - 응답 타입 : text/html

  - 디렉토리 : 성공 -> : https://www.bokduck.com/id/search/result 

    ​           

- 아이디 찾기 인증 - 성공 - 아이디 보여줌 - AJAX

  - 요청 url : https://www.bokduck.com/id/search/result
  - 요청 방식 : GET

  - 요청 파라미터

    - tel : 핸드폰 번호

  - 응답 타입 : application/json

  - 응답 구조 : member/idsearch.html


​         

- 비밀번호 바꾸기 버튼 눌렀을때  

  - 요청 url :  https://www.bokduck.com/password 
  - 요청 방식 : GET
  - 응답방식 : text/html
  - 응답 구조 : member/passwordsearch.html 


​       

- 비밀번호 바꾸기_아이디 확인

  - 요청 url : https://www.bokduck.com/password 

  - 요청 방식 : POST

  - 요청파라미터 

    - username : 아이디(이메일)

  - 응답타입 : application/json

  - 디렉토리

    - 이름 :  result : "success" 혹은 "fail" (string)

    - 성공 : alert("메일로 비밀번호 변경 페이지가 전송 되었습니다")

      -> 이메일로 비밀번호 바꾸는 페이지 전송함
    
      실패 : alert("없는 아이디 입니다.")


​           

 - .비밀번호 바꾸는 페이지 

   - 요청 url : https://www.bokduck.com/password/change
   - 요청 방식 : POST
   - 요청파라미터 

     - password : 바꾼 새로운 비밀번호
   - 응답 타입 : html/text
   - 디렉토리 : alert("변경 되었습니다") -> member/login.html 

     



# 리뷰



- 리뷰 버튼 클릭 - 리뷰 페이지로 넘어감
  - 요청 url : https://bokduck.com/review/list
  - 요청 방식 : GET
  - 응답 타입 : text/html
  - 디렉토리 : post/review/list.html



- #### 자동완성 -  AJAX

  - 요청 url : https://www.bokduck.com/review/autosearch
  - 요청 방식 : POST
  - 응답 타입 : application/json
  - 응답 파라미터 : content - 검색 내용?
  - 응답구조 :
    - 이름 - result : "success" 혹은 "fail" (string)
    - 지역 , 태그 자동완성 -> DB에서 가져옴



- 리뷰 검색 

  - 요청 url :   https://www.bokduck.com/review/search

  - 요청 방식 : GET

  - 응답 파라미터

    - search : 검색한 내용 
    - reviewCategorys : 리뷰 카테고리

  - 응답 타입 : text/html

  - 디렉토리 : post/review/list.html

    

- 글 리스트에서 '좋아요' 버튼을 눌렀을 때 - AJAX

  - 요청 url : https://www.bokduck.com/review/list/like
  - 요청 방식 :  post
  - 요청 파라미터 

    - reviewId : 좋아요 한 글 번호
  - 응답 타입 :  application/json
  - 응답구조  :  -
    - 이름  result : "success" 혹은 "fail" (string)
    - 성공 : 하트 색 바뀜
    - 실패 : 하트 색 그대로
  
  
  
- 특정 리뷰 눌렀을때 - 상세리뷰로 들어감

  - 요청 url :   https://www.bokduck.com/review/read

  - 요청 방식 : get

  - 응답 파라미터

    - reviewId  : 누른 리뷰 id

  - 응답 타입 : text/html

  - 디렉토리 : post/review/read.html

    

- 상세 리뷰에서 좋아요 눌렀을때 - AJAX

  - 요청 url :   https://www.bokduck.com/review/read/like
- 요청 방식 : post
  
  - 응답 타입 : application/json
- 응답 파라미터 
  
  - reviewId : 좋아요 한 글 번호
  - 응답 구조 : 
  - 이름  result : "success" 혹은 "fail" (string)
    - 성공 : 하트 색 바뀜
  - 실패 : 하트 색 그대로



- 리뷰 - 글쓰기  버튼을 눌렀을 때

  - 요청 url : https://www.bokduck.com/review/write
  - 요청 방식 :  get
  - 응답 타입 : text/html
  - 디렉토리 : post/review/write.html

  

- 리뷰 -  작성 후 '게시' 버튼 누를 때 

  - 요청 url : https://www.bokduck.com/review/write

  - 요청 방식 : post

  - 요청 파라미터

    - photo_url : 사진  
    - adress : 주소  
    - categories : 카테고리  
    - content :리뷰내용  
    - tag : 태그 
    - stars : 별점  
    - short : 한줄평  
    - certification_url : 인증 pdf 파일

  - 응답 타입 : text/html

  - 디렉토리 :  /post/review/read.html

    

- 리뷰 - 수정하기  버튼을 눌렀을 때

  - 요청 url : https://www.bokduck.com/review/modify

  - 요청 방식 :  get

  - 요청 파라미터

    - reviewId : 수정할 글 번호

  - 응답 타입 : text/html

  - 디렉토리 : post/review/write.html

    

- 리뷰 -  수정 후 '게시' 버튼 눌렀을 때

  - 요청 url :   https://www.bokduck.com/review/modify

  - 요청 방식 :  post

  - 요청 파라미터

    - reviewId : 수정 할 글 번호
    - photo_url : 사진  
    - categories : 카테고리  
    - content :리뷰내용 
    - tag : 태그 
    - stars : 별점  
    - short : 한줄평

  - 응답 타입 : text/html

  - 디렉토리 :   post/review/read.html

    

- 리뷰 -  삭제 - AJAX

  - 요청 url :  https://www.bukduck.com/review/delete
  
  - 요청 방식 :  get
  
  - 요청 파라미터
    
    -   reviewId : 리뷰 번호
    
  - 응답 타입 :   application/json
  
  - 응답 구조 
  
    - 이름  result : "success" 혹은 "fail" (string)
  
    - 성공 : alert(“이 글을 삭제하시겠습니까?”) ‘예’ 누르면redirect:/post/review/list.html, , 아니요- 그대로
  
    - 실패 : alert("실패 되었습니다") ->post/review/read.html
  
      


​     

- 댓글 달기 - AJAX

  - 요청 url : https://www.bokduck.com/review/read/comment
  - 요청 방식 : post
  - 요청 파라미터

    - reviewId : 리뷰 글 번호 
    - content: 댓글 내용
  - 응답 타입 : application/json
  - 응답 구조 
    - 이름  result : "success" 혹은 "fail" (string)
    - 성공 -> 로그인돼있을 때 : 댓글 올라감
    - 실패 -> 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/review/list.html
  
  
  
- 댓글 - 수정 AJAX

  - 요청 url : https://www.bokduck.com/review/read/comment/modify
  - 요청 방식 : post
  - 요청 파라미터

    - reviewId : 리뷰 번호  
    - content: 수정된 댓글 내용
  - 응답 타입 : application/json
  - 응답 구조 : 
    - 이름  result : "success" 혹은 "fail" (string)
    - 성공 -> 로그인돼있을 때 : 수정된 댓글이 올라감
    - 실패 -> 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/review/list.html

  

- 댓글 - 삭제 ajax

  - 요청 url : https://www.bokduck.com/review/read/comment/delete
  - 요청 방식 : POST
  - 요청 파라미터

    - reviewId : 댓글 번호
  - 응답 타입 : application/json
  - 응답 구조 : 
    - 이름  result : "success" 혹은 "fail" (string)
    - 성공 -> 로그인돼있을 때 :  alert("정말 삭제하시겠습니까?") -> 예 :댓글 삭제됨 아니요-> 그대로
    - 실패 -> 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/review/list.html

  

- '대댓글달기' 버튼을 눌렀을 때 - AJAX

  - 요청 url : https://www.bokduck.com/review/read/recomment

  - 요청 방식 :  post

  - 요청 파라미터 :

    -  commentId : 부모댓글 번호

  - 응답 타입 : application/json

  - 응답 구조 : 

    - 이름  result : "success" 혹은 "fail" (string)

    - 성공 -> 로그인돼있을 때 : 텍스트창이 뜬다

    - 실패 -> 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/review/list.html
    
      

- 대댓글 달기 실행 -AJAX

  - 요청 url : https://www.bokduck.com/review/read/recomment/active

  - 요청 방식 : post

  - 요청 파라미터

    - reviewId : 리뷰 글 번호 
    - content: 댓글 내용
    - parentId : 부모 댓글 번호 

  - 응답 타입 : application/json

  - 응답 구조 : 

    - 이름  result : "success" 혹은 "fail" (string)
    - 성공 -> 로그인돼있을 때 : 대댓글 올라감
    - 실패 -> 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/review/list.html
    
    

- 대댓글 - 수정 AJAX

  - 요청 url : https://www.bokduck.com/review/read/recomment/modify
  - 요청 방식 : post
  - 요청 파라미터

    - content: 수정된 댓글 내용
    - commentId : 댓글 번호
  - 응답 타입 : application/json
  - 응답 구조 : 
    - 이름  result : "success" 혹은 "fail" (string)
    - 성공 -> 로그인돼있을 때 : 댓글 수정 됨
    - 실패 -> 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/review/list.html


​       

- 대댓글 - 삭제 - AJAX

  - 요청 url : https://www.bokduck.com/review/read/recomment/delete

  - 요청 방식 : POST

  - 요청 파라미터

    - commentId : 댓글 번호

  - 응답 타입 : application/json

  - 응답 구조 : 

    - 이름  result : "success" 혹은 "fail" (string)
    - 성공 -> 로그인돼있을 때 :  alert("정말 삭제하시겠습니까?") -> 예 :댓글 삭제 됨 아니요-> 그대로
    - 실패 -> 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/review/list.html
    
    

---

  ### 커뮤니티("/community")

  

 - '커뮤니티' 버튼 클릭 - 커뮤니티 페이지로 넘어감
   - 요청 url : https://bokduck.com/community/list

   - 요청 방식 : GET

   - 응답 타입 : text/html

   - 디렉토리 : post/community/list.html

  


 - 카테고리 버튼을 눌렀을 때 -AJAX

   - 요청 url : https://www.bokduck.com/community/list

   - 요청 방식 :  get

   - 요청 파라미터 : category

   - 응답 타입 : application/json

   - 응답 구조 : post/community/list.html


​         

- 스크롤할 때 - AJAX

  - 요청 url : https://www.bokduck.com/community/list/scroller
  - 요청 방식 :  post
  - 요청 파라미터 :
  - categoryName : 카테고리 이름
    
  - pagenum : ajax 요청할 번호
  - 응답 타입 : application/json
  - 응답 구조 : { items : [ {title:  content:  }, {title:  content: }, {title:  content: }, {title:  content:}, {title:  content:}, {title:  content:}, {title:  content:}, {title:  content:}, {title:  content:}, {title:  content:} ] }
    - 이름  result : "success" 혹은 "fail" (string)
    - 성공 -> 다음 pagenum 으로 감
    - 실패 -> 끝 번호 다음 pagenum 없음 -> 그대로


​         

 - #### 자동완성 -  AJAX

   - 요청 url : https://www.bokduck.com/community/autosearch
   - 요청 방식 : POST
   - 응답 타입 : application/json
   - 응답 파라미터 : content - 검색 내용?
   - 응답구조 :
     - 이름 - result : "success" 혹은 "fail" (string)
     - 태그 자동완성 -> DB에서 가져옴

  


 - #### 정렬 버튼 눌렀을 때

   - 요청 url : https://www.bokduck.com/sort
   - 요청방식 : GET
   - 요청 파라미터 : sortType(최신순, 인기순)
   - 응답 타입 : text/html
   - 응답 구조 : /post/community/list.html

  


- 글 리스트에서 '좋아요' 버튼을 눌렀을 때 - AJAX


    - 요청 url : https://www.bokduck.com/community/list/like
    - 요청 방식 :  post
    - 요청 파라미터  
    
      - communityId : 글 번호
    - 응답 타입 : application/json
    - 응답 구조 : 
    
      - 이름 - result : "success" 혹은 "fail" (string)
      - 성공 : 하트 색 바뀜
      - 실패 : 하트 색 그대로

  



 - '글쓰기' 버튼을 눌렀을 때

   - 요청 url : https://www.bokduck.com/community/write

   - 요청 방식 :  get

   - 응답 타입 : text/html

   - 디렉토리 : post/community/write.html


​         


- 글을 다 쓴 후 '게시' 버튼을 눌렀을 때
  - 요청 url : https://www.bokduck.com/community/write
  - 요청 방식 :  post
  - 요청 파라미터 
    - title : 글 제목
    - content : 글쓴 내용
    - tag : 태그
    - category : 카테고리
  - 응답 타입 : text/html
  - 디렉토리 : post/community/read.html

  

- 리스트에서 게시글을 클릭했을 때 - 상세리뷰로 들어감
  - 요청 url : https://www.bokduck.com/community/read
  - 요청 방식 :  get
  - 요청 파라미터 : 
    - communityId : 글 번호
  - 응답 타입 : text/html
  - 응답 구조 : post/community/read.html


​         

- 상세 페이지에서 '좋아요' 버튼을 눌렀을 때 - AJAX
  - 요청 url : https://www.bokduck.com/community/read/like
  - 요청 방식 :  post
  - 요청 파라미터 : 
  
    -  communityId : 글 번호
  - 응답 타입 :  application/json
  - 응답 구조 : 
    - 이름 - result : "success" 혹은 "fail" (string)
    - 성공 : 하트 색 바뀜
    - 실패 : 하트 색 그대로


​         

- '신고' 버튼 눌렀을 때 - AJAX
  - 요청 url :  https://www.bokduck.com/community/read/report
  - 요청 방식 :  post
  - 요청 파라미터 : communityId
  - 응답 타입 :  application/json
  - 응답 구조 :  
    - 이름 : result : "success" 혹은 "fail" (string)
    - 성공 : 신고 이미지 바뀌기
    - 실패 : 신고 이미지 그대로


​         

- 자신의 글에서 '수정' 버튼을 눌렀을 때 
  - 요청 url : https://www.bokduck.com/community/modify
  - 요청 방식 :  get
  - 요청 파라미터 : 
    - communityId : 수정할 글 번호 
  - 응답 타입 :  text/html
  - 디렉토리 : post/community/modify.html


​         

- 수정 완료 후 '게시' 버튼을 눌렀을 때
  - 요청 url : https://www.bokduck.com/community/modify
  - 요청 방식 :  POST
  - 요청 파라미터 
    - communityId : 수정할 글 번호
    - title, 제목
    - content, 내용 
    - tag, 태그
    - category 카테고리
  - 디렉토리 : text/html
  - 디렉토리 : post/community/read.html


​         

- 자신의 글에서 '삭제' 버튼을 눌렀을 때 -AJAX
  - 요청 url : https://www.bokduck.com/community/delete
  - 요청 방식 :  get
  - 요청 파라미터 : communityId
  - 응답 타입 : application / json
  - 디렉토리 : 
    - 이름 : result : "success" 혹은 "fail" (string)
    - 성공 : alert(“이 글을 삭제하시겠습니까?”) ‘예’ 누르면redirect:/post/community/list.html 아니요 - 그대로
    - 실패 : 삭제 왼됨 -> post/community/read.html


​       

- 댓글 달기 -AJAX

  - 요청 url : https://www.bokduck.com/community/read/comment

  - 요청 방식 : post

  - 요청 파라미터

    - communityId: 커뮤니티 번호 
    - content: 댓글 내용

  - 응답 타입 : application/json

  - 응답 구조 

    - 이름 - result : "success" 혹은 "fail" (string)

    - 로그인돼있을 때 : 댓글 올라감

    - 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/community/list.html
    
      

- 댓글 - 수정 AJAX

  - 요청 url : https://www.bokduck.com/community/read/comment/modify
  - 요청 방식 : post
  - 요청 파라미터

    - communityId: 커뮤니티 번호  
    - content: 댓글 내용
  - 응답 타입 : application/json
  - 응답 구조 : 
    - 이름 - result : "success" 혹은 "fail" (string)
    - 로그인돼있을 때 : 댓글 수정됨
    - 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/community/list.html


​         

- 댓글 - 삭제 AJAX

  - 요청 url : https://www.bokduck.com/community/read/comment/delete
  - 요청 방식 : POST
  - 요청 파라미터

    - communityId: 댓글 번호
  - 응답 타입 : application/json
  - 응답 구조 : 
    - 이름 - result : "success" 혹은 "fail" (string)
    - 로그인돼있을 때 :  alert("정말 삭제하겠습니까?") -> 예 :댓글 삭제 됨 아니요-> 그대로
    - 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/community/list.html


​           

 - '대댓글달기' 버튼을 눌렀을 때 - AJAX

      - 요청 url : https://www.bokduck.com/community/read/recomment
      - 요청 방식 :  post
      - 요청 파라미터 :

        -  commentId : 부모댓글 번호
      - 응답 타입 : application/json
      - 응답 구조 : 
        - 이름 - result : "success" 혹은 "fail" (string)
        - 로그인돼있을 때 : 텍스트창이 뜬다
        - 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/community/list.html


​           

- 대댓글 달기 실행 -AJAX

  - 요청 url : https://www.bokduck.com/community/read/recomment/active
  - 요청 방식 : post
  - 요청 파라미터

    - communityId: 커뮤니티 글 번호 
    - content: 댓글 내용
    - parentId : 부모 댓글 번호
  - 응답 타입 : application/json
  - 응답 구조 : 
    - 이름 - result : "success" 혹은 "fail" (string)
    - 로그인돼있을 때 : 대댓글 올라감
    - 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/community/list.html


​           

- 대댓글 - 수정 AJAX

  - 요청 url : https://www.bokduck.com/community/read/recomment/modify
  - 요청 방식 : post
  - 요청 파라미터

    - content: 수정된 댓글 내용
    - commentId : 댓글 번호
  - 응답 타입 : application/json
  - 응답 구조 : 
    - 이름 - result : "success" 혹은 "fail" (string)
    - 로그인돼있을 때 : 댓글 수정 됨
    - 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/community/list.html


​             

- 대댓글 - 삭제 AJAX

  - 요청 url : https://www.bokduck.com/community/read/recomment/delete
  - 요청 방식 : POST
  - 요청 파라미터

    - commentId : 댓글 번호
  - 응답 타입 : application/json
  - 응답 구조 : 
    - 이름 - result : "success" 혹은 "fail" (string)
    - 로그인돼있을 때 :  alert("정말 삭제하겠습니까?") -> 예 :댓글 삭제 됨 아니요-> 그대로
    - 세션이 만료되었을 때 : alert("로그인이 필요합니다.") 후 redirect:/post/community/list.html


​          




  ### 마이페이지 ("/mypage")

- 마이페이지 버튼 클릭 - 로그인한 회원만

  - 요청 url : https://bokduck.com/mypage

  - 요청 방식 : GET

  - 응답 타입 : text/html

  - 디렉토리 : member/mypage.html

    

- 회원정보 '변경' 버튼을 눌렀을 때

  - 요청 url : "https://www.bokduck.com/mypage"

  - 요청 방식 :  post

  - 요청 파라미터 

    - nickname : 아이디
    - tel : 전화번호
    - userAddress : 주소

  - 응답 타입 : text/html

  - 디렉토리 : /member/mypage.html

    


- 페이지를 넘겼을 때 - AJAX

  - 요청 url : "https://www.bokduck.com/mypage/page"
  - 요청 방식 : post

  - 요청 파라미터 

    - page : 현재 페이지 번호

    - boardName : 커뮤니티, 리뷰 탭

  - 응답 타입 : application/json

  - 응답 구조 : 내가 작성한 글 페이징


  ```
강사님 어드바이스

'리뷰' / '커뮤니티' 탭의 1페이지 게시글까지는 마이페이지 로딩에 포함시키고
페이지가 넘어갈 때 AJAX를 쓴다!

  ```

  

- '회원탈퇴' 버튼을 눌렀을 때 - AJAX
  - 요청 url : https://www.bokduck.com/quit
  - 요청 방식 :  post
  - 응답 타입 : application/json
  - 디렉토리 : 
    - 이름 - result : "success" 혹은 "fail" (string)
    - 성공 -  alert(“정말로 탈퇴하시겠습니까?”) ‘예’ 누르면 /로 리다이렉트
    - 실패 - 그대로 -> member/mypage.html




  ## 관리자페이지

  - 관리자 버튼 클릭 - 관리자는 마이페이지 대신 관리자페이지가 보임
    - 요청 url : https://bokduck.com/manage
    - 요청 방식 : GET
    - 응답 타입 : text/html
    - 디렉토리 : member/manage.html

 

  - 승인 버튼 클릭 시 - AJAX

    - 요청 url : https://www.bokduck.com/manage/list/approval

    - 요청방식 : POST

    - 요청 파라미터 : reviewId (리뷰 게시물 기본키)

    - 응답 타입 : application/json

    - 응답 구조

      - 이름 - result : "success" 혹은 "fail" (string)

      - 성공 : alert("승인 완료하였습니다.") -> post/review/list.html 에 승인 한 글 올라가고 관리자페이지 리스트에서 사라짐
      
      - 실패 : alert("거부 실패되었습니다.") -> 관리자 페이지 리스트에서 삭제 안됨
      
        
      
        

  - 거부 버튼 클릭시 - AJAX

    - 요청 url : https://www.bokduck.com/manage/list/refusal

    - 요청방식 : post

    - 요청 파라미터 : reviewId (리뷰 게시물 기본키)

    - 응답 타입 : application/json

    - 응답 구조

      - 이름 - result : "success" 혹은 "fail" (string)

      - 성공 : alert("거부 완료하였습니다.") -> post/review/list.html 에 글 안 올라감
      
      - 실패 : alert("거부 실패되었습니다.") -> 관리자 페이지 리스트에서 삭제 안됨
      
        

  - 다음 페이지로 넘겼을때  

    - 요청 url : https://www.bokduck.com/manage/list
    - 요청 방식 : GET
    - 요청 파라미터 :
      - pageNum (현재 페이지 번호) 
    - 응답 타입 : text/html
    - 디렉토리 : member/manage/list.html

  