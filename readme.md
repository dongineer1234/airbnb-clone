####################################################################################################

#0.0 Introduction

# Django
: 웹 어플리케이션(파이썬)을 만들기 위해 사용되는 유명한 프레임워크

# tailwindCSS
: 이 과정의 디자인 utility-first CSS 프레임워크

# utility-first CSS
: 이미 만들어져 있는 CSS를 활용

####################################################################################################

#0.1 Theory Requirements

# 필요한 기술
: html, css, javascript약간, python

# html, css
: class, id, flex

# python
: function, class, inheritance(상속)

# Django, python의 공통점
: Object Oriented(객체지향) 방식을 따름
class, inheritance(상속)를 잘 이해하는 게 중요

# Django
: 웹 어플리케이션(파이썬)을 만들기 위해 사용되는 유명한 프레임워크
모든게 class, inheritance로 돌아감 

####################################################################################################

#0.2 Software Requirements part One

# code editor
: VSC

# PyCharm
: IDE(Integrated Development Environment)
오로지 python을 위한 editor
VSC에서도 기능을 제공 하긴 하지만 PyCharm에서 제공하는 기능이 더 많음
2개의 version이 있는데 free version에서는 Django에 대한 충분한 지원이 없음
Django와 html, js에 대한 지원을 바란다면 Professional version을 받아야 함

####################################################################################################

#0.3 Software Requirements part Two

# python
: function, class, inheritance(상속)
3 version install, cmd에서 python
install 중 add path 반드시 체크

####################################################################################################

#0.4 Django vs. Flask

# python 프레임워크 중 Django를 택 한 이유
: 다른 python 프레임워크인 Flask, Pyramid
이 둘을 사용하면 아주 짧은 시간에 뭔가 만들어낼 수 는 있지만
되게 작고 가벼워서 많은 기능을 제공하진 않음
마이크로 프레임워크인 Flask는 직접 해야될 일들이 많음 
하지만 Django는 그런 부분들을 이미 처리하고 있음

# Django
: 웹 어플리케이션(파이썬)을 만들기 위해 사용되는 유명한 프레임워크
모든게 class, inheritance로 돌아감
Django는 거대한 프레임워크로 사용 예로는 사용자 인증을 처리해주고
컨텐츠 관리 기능이 있음 관리자 페이지, 사용자 인증이 Django를 사용하는 가장 큰 이유
이미 만들어진 form들이 있어서 필요한 기능(패스워드 바꾸기, 프로필 바꾸기)이 있으면 
갖다 쓰면 됨 이메일 백엔드도 있어서 이메일 인증도 해줄 수 있음 보안기능도 있음
아주 빠르고 신속하고 커스터마이징도 쉬움
airbnb에는 로그인, 로그아웃, 관리자 패널, 뭔가 업로드하고 삭제하는 기능이 필요하기,
비밀번호 변경하기, 본인확인 이메일 등 기능이 필요 하기 때문에 Django가 적합

####################################################################################################

#0.5 Django vs. React

# Django를 사용하는 사이트
: 파이어폭스, 인스타그램, 핀터레스트, 네셔널지오그래픽

# Django 템플릿 시스템
: 인스타그램, 핀터레스트는 Django 템플릿 시스템을 쓰지 않음
그 이유는 그들의 서비스는 규모가 아주 거대해졌고 좀 더 다이나믹한 걸 원하고 있음
그들은 백엔드에서만 API 서버로서 Django를 사용하고 있음

# React
: 활발한 상호작용이 강력한 기능 
이 과정에서 딱히 React의 강력한 기능들이 필요하지 않음
인스타그램의 프론트엔드는 100% React를 바탕 하지만 API는 Django사용

####################################################################################################

#1.0 The Pacakge Installer for Python

# Pipenv
: Python에는 공식 npm(패키지 관리자)이 없음
우리는 global보다 오직 해당 프로젝트에만 설치하고 싶음
하지만 pip는 무조건 global로 설치를 해버림 좋지 않음

####################################################################################################

#1.1 Meet Pipenv

# Pipenv
: 윈도우는 이 세계에서 일등 시민

####################################################################################################

#1.2 Creating our Env and Installing Django

# python3 환경설정
: pipenv --three

# Pipfile
: npm의 package.json이랑 같은 것 

