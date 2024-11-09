# 도서 관리 시스템 - Locallibrary

## Skills
<img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" />&nbsp; <!--django-->

## 프로젝트 목표
1. **도서 관리 시스템 구축**: 도서 목록 조회, 상세 정보와 대출 상태 확인 기능을 제공하여 도서관의 효율적인 관리와 접근성 향상
2. **REST API 제공**: 도서 정보와 대출 데이터를 REST API로 제공하여 외부 시스템 또는 프론트엔드와 연동 가능한 구조 구축
3. **권한 기반 접근 제어**: 관리자와 일반 사용자 권한을 구분하여 특정 기능에 대한 접근을 제한하고 보안을 강화
4. **심플하고 직관적인 UI 제공**: CSS 스타일링을 적용하여 사용자에게 깔끔한 인터페이스 제공

## 사용한 데이터 셋
- 도서 및 저자 데이터베이스

## 워크플로우
1. **프로젝트 설정**: Django 프로젝트 및 앱 생성, MySQL 데이터베이스 연결
2. **모델 구축**: `Book`, `Author`, `BookInstance`, `Genre` 모델 설계
3. **기능 개발**
   - 도서/저자 목록 페이지, 상세 페이지 구현
   - 대출 관리 페이지 및 연장 기능 추가
   - 검색 및 필터링 기능
   - REST API 엔드포인트 구축
4. **UI 개발**: CSS 스타일링으로 직관적 UI 제공
5. **권한 설정**: 일반 사용자와 관리자 권한 구분

## 프로젝트 결과 (구현한 기능)
1. **도서 및 저자 정보 관리**
   - 도서 목록 및 상세 정보 페이지 구현
   - 저자 목록 및 상세 정보 페이지 구현
2. **도서 대출 및 상태 관리**
   - `BookInstance` 모델을 활용한 대출 상태 관리 및 대출 목록 페이지 구현
3. **검색 및 필터링 기능**
   - 키워드 검색 기능을 통해 도서 필터링
4. **사용자 인증 및 권한 관리**
   - 로그인 및 로그아웃 기능, 관리자 권한 설정
5. **REST API 제공**
   - 도서 목록 및 인스턴스 정보 JSON 제공
6. **UI 및 CSS 스타일링**
   - 사이드바 및 버튼 스타일링으로 직관적 UI 제공

## 문제 해결
1. **문제**: 초기 데이터베이스 연결 시 'OperationalError: (2002, "Can't connect to MySQL server on 'localhost'")' 오류 발생
   - **해결 방법**: `settings.py`에서 DATABASE 설정을 확인하고, MySQL 서버가 실행 중인지 확인. 이후 올바른 호스트와 포트 번호 입력하여 해결

2. **문제**: API 호출 시 'AttributeError: module 'rest_framework' has no attribute 'APIView'' 오류 발생
   - **해결 방법**: `djangorestframework` 라이브러리 설치를 확인하고, 최신 버전으로 업데이트한 뒤 문제 해결

3. **문제**: 페이지네이션 시 'Page not found (404)' 오류가 발생
   - **해결 방법**: `ListView`에서 `paginate_by` 설정 확인 후 URL 패턴에 페이지 번호를 포함하여 페이지네이션 문제 해결

## 프로젝트를 통해 얻은 역량
- **Django 웹 개발 역량**: Django 모델링, 뷰, URL 매핑, 템플릿 엔진 활용
- **REST API 설계 능력**: RESTful 엔드포인트 구현
- **웹 크롤링/파싱 역량**: BeautifulSoup, Requests 등을 통해 웹 페이지의 데이터 크롤링
- **데이터베이스 관리 역량**: MySQL 데이터베이스 설정, 쿼리 작성, 데이터 관리
- **UI 및 UX 개선 역량**: 기본 CSS 스타일링을 통한 사용자 경험 향상
