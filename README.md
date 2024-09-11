# Solo Page Making Project 02
(JDBC -> Mybatis)

## 프로젝트 개요
이 프로젝트는 **JSP**와 **MyBatis**를 기반으로 한 웹 애플리케이션으로, 간단한 **회원 관리** 및 **게시판 기능**을 구현하고 있습니다. **Java의 MVC 패턴**을 적용하였으며, 데이터 관리를 위한 **Oracle 데이터베이스**와 연동하여 실무 환경에 가까운 설계를 목표로 하였습니다.

이 프로젝트는 **단독 프로젝트**로 진행되었으며, 웹 애플리케이션의 전반적인 흐름을 이해하고, 백엔드 및 프론트엔드 개발 기술을 습득하는 데 중점을 두었습니다. 이를 통해 기본적인 웹 개발 기술과 데이터베이스 연동을 학습하는 것이 목적입니다.

## 사용된 기술 스택

- **프로그래밍 언어**: Java, JSP
- **프레임워크**: MyBatis (JDBC의 대안으로 사용)
- **데이터베이스**: Oracle
- **뷰 템플릿**: JSP
- **프론트엔드**: HTML, CSS, JavaScript
- **버전 관리**: Git
- **배포 환경**: 로컬 환경 (향후 클라우드 환경 적용 계획)
- **추후 적용**: Spring, Spring Boot, Cloud 배포, JPA 등...

### 기술 선택 이유
1. **MyBatis**: 효율적인 SQL 작성과 데이터베이스 연동을 지원하는 ORM 도구로, 복잡한 SQL을 직접 다루면서도 객체 매핑의 장점을 누릴 수 있어 선택하였습니다. 실무 환경에서 많이 사용되며, SQL 최적화와 데이터 관리의 유연성을 확보할 수 있습니다.
2. **Oracle Database**: 대규모 데이터 처리를 위한 강력한 성능을 제공하며, SQL 최적화 및 데이터베이스 설계에 대한 심화 학습을 위해 선택하였습니다.
3. **JSP**: 웹 페이지의 동적인 내용을 처리하기 위한 템플릿 엔진으로 사용하였으며, MVC 패턴에서 View를 구현하는 데 적합한 기술로 채택하였습니다.

## 주요 기능

1. **회원 관리 시스템**
   - **회원 가입**, **로그인**, **로그아웃**, **회원 정보 수정 및 삭제** 기능을 제공합니다.
   - 각 기능은 데이터베이스와 연동되어 회원 데이터를 관리하며, 향후 비밀번호 암호화 및 보안 기능을 추가할 계획입니다.

2. **게시판 기능**
   - 사용자들은 게시글을 **작성**, **수정**, **삭제**할 수 있습니다.
   - 게시판 목록에서 게시글을 확인할 수 있으며, **페이지네이션** 기능을 통해 여러 페이지에 걸친 게시글 목록을 관리할 수 있습니다.

3. **클라우드 배포 (향후 적용 예정)**
   - 추후 네이버 클라우드 플랫폼(NCP)을 활용하여 클라우드 배포를 계획하고 있습니다.

## 프로젝트 구조

- **Controller**: 사용자의 요청을 처리하고, 비즈니스 로직을 수행한 후 결과를 JSP로 전달하는 역할을 합니다.
- **Model (Bean)**: 데이터를 담고 있는 객체로, 회원과 게시글의 데이터를 관리합니다.
- **DAO (Data Access Object)**: 데이터베이스와 직접적으로 연결하여 데이터를 조회, 삽입, 삭제, 수정하는 역할을 담당합니다.
- **View (JSP)**: 사용자가 볼 수 있는 웹 페이지를 생성하며, 데이터를 동적으로 처리하여 클라이언트에게 전달합니다.

### MVC 패턴에 따른 역할
- **Model**: `bean` 클래스를 사용하여 게시글 및 회원 데이터를 관리합니다.
- **View**: `JSP` 파일을 통해 사용자에게 데이터를 시각적으로 보여줍니다.
- **Controller**: 각종 사용자 요청을 받아 비즈니스 로직을 처리하고 결과를 반환합니다.

## 문제 해결 및 학습 내용

1. **SQL 최적화**:
   - 쿼리 실행 성능을 높이기 위해 인덱스를 추가하고, 쿼리 성능을 최적화하였습니다. 이를 통해 데이터베이스와의 효율적인 연동을 학습하였습니다.

2. **페이지네이션 오류 해결**:
   - 게시판 페이지네이션에서 발생한 오류를 발견하고, 로직을 수정하여 다중 페이지에서의 원활한 탐색을 가능하게 하였습니다.

