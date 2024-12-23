# 게시판 API specification 정의

## 1. 게시판
### 생성
* POST
* Path 
  - /boards
* Example Endpoint
  - https://localhost:8080/boards
* Request Parameters
  - Body Parameters
    * boardName | String | 게시판 이름
    * boardUser | String | 게시판 생성자
    * boardUserPassword | String | 게시판 생성자 비밀번호
      
###  조회
* GET
* Path
  - /boards/{boardId}
* Example Endpoint
  - https://localhost:8080/boards/{boardId}
* Request Parameters
  - Path Segment Parameter
    * boardId | Number | 게시판 ID
* Response Message
  - message String
  - data
    * boardId | Number | 게시판 ID
    * boardName | String | 게시판 이름
      
### 수정
* PUT
* Path
  - /boards/{boardId}
* Example Endpoint
  - https://localhost:8080/boards/{boardId}
* Request Parameters
  - boardId | Number | 게시판 ID
  - Body Parameters
    - boardName | String | 게시판 이름

### 삭제
* DELETE
* Path
  - /boards/{boardId}
* -Example Endpoint
  - https://localhost:8080/boards/{boardId}
* Request Parameters
  - Path Segment Parameter
    * boardId | Number | 게시판 ID
* Response Message
  - message | String
  - data | String | 삭제된 게시판 ID

## 2. 게시글
### 생성
* POST
* Path
  - /posts
* Example Endpoint
  - https://localhost:8080/posts
* Request Parameters
  - Body Parameters
    - title | String | 게시글 제목
    - content | String | 게시글 내용
    - boardId | Number | 게시판 ID

### 조회
* GET
* Path
  - /posts/{postId}
* Example Endpoint
  - https://localhost:8080/posts/{postId}
* Request Parameters
  - Path Segment Parameter
    - postId | Number | 게시판 ID
    - Response | Message
    - message | String
* data
  - postId | Number | 게시글 ID
  - title | String | 게시글 제목
  - content | String | 게시글 내용
  - boardId | Number | 게시판 ID
### 수정
### 삭제
* DELETE
* Path
  - /posts/{postId}
* Example Endpoint
  - https://localhost:8080/posts/{postId}
* Request Parameters
  - Path Segment Parameter
    - postId Number 게시글 ID
* Response Message
  - message String
  - data String 삭제된 게시글 ID

## 3. 댓글
### 생성
  POST
  Path
  /comments
  Example Endpoint
  https://localhost:8080/comments
  Request Parameters
  Body Parameters
  content String 댓글 내용
  postId Number 게시글 ID
### 조회
  GET
  Path
  /comments/{commentsId}
  Example Endpoint
  https://localhost:8080/comments/{commentsId}
  Request Parameters
  Path Segment Parameter
  commentsId Number 댓글 ID
  Response Message
  message String
  data
  postId Number 게시글 ID
  content String 댓글 내용
### 수정
### 삭제
  DELETE
  Path
  /comments/{commentsId}
  Example Endpoint
  https://localhost:8080/comments/{commentsId}
  Request Parameters
  Path Segment Parameter
  commentsId Number 댓글 ID
  Response Message
  message String
  data String 삭제된 댓글 ID