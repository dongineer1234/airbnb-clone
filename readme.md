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

#3.1 Introduction to the User Model

# python manage.py makemigrations
: user migration, User model 생성 user에 관한 별게 다 있음

# python manage.py migrate
: migration 그리고 서버에 연결하면 오류가 뜨지 않을 것임

# 0001_initial.py
: 여기 필드에 각종 요소가 있는 이유는 models.py에 AbstractUser을 넣었기 때문

# python manage.py makemigrations
: user migration, User model 생성 user에 관한 별게 다 있음
models.py에서 설정 후 명령어 실행 하고 python manage.py migrate
명령어 실행

####################################################################################################

#3.2 First Model Fields

# bio = models.TextField(default="") default를 붙이는 이유
: 데이터베이스에 bio의 값이 없어도 default값을 넣어줌
default를 해줘야 데이터베이스가 처리할 수 있음
혹은 null=True를 사용하여 데이터베이스에게 이 비어있는 건 신경쓰지마
할 수 있음 column이 생기기 전부터 있던 데이터를 채움

# docstring
: python에서 사용 되며 클래스를 만들 때마다 이런 문구를 넣어서
이게 무슨 클래스인지 알려주는 것

# pillow
: python의 라이브러리며 없으면 migration이 안됨
pipenv install Pillow

# models.py
: 우리가 원하는 database가 어떻게 생겼는지에 대해서 설명
우리의 data를 변경하는 곳 models를 생성 후 makemigrations하면 필드가 생성됨 물론 다음 migrate까지 해줘야 함 현재 추가된게 avatar, gender, bio avatar에서는 사진도 선택이 가능 gender는 뭐든 입력이 가능
대단한게 makemigration 후 migrate할 필요가 없음
값에 blank를 허용하면 데이터베이스에 필수로 값을 넣어주지 않아도 됨
blank=True를 해줘야 form에 적용됨
이 모든 것은 전부 Django documentation에서 얻은 정보

# char, text 필드의 차이
: char 필드는 한 줄 텍스트고 글자 수 제한이 있음
text는 여러줄 쓸 수 있고 글자 수 제한이 없음

# char 필드
: 커스텀마이징이 가능 예를들어 초이스를 만들 수 있음

####################################################################################################

#3.3 Finishing User Model

# super 호스트
: 인증받은 airbnb 호스트

# models.py
: 우리가 원하는 database가 어떻게 생겼는지에 대해서 설명
우리의 data를 변경하는 곳 models를 생성 후 makemigrations하면 필드가 생성됨 물론 다음 migrate까지 해줘야 함 현재 추가된게 avatar, gender, bio avatar에서는 사진도 선택이 가능 gender는 뭐든 입력이 가능
대단한게 makemigration 후 migrate할 필요가 없음
값에 blank를 허용하면 데이터베이스에 필수로 값을 넣어주지 않아도 됨
blank=True를 해줘야 form에 적용됨
이 모든 것은 전부 Django documentation에서 얻은 정보
설정을 마쳤으면 migration을 만들고 migrate를 해줘야 함

####################################################################################################

#3.4 Falling in Love with Admin Panel

# admin에 model이 나타나게 만들기
: @admin.register(models.User) 이것을 decorator이라 부름
admin.site.register(models.User, CustomUserAdmin) 와 같은 것
이 말은 admin 패널에서 이 user를 보고 싶다는 말
decorator은 클래스 바로 위에 있어야 작동함 띄어쓰기 하면 안됨

# list _display
: Django admin패널 기능 중 하나
list가 admin에 출력됨

# list_filter
: Django admin패널 기능 중 하나
list의 필터기능 가능한 옵션들을 model에서 잘 찾아서 출력해줌

# admin 패널
: 장고는 기본으로 user를 위한 admin패널이 만들어져 있으므로
여태만든 건 개념을 설명하기 위하여 작성한 것이고 지우면 됨

####################################################################################################

#3.5 UserAdmin + CustomAdmin

# UserAdmin
: 썼더니 옆에 필터와 파란색 뭔가가 생김 비밀번호 바꾸는 버튼도 생김
하지만 UserAdmin은 우리가 만든 User 필드를 아직 모르는 상태
전에 만들어 놓은 avatar, gender, bio 이런거 싹 없어짐

# fieldset
: 퍼런거 밑에 섹터
이 안에 들어가는건 퍼런거 이름이 될 것
설정 후 들어가면 퍼런거 안에 지정한거 그리고 model에서 가져온 avatar, gender, bio 이런게 따라옴 원래 있던거랑 합쳐가지고 더 좋게 만들 수 있음

####################################################################################################

#3.6 RECAP OMG!