## 배운 점 및 향후 개선 사항

- **MyBatis와 JDBC의 차이점**을 학습하고, 데이터베이스 연동에서 더 효율적인 방법을 이해할 수 있었습니다.
- 향후 **보안 강화**를 위해 Spring Security를 적용할 예정이며, **JWT**를 활용한 인증 방식 도입도 고려하고 있습니다.

## 설치 및 실행 방법

1. **프로젝트 클론**
    ```bash
    git clone <프로젝트 주소>
    ```
2. **Oracle 데이터베이스 설정**
    - `src/main/resources/sql` 폴더 내의 SQL 파일을 사용하여 데이터베이스 테이블을 생성합니다.
3. **서버 실행**
    - Tomcat 서버를 사용하여 애플리케이션을 실행합니다.
4. **웹 브라우저에서 접속**
    - 브라우저에서 `http://localhost:8080`으로 접속하여 애플리케이션을 확인할 수 있습니다.

## 기여 방법

1. **이슈 등록** 및 **버그 제안**.
2. **새로운 기능 추가** 시 Pull Request 제출.


DOM TREE
```
└── projectMyBatis/
    ├── .classpath
    ├── .project
    ├── .settings/
    │   ├── .jsdtscope
    │   ├── org.eclipse.core.resources.prefs
    │   ├── org.eclipse.jdt.core.prefs
    │   ├── org.eclipse.wst.common.component
    │   ├── org.eclipse.wst.common.project.facet.core.xml
    │   ├── org.eclipse.wst.jsdt.ui.superType.container
    │   ├── org.eclipse.wst.jsdt.ui.superType.name
    ├── build/
    │   └── classes/
    │       └── board/
    │           ├── bean/
    │           │   ├── BoardDTO.class
    │           └── dao/
    │               ├── BoardDAO.class
    │               ├── CommentDAO.class
    │       └── member/
    │           ├── bean/
    │           │   ├── MemberDTO.class
    │           └── dao/
    │               ├── MemberDAO.class
    ├── src/
    │   └── main/
    │       └── java/
    │           └── board/
    │               ├── bean/
    │               │   ├── BoardDTO.java
    │               └── dao/
    │                   ├── BoardDAO.java
    │                   ├── CommentDAO.java
    │           └── member/
    │               ├── bean/
    │               │   ├── MemberDTO.java
    │               └── dao/
    │                   ├── MemberDAO.java
    │       └── SQL/
    │           ├── board.sql
    │           ├── member.sql
    │       └── webapp/
    │           ├── index.jsp
    │           ├── mainpage.html
    │           └── board/
    │               ├── addComment.jsp
    │               ├── boardList.jsp
    │               ├── boardView.jsp
    │               ├── boardWrite.jsp
    │               ├── boardWriteForm.jsp
    │           └── css/
    │               ├── boardList.css
    │               ├── boardView.css
    │               ├── boardWrite.css
    │               ├── indexcss.css
    │               ├── logincss.css
    │               ├── mainpage.css
    │               ├── memberWritecss.css
    │               ├── updatecss.css
    │           └── image/
    │               ├── back.png
    │               ├── home.png
    │               ├── home2.png
    │               ├── loader.gif
    │           └── js/
    │               ├── member.js
    │               ├── script.js
    │           └── jsp/
    │               ├── nav.jsp
    │           └── member/
    │               ├── checkId.jsp
    │               ├── loginFail.jsp
    │               ├── loginOk.jsp
    │               ├── memberLogin.jsp
    │               ├── memberLoginForm.jsp
    │               ├── memberLogout.jsp
    │               ├── memberUpdate.jsp
    │               ├── memberUpdateForm.jsp
    │               ├── memberWrite.jsp
    │               ├── memberWriteForm.jsp
    ├── META-INF/
    │   ├── context.xml
    │   ├── MANIFEST.MF
    └── WEB-INF/
        ├── web.xml
        └── lib/
            ├── lombok.jar
            ├── mybatis-3.5.16.jar
            ├── ojdbc11.jar


```

-------------------------------
# Solo Page Making Project 01

## 프로젝트 개요
이 프로젝트는 **JSP**와 **Spring Framework**를 기반으로 한 웹 애플리케이션으로, 간단한 회원 관리 및 게시판 기능을 포함하고 있습니다. **Java의 MVC 패턴**을 따르며, 데이터 관리를 위한 **Oracle 데이터베이스**와의 연동을 통해 실무 환경에 가까운 설계를 목표로 하였습니다.

