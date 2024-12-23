GET : 조회
POST : 생성, 업데이트

API 명세
----------------------------
게시판 생성
-Path : Post "/boardName"
-BodyParams : 
Name            | Required  | Type      | Description
boardName       | O         | String    | 게시판명
boardPassword   | O         | String    | 게시판비밀번호

게시판 조회
-Path : Get "/boardName"
-BodyParams :
Name                | Required | Type      | Description
postUserName        | O        | String    | 게시글 작성자




게시판 수정
-Path : Put "/boardName"
-BodyParams :
Name                | Required | Type      | Description
postUserName        | O        | String    | 게시글 작성자
postUserPassword    | O        | String    | 게시글 삭제시 비밀번호


게시판 삭제
-Path : Delete "/boardName"
-BodyParams :
Name                | Required | Type      | Description
postUserName        | O        | String    | 게시글 작성자
postUserPassword    | O        | String    | 게시글 삭제시 비밀번호 

------------------------------------
게시글 생성
-Path : Post "/"
-BodyParams :
Name                | Required | Type      | Description
postUserName        | O        | String    | 게시글 작성자
postUserPassword    | O        | String    | 게시글 삭제시 비밀번호
postTitle           | O        | String    | 게시글 제목
postContents        | O        | String    | 게시글 내용
postViewCount       |          | String    | 게시글 조횟수

게시글 조회
-Path : Get "/"
-BodyParams :
Name                | Required | Type      | Description
postUserName        | O        | String    | 게시글 작성자
postTitle           | O        | String    | 게시글 제목
postContents        | O        | String    | 게시글 내용

게시글 수정
-Path : Put "/"
-BodyParams :
Name                | Required | Type      | Description
postUserPassword    | O        | String    | 게시글 삭제시 비밀번호
postTitle           | O        | String    | 게시글 제목
postContents        | O        | String    | 게시글 내용

게시글 삭제
-Path : Delete "/"
-BodyParams :
Name                | Required | Type      | Description
postUserName        | O        | String    | 게시글 작성자
postUserPassword    | O        | String    | 게시글 삭제시 비밀번호
postTitle           | O        | String    | 게시글 제목

------------------------------------
댓글 생성