# pipenv shell
: 우리는 현재 버블의 바깥이고 
pipenv --three를 해서 버블을 만들어 놓은 상태
pipenv shell을 해서 버블 안으로 들어감

# Django install
: pipenv install Django==최신version

# 정리
: 
1. 프로젝트를 위한 폴더생성
2. pipenv --three 명령어 실행
3. pipenv shell을 입력해서 버블(개발환경)안으로 들어감
4. pipenv install Django==최신version 설치

####################################################################################################

#1.3 Creating the Github Repository

# .gitignore
: 보안과 관련되어 있어서 공개 되면 안되는 정보,
굳이 올릴 필요가 없는 파일들
python project에서 일반적으로 github에 올리지 않는 파일들
을 적어줌

# # Mac .DS_Store
: Mac일 경우 .gitignore에 추가

####################################################################################################

#1.4 Testing the Bubble

# pipenv shell
: 우리는 현재 버블의 바깥이고 
pipenv --three를 해서 버블을 만들어 놓은 상태
pipenv shell을 해서 버블 안으로 들어감
어떤 콘솔을 쓰든 간에 pipenv shell부터 먼저 실행해서
버블 안으로 들어가야 함

####################################################################################################

#2.0 Creating a Django Project

# create project
: Django-admin startproject project
이렇게 하는건 전문가아님

# 전문가의 create project
: main directory에 진입해서
Django-admin startproject config를 실행
그리고 바깥 config를 Aconfig로 바꿈
그 이유는 안에 있는 이 config directory와 manage.py 파일을
밖으로 꺼낼 것이기 때문 동일 directory명이면 꺼내지지 않으니까
그리고 Aconfig를 삭제

# Extention에서 python install
: '내 폴더 이름':pipenv 설정되게 해야함

####################################################################################################

#2.1 Setting up VSCode and Python Like a PRO

# python
: function, class, inheritance(상속)
3 version install, cmd에서 python
install 중 add path 반드시 체크
compile language가 아닌 runtime language이기 때문에
프로그램이 시작되었는데 에러가 있으면 안됨
그래서 에러가 생길 부분을 미리 감지하려고 하는게 Linter
flake8은 Linter

# python pep
: 어떻게 python 코딩을 하면 좋을지 가이드라인

# flake8 install
: pipenv install flake8
flake8 + black 최고의 조합

# prettier
: pipenv install black --dev --pre

# settings.json
: 
{
  "python.pythonPath": "C:\\Users\\dongenius\\.virtualenvs\\airbnb-clone-LS0h6v51\\Scripts\\python.exe",
  "python.linting.flake8Enabled": true,
  "python.linting.pylintEnabled": false,
  "python.linting.enabled": true,
  "python.formatting.provider": "black",
  "python.linting.flake8Args": ["--max-line-length=88"]
}

####################################################################################################

#2.2 Falling in love with Django part One

# __init__.py
: Django 관련된 파일이 아니라, 파이썬에 필요한 파일
새로운 폴더를 만들 때, Python에서 그 폴더의 파일들을 써야 할 때는 항상
그 안에 이 파일을 둬야함 일종의 import를 하는 것
이 파일이 있어야 (manage.py에서 보듯이) "config.settings"를 쓸 수 있음

# settings.py
: 이미 우리가 애플리케이션을 만드는 데 필요한 모든 게 담겨있음 TIME_ZONE을 우리 시간대인 "Asia/Seoul"로 수정


####################################################################################################

#2.3 Falling in love with Django part Two

# pipenv shell
: 우리는 현재 버블의 바깥이고 
pipenv --three를 해서 버블을 만들어 놓은 상태
pipenv shell을 해서 버블 안으로 들어감
어떤 콘솔을 쓰든 간에 pipenv shell부터 먼저 실행해서
버블 안으로 들어가야 함

# python manage.py migrate

# python manage.py runserver
: 웹사이트 만듦, 서버구동
http://127.0.0.1:8000/admin (관리자 패널 로그인)

# python manage.py createsuperuser
: 관리자 계정 생성

# db.sqlite3
: 우리의 데이터베이스

####################################################################################################

#2.4 Django Migrations

# db.sqlite3 삭제
: runserver의 빨간색으로 표시되는 메시지를 다시 보고 싶기 때문
삭제했을 때 출력되는 메시지는 해당 migrations를 적용하지 않으면 우리의 프로젝트가 정상적으로 작동하지 않을 거라는 메시지