# 정리
: config는 마스터폴더 같은거고 나머지는 application
conversations, lists, reservations, reviews, rooms, users 이것들이
다 application
application은 function의 그룹
user에 보면 models와 admin이 있음 우리가 앞에까지 이것들을 구현해 보았음 우리가 장고를 사용하는 게 아니라 장고가 우리 코드를 사용하는 것
장고는 데이터베이스랑 통신 장고는 장고ORM(object relational mapping)이라는 아주 멋진 걸 탑재하고 있음 이것이 우리의 파이썬 코드를 SQL문으로 바꿔서 데이터베이스가 알아들을 수 있게 만들어줌
models.py에 집어넣는 것 모두 장고가 알아서 데이터베이스 테이블로 만들어 줌 model은 fields로 이루어져 있음 문자에 사용되는 char필드, text필드, date필드, boolean필드, url필드며 image필드까지 여러 필드가 있음 이미 프레임이 만들어져 있어서 적합하지 않은 파일이나 값을 입력하려해도 장고가 유효성 검사를 하며 허락하지 않음 모든 필드는 데이터베이스로 들어가게 됨 파이썬 코드를 입력하면 장고 magic으로
sql문으로 장고가 바꿔줌 우리가 model을 직접 보려면 admin 패널에서
볼 수 있음 admin 패널은 admin.py로 작업해줘야 함
admin.py에서 model을 가져오려면 register해줘야함
그러려면 class를 사용해야 됨 class는 기본적으로 model을 조정할 수 있음
class위에 decorator를 써주면 class의 위치를 알고 CustomUserAdmin class 위에 있으니까 models.User을 Customer User에 적용하려 한다는 것을 알게됨 전에도 말했듯이 admin.py에서 admin 패널의 구성을 바꿀 수 있음 그리고 이건 선택권이 아니라 장고가 이런 식으로 작동하도록 만들어져 있음 장고가 register된 model과 class를 찾은 다음 특정 키워드를 찾을것임 filedset은 퍼런부분임 admin밖에 있는 부분은
list_display임 장고는 상속이 쓰이는데 이미 만들어둔 기능을 복붙해줌
장고가 우리가 만든 폴더를 인식하려면 setting.py에 등록해줘야 함
setting.py에 있는 DJANGO_APPS는 이미 디폴트로 주어진 애들임
admin패널, auth, sesstions, messages같은 애들임 그리고 PROJECT_APPS는
우리가 쓰려고 하는 application임 THIRD_PARTY_APPS는 여기에 나중에 다른 사람이 만든 applications를 넣도록 할것임 넣은것을 우리 project에 import할 수 있음  그리고 우리가 만든 User를 쓰려고 AUTH_USER_MODEL를 바꿔줬음 매번 이걸 바꿔 줄 필요는 없음 필요에 따라 장고 User를 사용할 수 있음 application마다 요구사항이 다를 수 있음 그리고 넘어가기전
데이터베이스와 pycache파일은 꼭 삭제 migration도 삭제 migration은 항상 적게 유지하는 것이 좋음 model을 만들 때 migration은 한 번 해주는 게 좋음 아 그리고 항상 깜빡하는데 수정하면 makemigrate하고 migrate 꼭 해줘라

####################################################################################################

#4.0 TimeStampedModel

# room 생성
: models.py에서 생성후 admin.py에 등록
등록하고 나서는 당연히 안뜸 왜냐 migration을 안했기 때문

# django-admin startapp core
: core 폴더가 생기는데 여기서 다른 application에서 재사용 가능한
common 파일을 만들어 줄거임 그럼 효율적인 작업이 가능함 여기서 model을 만들어주고 이 model을 이용해서 rooms를 확장함 user을 제외한 모든 model은 전부 이 한가지 model을 활용해서 확장할 것임

# class Meta: abstract = True
: 데이터베이스에는 등록되지 않는 model이 됨

####################################################################################################

#4.1 Room Model part One

# pipenv install django-countries
: config - settings.py가서 INSTALLED APPS에 가서 등록
페이지 설명에 있는대로 설정해줌

# 좋은코딩 방법
: 먼저 django랑 관련된 걸 전부 import함
그리고 외부 패키지를 import해줌 그리고 내가 만든 패키지를 import
예를들어 파이썬에서 import를 할 경우 가장 위에다 써줌 그다음 django관련 그리고 외부패키지 그 다음 application을 import

# auto_now
: true해주면 model을 save할 때 date랑 time을 기록
model을 생성할 때마다 수시로 업데이트
model이 생성된 날짜를 구하려면 auto_now_add를 써주고
auto_now true가 새로운 날짜로 업데이트해줌

####################################################################################################

#4.2 Foreing Keys like a Boss

# foreign key
: 한 모델을 다른 모델과 연결시켜주는 역할
현재 room model과 host를 연결 일대다 관계

####################################################################################################

#4.3 ManyToMany like a Boss

# class
: 파이썬이 class를 발견하면 class를 마치 string처럼 보여줌

# model
: 아빠 model은 많은 자식들을 갖을 수 있음
마치 user가 여러 room을 가질 수 있는 것과 같음
user는 엄마 room은 자식 한 room에 여러명 user을 가질 수 없음



####################################################################################################



