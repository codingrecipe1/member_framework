## Spring Framework 회원 프로젝트 
- 프로젝트 세팅은 제 채널의 세팅 영상을 참고해주세요!

### 개발환경
- IntelliJ IDEA Community Edition  
- amazon corretto open jdk 11
- mysql 8
- mybatis
- JSP
- Tomcat 9

### 주요 기능
- 회원가입
- 로그인
- 회원목록 출력
- 상세조회
- 수정
- 삭제
- ajax 이메일 중복체크

### DB sql
```
-- 계정 생성하기
create database db_codingrecipe;
create user user_codingrecipe@localhost identified by '1234';
grant all privileges on db_codingrecipe.* to user_codingrecipe@localhost;

-- 회원 테이블
drop table if exists member_table;
create table member_table(
	id bigint primary key auto_increment,
    memberEmail varchar(20) unique,
    memberPassword varchar(20),
    memberName varchar(20),
    memberAge int,
    memberMobile varchar(30)
); 
```