# db.sqlite3
: 데이터베이스 파일이며  초기상태는 비어있는 상태
우리의 프로젝트에 대해 아무것도 모르는 상태 좋지 않음
Django 코드를 사용해서 admin, auth, contenttypes, sessions 그밖에 다양한 것들을 저장할 것 sqlite3는 많은 사람들이 테스트, 소규모 프로젝트를 할 때 자주 사용되는 데이터베이스
데이터베이스는 하나의 상태에서 다른 상태로 다른 데이터 유형으로 바꾸는 것 데이터의 유형이 변경될 때마다 migrate가 필요
Django는 이미 17개의 migrations를 생성

# python manage.py makemigrations
: 입력하면 Django는 데이터 models를 확인하고 migration파일을 생성
No changes detected라고 뜨는데 그건 변경된 데이터가 없기 때문
하지만 우리는 이미 migrations를 적용한 것

# Django 엔진의 동작 방식
: 일부 데이터 유형을 변경하고 Django를 사용해서 migrations하는 것
그 다음 Django를 사용해서 데이터베이스를 업데이트 하는 것
따라서 먼저 migration을 생성하고 나서 migrate
그러므로 SQL을 배울 필요가 없음
데이터유형이 바뀌면 migration을 생성하고 해당 migraion을 적용하는 것
그리고 데이터베이스를 업데이트 그렇게 되면 데이터베이스와 Django를 동기화할 수 있는 것
Django에는 user system, authentication, administration, sessions 등이
포함되어 있음 그래서 당연히 migrations를 적용해야 되는 것
그리고 Django와 동일한 데이터 유형을 동기화 하기 위해 데이터베이스를 업데이트 하는것

# python manage.py migrate
: db.sqlite3에 정보가 쌓임
데이터유형을 데이터베이스에게 알려주는 정보
데이터베이스는 Django가 결과적으로 ID, password, last_login이 포함된
인증된 사용자의 정보를 저장하게 될 것이라는 것을 알게 되는 것
이것이 migration! models를 작성하게 되면 변수들을 수정해야 하기 때문에
migration에 대해 다룰 예정 예를들어 user는 단순히 first_name과 last_name만 갖고 있음 하지만 gender도 추가 될 수도 있음
gender를 추가하게 되면 우리는 migration을 생성하고 migrate를 수행하게 될 것임

####################################################################################################

#2.5 Django Applications

# Django
: 웹 어플리케이션(파이썬)을 만들기 위해 사용되는 유명한 프레임워크
모든게 class, inheritance로 돌아감
Django는 거대한 프레임워크로 사용 예로는 사용자 인증을 처리해주고
컨텐츠 관리 기능이 있음 관리자 페이지, 사용자 인증이 Django를 사용하는 가장 큰 이유
이미 만들어진 form들이 있어서 필요한 기능(패스워드 바꾸기, 프로필 바꾸기)이 있으면 
갖다 쓰면 됨 이메일 백엔드도 있어서 이메일 인증도 해줄 수 있음 보안기능도 있음
아주 빠르고 신속하고 커스터마이징도 쉬움
airbnb에는 로그인, 로그아웃, 관리자 패널, 뭔가 업로드하고 삭제하는 기능이 필요하기,
비밀번호 변경하기, 본인확인 이메일 등 기능이 필요 하기 때문에 Django가 적합

우리가 만든 Django 프로젝트는 여러 application을 포함
function의 집합임 Django는 무언가를 시작하기 전에 project를 계획하게끔
만듦 function의 집합이란 개념이 중요 

room application에 있는 함수로는 room 생성, 검색, 삭제, 수정, page 보여주기, 모든 room 보여주기, 업로드하기 이런개념

하단에 있는 review application에 있는 함수로는 review 생성, 삭제, 수정, 보기, 나열 예약 application 예약생성, 예약삭제, 예약승인, 예약취소, 예약리스트를 호스트가 확인, 유저 예약 리스트 확인

user application에 있는 함수로는 로그인, 로그아웃, 페이스북으로 로그인, 구글로 로그인, 메세지 주고 받기, 삭제, 수정, 팔로우하기, 언팔하기, 팔로우 리스트보기, 마음에 든 room으로 리스트 만들기

