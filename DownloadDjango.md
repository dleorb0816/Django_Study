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

## Django 설치후 
