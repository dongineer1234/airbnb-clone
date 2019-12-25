####################################################################################################

#0.0 Introduction

# django
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

# django, python의 공통점
: Object Oriented(객체지향) 방식을 따름
class, inheritance(상속)를 잘 이해하는 게 중요

# django
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
2개의 version이 있는데 free version에서는 django에 대한 충분한 지원이 없음
django와 html, js에 대한 지원을 바란다면 Professional version을 받아야 함

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

# django
: 웹 어플리케이션(파이썬)을 만들기 위해 사용되는 유명한 프레임워크
모든게 class, inheritance로 돌아감
django는 거대한 프레임워크로 사용 예로는 사용자 인증을 처리해주고
컨텐츠 관리 기능이 있음 관리자 페이지, 사용자 인증이 django를 사용하는 가장 큰 이유
이미 만들어진 form들이 있어서 필요한 기능(패스워드 바꾸기, 프로필 바꾸기)이 있으면 
갖다 쓰면 됨 이메일 백엔드도 있어서 이메일 인증도 해줄 수 있음 보안기능도 있음
아주 빠르고 신속하고 커스터마이징도 쉬움
airbnb에는 로그인, 로그아웃, 관리자 패널, 뭔가 업로드하고 삭제하는 기능이 필요하기,
비밀번호 변경하기, 본인확인 이메일 등 기능이 필요 하기 때문에 django가 적합

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
: django-admin startproject project
이렇게 하는건 전문가아님

# 전문가의 create project
: main directory에 진입해서
django-admin startproject config를 실행
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

####################################################################################################
