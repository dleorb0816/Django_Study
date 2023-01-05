# Superuser 생성 및 기본 테이블 생성

## 장고 프레임워크 슈퍼유저 및 기본 테이블 생성

  -> c:\zdragon\myproject> python manage.py createsuperuser  
  -> 그런데 **기본 테이블 생성**이 안되어 있기 때문에 슈퍼유저(superuser) 생성이 안된다.  
  -> 기본 테이블 생성 --> python manage.py migrate  
  -> 기본 테이블 생성 후 다시 --> 슈퍼유저 생성 --> python manage.py createsuperuser  
  -> 관리자모드 접속은?? -->  localhost:8000/admin
