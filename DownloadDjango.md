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
