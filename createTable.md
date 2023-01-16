# 테이블 생성하기

장고 프로젝트에서 애플리케이션(App)을 생서하고, 여러 데이터 값들을 저장하기 위해서 --> 모델(models)   
이 모델을 사용하여 테이블을 생성하고, 데이터를 어떻게 처리하는지에 대해서 학습 --> 중요!!  

python manage.py migrate --> 실행 --> 프로젝트 생성시 필요한 기본적인 테이블, 앱들이 설치.  
이렇게 설치된 앱들은 어디? --> 환경설정폴더(myproject or config)[최상위 폴더]/settings.py파일에서 확인이 가능.  

# 왜 이름이 모델일까? --> 왜 이름이 모델이지???
 1) 일상 용어에서 사람들이 뭔가를 대표하고 샘플표본으로 받아들일 만한 단어가? --> 모델(model), 표본(specimen)  
 2) 예를들어, 후진국 또는 개발도상국에서 경제성장을 위하여 롤모델로 삼을만한 선진국이 어디일까? --> 대한민국  
 3) 어떤 프로그램(App)을 만들 때 데이터가 저장되고 관리되는 것이 필요한데 이러한걸 처리하기 위한 모델(표본)이 필요하다.  
 4) 이러한 모델 --> 데이터 모델 or 데이터베이스 모델  
 
 한줄 메모장  
           - 한 줄 메모장에 필요한 데이터 모델이 필요.  
           - 뭐가 필요하지???(고민)  
           - 어떤 필드(컬럼)들이 필요하고, 또 각각의 필드 타입은 어떻게 정할까?(고민)  
           - 이렇게 해서 만들어진 데이터 모델 --> 테이블

**최소한의 필요한 것 위주로 데이터 모델을 만든다면?**  
- idx(정수형)  
- memo_text(문자형)  
- published_date(날짜형)  

onememos앱안의 models.py에 아래와 같이 코드 작성  
```python
from django.db import models

# Create your models here.
# 1) 데이터 모델
# idx (PK는 굳이 코드 작성할 필요가 없다.)
# memo_text
# published_date
class Memo(models.Model):
    memo_text = models.CharField(max_length=200)
    published_date = models.DateTimeField(auto_now_add=True)

# 2) 작성 후 --> 반영을 위해서 --> 어디에? --> Admin 사이트에 반영 --> admin.py 열고 추가 작성.
```

onememos앱안의 admin.py에 아래와 같이 코드 작성

```python
from django.contrib import admin
from onememos.models.py import Memo

# Register your models here.
# Memo를 Admin사이트에 등록한다라는 뜻
admin.site.register(Memo)
```

**migrate 하기 전에 해야할 두가지**
- 최상위 폴더의 settings.py파일의 Installed_Apps에 내용 추가
- cmd에 ```py manatge.py make migrations```입력 하면 onememos앱 안의 migrations에 테이블이 만들어진다
- cmd에서 migrate명령어 실행
