# App 생성하기

## 1. 앱이랑 무엇인가?
- 기본적으로 App == Application == Program(프로그램) 같은 의미로 생각하면 됨.

## 2. Project vs App 차이는 무엇인가?
- 프로젝트는 큰 개념이고 앱은 그 하위의 작은 개념.
- 큰 프로젝트 안에서 필요한 프로그램들의 단위가 앱으로써 회원가입, 게시판, 설문조사 등의 앱이 있을 수 있음.
- 즉 앱은 프로젝트내에서 특정한 기능을 수행하는 프로그램 단위.

## 3. 앱생성 명령어
- 가상모드로 진입
- C:\zdragon\myproject>py manage.py startapp onememos

## 4. onememos 폴더 생성 및 파일들
- migrations(폴더)
- admin.py
- views.py
- models.py
- urls.py(별도로 수동으로 생성해줘야 하는 파일. 최상위 URLconf와의 연결을 위하여 필요. 최상위 urls.py파일에 있음)

## 5. 최상위 urls.py --> urlpatterns --> 앱패스 추가
- path('onememos/', include('onememos.urls')),#include임포트 했는지 확인. 안하면 서버 구동시 에러.
- path('admin/', admin.site.urls),

## include() 함수
- 다른 URLconf패스들을 참조할 수 있도록 해주는 함수. 앱 구동 및 연결 시 중요한 역할을 하는 함수.