이 프로젝트는 저의 단독 프로젝트로서, **웹 애플리케이션의 기본적인 흐름**을 이해하고, **백엔드 및 프론트엔드 개발 기술**을 습득하기 위해 진행하였습니다.

## 사용된 기술 스택

- **프로그래밍 언어**: Java, JSP
- **프레임워크**: Spring Framework
- **데이터베이스**: Oracle
- **뷰 템플릿**: JSP
- **ORM**: MyBatis (향후 적용 예정)
- **프론트엔드**: HTML, CSS, JavaScript
- **버전 관리**: Git
- **배포 환경**: 네이버 클라우드 (향후 적용 예정)

### 기술 선택 이유
1. **Spring Framework**: 대규모 애플리케이션 개발에 적합하며, 확장성이 뛰어난 프레임워크로 실무에서 많이 사용되기 때문에 선택하였습니다.
2. **Oracle Database**: 대규모 데이터 처리가 필요한 시스템에서 자주 사용되므로 선택하였고, 데이터베이스 설계 및 SQL 최적화에 대한 이해를 높이기 위한 목적이 있습니다.
3. **MyBatis**: ORM 도구로 데이터베이스와의 효율적인 연동을 목표로 하였으나, 아직 적용되지 않은 상태입니다. 향후 확장을 고려하여 설계를 진행하였습니다.

## 주요 기능

1. **회원 관리 시스템**
    - **회원 가입**, **로그인**, **로그아웃**, **회원 정보 수정 및 삭제** 기능 제공.
    - 비밀번호 암호화 등 보안 요소는 미적용 상태이지만, 향후 이를 개선할 예정입니다.
  
2. **게시판 기능**
    - 사용자는 게시글을 **작성**, **수정**, **삭제**할 수 있으며, 게시판 목록에서 게시글을 확인할 수 있습니다.
    - **페이지네이션** 기능을 구현하여 여러 페이지에 걸쳐 게시글을 관리할 수 있습니다.

3. **클라우드 배포 (미적용)**
    - 클라우드 배포는 향후 네이버 클라우드 플랫폼(NCP)을 통해 실습할 예정이며, 이 부분은 아직 적용되지 않았습니다.

## 프로젝트 구조

- **Controller**: 사용자의 요청을 처리하고, 해당 요청을 처리한 후 결과를 돌려주는 역할.
- **Model (Bean)**: 데이터를 담고 있는 객체로, 비즈니스 로직을 수행.
- **DAO (Data Access Object)**: 데이터베이스에 접근하여 데이터를 가져오고, 삽입, 삭제, 업데이트하는 역할.
- **View (JSP)**: 클라이언트가 볼 수 있는 웹 페이지를 생성.

### MVC 패턴에 따른 역할
- **Model**: `bean` 클래스를 통해 게시글 및 회원 데이터를 관리.
- **View**: `JSP` 페이지를 통해 사용자에게 데이터를 시각적으로 제공.
- **Controller**: 각종 사용자 요청을 처리하여, 비즈니스 로직을 수행하고 결과를 반환.

### 폴더 구조


- **src/main/java**
  - **board**: 게시판 기능을 담당하는 로직이 위치.
    - **bean**: 게시글 데이터를 관리하는 모델 클래스.
    - **dao**: 게시글 관련 데이터베이스 액세스를 관리하는 클래스.
  - **member**: 회원 관리 기능을 담당하는 로직이 위치.
    - **bean**: 회원 데이터를 관리하는 모델 클래스.
    - **dao**: 회원 관련 데이터베이스 액세스를 담당하는 클래스.
- **src/main/webapp**: JSP 파일과 정적 자원(CSS, JavaScript 등)을 포함하는 웹 애플리케이션의 프론트엔드 구성.

## 문제 해결 및 학습 내용

1. **SQL 최적화**:
    - 쿼리 실행 시간이 오래 걸리는 문제를 해결하기 위해 **인덱스**를 추가하고, **JOIN 연산**을 최적화하였습니다.
    - 이를 통해 데이터베이스의 성능을 개선하는 방법을 학습하였습니다.

2. **NullPointerException 처리**:
    - 초기 개발 과정에서 **NullPointerException**이 발생하였으며, 이를 **예외 처리**와 **방어적 코딩 기법**을 통해 해결하였습니다. 해당 문제 해결을 통해 Java 예외 처리에 대한 이해를 높였습니다.

