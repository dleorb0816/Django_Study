## Django 다운로드

1. 파이썬 다운로드 및 설치
2. 가상환경 구축먼저 해주는 것 권장(venv 사용)
3. Pip 프로그램을 이용하여 설치(Django 설치)

## Django 가상환경 구축 및 설치

1. 본인 PC에 설치된 파이썬 버전 확인
- cmd 명령 프롬프트에서 C:>python 입력하고 버전 확인
2. 가상환경 구축 -> 구축한 가상환경 디렉토리 진입 -> 활성화 -> 장고 설치
- 가상환경 구축 1 -> python -m venv mywebsite(파이썬 모듈 중 venv라는 모듈을 사용하여 가상 디렉토리 생성)
- 가상환경 구축 2 -> pip install virtualenv(https://virtualenv.pypa.io/en/latest/index.html) 
                    -> 가상 디렉토리 생성 -> virtualenv mywebsite
- mywebsite 디렉토리로 이동 후 -> scripts 디렉토리 -> activate.bat 실행 -> 가상환경 안에서 -> pip install Django

## Django 설치후 버전확인

1. 본인 PC에 설치된 파이썬 버전 확인
- CMD 명령 프롬프트에서 C:>python 입력하고 버전 확인.
2. 본인 PC에 설치된 장고 프레임워크 버전 확인
```python
import django
print(django.get_version()) # 장고 임포트 후 장고 프레임워크 버전 확인.
C:₩users₩userid₩python -m django --version

가상환경을 빠져나오는 방법 -> deactivate
```
## Django 삭제

1. 장고 프레임워크 삭제
설치를 수동 및 자동으로 할 수 있는 것처럼 삭제 또한 수동 및 자동삭제가 가능.  
만약 Pip 프로그램을 이용하여 설치하는거라면 내부적으로 구버전에 대한 부분을 삭제하고 설치하므로 고민할 필요 X  
그러나 수동 설치 시에는 장고가 설치된 디렉토리로 이동해서 명령어 등으로 삭제 후 진행해야 한다.  

2. 윈도우에서 장고 프레임워크 삭제
 구축한 가상환경 디렉토리를 서브 디렉토리까지 모두 지우는 도스 명령어 옵션을 줘서 삭제해주면 된다.  
    -> c:₩>md 디렉토리명  
    -> c:₩>rd 디렉토리명  
    -> /s 옵션  : 서브 디렉토리까지 삭제. 이 옵션을 사용하면 서브 디렉토리까지 삭제할 것인지 물음.  
    -> /q 옵션  : 삭제여부를 묻지않고 삭제.(5분 50초부터 들으면 됨)  
    
## Django 특정버전 지정 설치

1. Pip 프로그램을 이용한 장고 프레임 워크 특정 버전 설치
    -> pip install Django==3.2.9  
    -> pip uninstall Django (삭제시 장고 버전을 따로 지정하지 않아도 됨)  
    

## Django 학습환경 구축 실습

1. 실습 디렉토리 생성  
    - c:\>Django
    - md,rd, /s, /q 옵션들 사용  
2. 파이썬 설치 버전 확인 후 --> 가상환경 구축 --> venv모듈 사용 --> myenvironment 이름으로 생성 --> 폴더 100여개, 파일 900여개  
    - python
    - python - m venv 가상환경이름(myenvironment) [주로 다른 웹사이트를 만들때는 또 다른 가상환경을 만든다.]
3. 가상환경 디렉토리(myenvironment)로 진입 후 --> 활성화 작업(activate.bat)
    - c:\ > Django > myenvironment > Scripts > activate.bat(가상환경 모드로 진입)
    
    * 가상환경 모드로 진입한 화면
    ```
    ( myenvironment ) c:\>.................
    ```
4. 장고 설치
    - pip install Django 또는 pip install Django==3.2.9
    - pip uninstall Django
5. 장고 버전 확인
    - import django
    - print( django.get_version() )
    - python -m django --version => 명령 프롬프트에서 실행할 경우

## 웹사이트 띄우기 

1. 프로젝트 생성 --> mywebsite or mysite or myporject  
  1-1. 제일먼저 가상환경 모드로 진입 --> myenvironment --> Scripts --> activate.bat 활성화  
  1-2. 만약 가상환경 모드로 진입하지 않고 뭔가를 하려고 하면(버전확인) --> X  
2. C:\zdragon> --> 실픕 폴더 루트로 이동해서 --> 프로젝트 생성
  2-1. django-admin startproject myproject(프로젝트 이름)