이 모든걸 한 폴더에 집어넣는건 안됨

Divide and Conquer(분리하여 지배) 방식을 사용할 것임

list application은 오직 list만 생성, 수정, 삭제, 공유

reservation application도 예약 생성하기, 수정, 삭제, 예약점수

Django를 효과적으로 사용하기 위해서는 Divide and Conquer를
바탕으로 계호기을 하고 시작해야함

이 모든 application들을 config에 통합하여 아름다운 Django 웹사이트를 만들 수 있음 Django 프로젝트는 여러 작은 application의 집합체라 보면 됨 Django를 효과적으로 사용하기 위해서는 언제 application을 만들고 또 만들지 않아야 하는지 구분할 수 있어야함 쉽게 설명해서 한 문장으로 application을 표현할 수 있어야함 문장에 and가 들어가면 안됨 그러면 그건 별개의 application이 돼야함

예를 들어 room application에 있는 함수로는 room 생성, 검색, 삭제, 수정, page 보여주기, 모든 room 보여주기, 업로드하기, 그리고(and) 리뷰 기능이 있다는 잘못된 것! 강조하지만 항상 작게 나누기

####################################################################################################

#2.6 Creating the Apps!

# Django-admin startapp
: 무조건 config 밖에서 만들어야 하고
Application을 만들때는 반드시 복수로
messages를 생성안한 이유는 messages가 이미 Django안에 있기 때문

# Django안에 Users application이 이미 존재 그런데 왜 user application을 만들었을까?
: Django Users는 매우 좋음 근데 문제는 이 페이지가 Django Admin에 있다는 것 그리고 전체 서버와 데이터베이스의 Admin창 우리는 유저가 이 페이지에 접근권한이 없기를 원함 그렇기때문에 우리는 실제 사용 유저들만을 위한 분리된 admin창을 필요함 이 창에서는 데이터베이스에 있는 모든 유저와 어떤 내용이든지 바꿀 수 있지만 모든 유저들을 위해 있는 것은 아님 우리와 같은 웹마스터들을 위해서 있는것

이 admin user application 이외에 페이스북으로 로그인, 구글로 로그인 같은 것을 관리할 users application이 따로 필요한 것
설치된 applications에는 users application이 없음

# 아직 rooms같은 application이 실행되지 않는 이유
: 아직 application이 설치되지 않았음

####################################################################################################

#2.7 Explaining the Apps

# 프레임워크와 라이브러리
: 절대로 안에 있는 내용물의 이름을 바꾸면 안됨
우리는 라이브러리를 쓰는 것이 아니고 프레임 워크를 사용하는 것임
프레임 워크는 룰에 따라 사용해야함 라이브러리는 그저 뭔가를 build하기
위해 사용하는 것 react는 라이브러리고 우리가 변수명을 마음껏 사용할 수 있음 물론 파일명도 마음껏 사용할 수 있음 하지만 django에서는 그러면 안됨 django의 룰에 따라서 사용해야 함 좀 바꾸지 마라

# application은 어떻게 동작하는가?
: 우리가 어떤 코드를 admin.py에 넣든지간에 그 코드는 admin패널에 반영

# users - apps.py
: configuration 파일

# models.py
: 우리가 원하는 database가 어떻게 생겼는지에 대해서 설명
우리의 data를 변경하는 곳

# tests.py
: 말그대로

# views.py
: html을 render(보여주는) function을 넣게 될것임
그 function은 form을 보여주고 upload 그리고 심지어 view가 없는
모든 것들을 처리 하게 될것임

# urls.py
: 웹 사이트의 url을 컨트롤
모든 url을 config의 urls.py에 넣는 것은 좋지 않음
우리는 많은 urls를 갖게 될것 그렇게 되면 너무 커지게 될 것임
우리에게 필요한 것은 Divide and Conquer(분할 정복)
applications에 각각 만들어줌

####################################################################################################

#3.0 Replacing Default User

# models.py
: 우리가 원하는 database가 어떻게 생겼는지에 대해서 설명
우리의 data를 변경하는 곳
이미 models class가 있기 때문에 우리가 생성한 models.py에 상속해서
사용할 수 있음

# user application
: settings.py에서 설치해야함

####################################################################################################







####################################################################################################