3. **페이지네이션 오류 해결**:
    - 게시판의 페이지 네비게이션이 올바르게 작동하지 않는 문제를 발견하고, 로직을 수정하여 다중 페이지에서의 원활한 탐색을 가능하게 하였습니다.

## 배운 점 및 향후 개선 사항

- **웹 애플리케이션 설계와 데이터 흐름**에 대한 깊은 이해를 얻었으며, **MVC 패턴**의 역할을 명확하게 학습할 수 있었습니다.
- 향후 **클라우드 배포**와 **MyBatis ORM 적용**을 통해 실무에서 활용되는 기술 스택을 더 많이 경험할 예정입니다.
- 보안 강화를 위해 **JWT**나 **Spring Security**와 같은 기술을 적용하는 것을 목표로 하고 있습니다.

## 설치 및 실행 방법

### 1. 프로젝트 클론
```bash
git clone https://github.com/KimSeongChan97/SoloPageMakingProject01.git
```

## 설치 및 실행 방법

1. **프로젝트 클론**
    ```bash
    git clone https://github.com/KimSeongChan97/SoloPageMakingProject01.git
    ```
2. **Oracle 데이터베이스 설정**
    - `src/main/resources/sql` 폴더의 SQL 파일을 사용하여 데이터베이스 테이블을 생성합니다.
3. **서버 실행**
    - `Spring Boot` 또는 `Tomcat` 서버를 사용하여 애플리케이션을 실행합니다.
4. **웹 브라우저에서 접속**
    - 브라우저에서 `http://localhost:8080`으로 접속하여 애플리케이션을 확인할 수 있습니다.

## 기여 방법

1. 이슈 등록 및 버그 제안.
2. 새로운 기능 추가 시 Pull Request 제출.

## Dom Tree
```
└── projectJSP/
    ├── .classpath
    ├── .project
    ├── .settings/
    │   ├── .jsdtscope
    │   ├── org.eclipse.core.resources.prefs
    │   ├── org.eclipse.jdt.core.prefs
    │   ├── org.eclipse.wst.common.component
    │   ├── org.eclipse.wst.common.project.facet.core.xml
    │   ├── org.eclipse.wst.jsdt.ui.superType.container
    │   ├── org.eclipse.wst.jsdt.ui.superType.name
    ├── build/
    │   └── classes/
    │       └── board/
    │           ├── bean/
    │           │   ├── BoardDTO.class
    │           └── dao/
    │               ├── BoardDAO.class
    │               ├── CommentDAO.class
    │       └── member/
    │           ├── bean/
    │           │   ├── MemberDTO.class
    │           └── dao/
    │               ├── MemberDAO.class
    ├── src/
    │   └── main/
    │       └── java/
    │           └── board/
    │               ├── bean/
    │               │   ├── BoardDTO.java
    │               └── dao/
    │                   ├── BoardDAO.java
    │                   ├── CommentDAO.java
    │           └── member/
    │               ├── bean/
    │               │   ├── MemberDTO.java
    │               └── dao/
    │                   ├── MemberDAO.java
    │       └── SQL/
    │           ├── board.sql
    │           ├── member.sql
    │       └── webapp/
    │           ├── index.jsp
    │           ├── mainpage.html
    │           └── board/
    │               ├── addComment.jsp
    │               ├── boardList.jsp
    │               ├── boardView.jsp
    │               ├── boardWrite.jsp
    │               ├── boardWriteForm.jsp
    │           └── css/
    │               ├── boardList.css
    │               ├── boardView.css
    │               ├── boardWrite.css
    │               ├── indexcss.css
    │               ├── logincss.css
    │               ├── mainpage.css
    │               ├── memberWritecss.css
    │               ├── updatecss.css
    │           └── image/
    │               ├── back.png
    │               ├── home.png
    │               ├── home2.png
    │               ├── loader.gif
    │           └── js/
    │               ├── member.js
    │               ├── script.js
    │           └── jsp/
    │               ├── nav.jsp
    │           └── member/
    │               ├── checkId.jsp
    │               ├── loginFail.jsp
    │               ├── loginOk.jsp
    │               ├── memberLogin.jsp
    │               ├── memberLoginForm.jsp
    │               ├── memberLogout.jsp
    │               ├── memberUpdate.jsp
    │               ├── memberUpdateForm.jsp
    │               ├── memberWrite.jsp
    │               ├── memberWriteForm.jsp
    ├── META-INF/
    │   ├── context.xml
    │   ├── MANIFEST.MF
    └── WEB-INF/
        ├── web.xml
        └── lib/
            ├── lombok.jar
            ├── ojdbc11.jar

```
