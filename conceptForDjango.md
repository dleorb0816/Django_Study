# 장고 학습을 위한 주요 개념들

#### - Framework(프레임워크)
#### - VirtualEnvironment(가상환경)
#### - Project vs App(Application)(프로젝트 vs 앱)
#### - Model(모델)
#### - MVC
#### - MVT


## 프레임워크란 무엇인가?

- **장고는 프레임워크다. 프레임워크란 무엇이고, 장단점을 설명해보시오**  
  - 장고는 파이썬으로 개발된 오픈 소스 웹 프레임워크다. 기본적으로 모델(M)-뷰(V)-컨트롤러(C)패턴을 따른다.
  - 데이터베이스와 연동 웹사이트 개발을 초보자라도 편리하고 쉽게 개발할 수 있도록 해주는 것을 목표로 만들어졌다.  

- **프레임워크 장점**
  - 프레임 워크는 기본적으로 "틀"을 생각하면 쉽다
  - 규칙이 적용된 "틀"안에서 규칙과 가이드대로 개발을 해나가면 초보자라도 품질 좋은 웹사이트를 만들 수 있다.
  - 모든 생활시설 및 가전제품들이 다 구비된 빌트인 아파트를 생각하면 쉽다. 규칙대로 살아가기만 하면 된다.
  - 유지보수 등을 위한 직원 및 개발팀의 충원이나 연속성이 비프레임워크에 비해서 상대적으로 보장된다.
  - 안정성, 통합성, 유지보수, 효율성, 단축성, 확장성 등 일관성 있게 추진이 가능하다.
  - 가장 큰 장점은 초보자라도 경력자가 만든 것과 같은 상당한 수준의 퀄리티있는 웹사이트를 개발해낼 수 있다는 것이다.
  - 프레임 워크를 사용하지 않고 초보자가 경력자와 같은 품질의 웹을 개발한다는 것은 거의 불가능이다.

- **프레임워크 단점**
  - 프레임워크의 가장 큰 단점은 학습곡선이 만만치 않다는 것이다. 즉 배우는 것이 어렵다.
  - 모던한 개발 방식이 많이 도입되는 편이라서 기존 전통적인 방식으로 웹개발을 해온 사람들에게는 새로움이 많다.
  - 대부분의 경우 웹개발 경험이 전무한 초보자라면 거의 불가능에 가깝다.
  - 설령 경험자라 하더라도 독학으로는 많은 시간이 걸리며, 수많은 시행착오와 오류에서 혼자 헤쳐나가기는 매우 힘들다.
  - 규칙과 가이드에서 벗어나는 것을 대부분의 프레임 워크가 허용하지 않는다.
  - 제공하는 틀안에서 모든 것을 규칙에 맞게 그리고 가이드에 맞게 개발해 나가야 하지만 원할한 개발이 가능하다.
  - 기존의 전통적인 방식으로 개발된 웹사이트와 통합하기가 쉽지 않다. 새롭게 만드는 것이 더 효율
  - 그러나 익숙해지고 숙달되면 쉽고 편리하게 웹개발이 가능하다.
  
- **가상환경이란 무엇인가?**
  - 가상 환경은 웹 개발 프로젝트를 진행할 때 독립된 환경을 구축해 준다. 이것은 매우 큰 장점이다.
  - 웹 개발 프로젝트 성격에 따라 프로젝트 마다 프로젝트에 사용되는 라이브러리나 관련 버전들이 다를 수 있다.
  - 이때 가상환경 도구를 이용하여 각각의 프로젝트에 맞는 독립된 환경을 구축할 수 있다.
  - 개발자의 PC한 곳에 각각 파이썬 및 장고 그 외 라이브러리 들을 버전별로 맞춰서 셋팅을 할 수 있다.  
  - 여러 개의 프로젝트를 만드는 것이 아니라면 사실 가상환경이 필요없을 수도 있지만 필요성 및 중요성은 계속 커지는 중..
  - 가상 환경 구축 툴이 여러개 있는데 파이썬내 모듈인 venv 모듈을 사용하여 아래처럼 구축한다.
  - **python -m venv 가상환경이름 -> 파이썬내 venv라는 모듈을 사용하여 구축**

## Project VS App

- **Project와 App은 무엇인가?
  - 기본적으로 프로젝트는 가장 큰 또는 최상위의 웹 개발 디렉토리(폴더)라고 생각하면 된다.
  - 웹 개발시 최상위 폴더를 생성하고 개발을 해나가는데 이것은 결국 해당 웹사이트의 루트 폴더가 되고 곧 프로젝트다.
  - 이한에 여러개의 프로그램(회원가입, 게시판,설문조사 등) 만들어 넣을 수 있는데 이를 "App(앱)"이라 부른다.
  - 결국 이런 여러 개의 앱들이 모여서 하나의 프로젝트가 되고 이는 곧 하나의 웹사이트가 된다.  
  - 장고에서 프로젝트 생성은 명령 프롬프트에서 **django-admin startproject 프로젝트명** 입력하고 생성
  - 보통은 위와 같이 생성을 하는데 이렇게 생성 시 같은 프로젝트명으로 환경설정 폴더가 생성이 된다는 것을 명심
  - 별도의 환경설정 폴더명을 가지는 방식으로 생성하는 것도 가능하나 장고 학습 시에는 이렇게 하는 것도 큰 상관은 없다.
  - 앱 생성은 **python manage.py startapp 앱명** 으로 생성한다.

## Model이란 무엇인가?

- **장고프레임워크에서 Model이란 무엇인가?**
  - 웹 개발 경험이 없는 초보자에게 모델이 무엇이냐고 물으면 대부분 슈퍼모델 선발대회가 연상될 수 있다.
  - 그만큼 모델의 개념은 초보자에게 난해하고 바로 떠오르는 개념이 아니다.
  - 여러 개념들중 가장 매칭이 안되고 바로 이미지가 연상되지 않는 개념중 하나라고 보면 된다.

- **모델은 곧 데이터(데이터베이스)**
  - 이제부터 모델이라고 하면 제일 먼저 "데이터"또는 "데이터베이스"를 우선적으로 연상하면 된다.
  - 장고 프레임워크에서 뿐만 아니라 다른 대부분의 프레임워크에서 마찬가지이다.
  - 즉 장고는 모델(Model)을 이용하여 데이터 및 데이터베이스 연동 작업을 처리한다고 생각하면 된다.  
  - 일반적으로 프레임워크가 데이터베이스 연동 작업시 데이터를 처리(CRUD)하기 위해서 SQL 쿼리문을 이용한다.
  - 그러나 프레임워크도 발전함에 따라 초보자들이 보다 데이터베이스 연동 작업을 편리하고 쉽게 할 수 있도록 발전했다.
  - 어떻게 처리?

- **어떻게 처리?**
  - DB를 건드리지 않고 코딩만으로 DB작업을 처리
  - 기존의 전통적인 방식의 웹 개발만 해본 사람들에게는 매우 신기하게 보여질 수도 있다.
  - 아예 웹 개발 경헙이 없는 사람들에게는 이것이 신기한 것인지? 모던한 웹개발 방식인지? 아예 모른다고 보면 될 것이다.
  - 중요한 키포인트는 세계적인 추세도 그렇고 국내 추세도 그렇고 이와 같은 흐름대로 DB 작업이 되어간다는 것이다.
  - 자바쪽의 스프링, 스프링부트 프레임워크에서도 JPA기반으로 이와 같이 DB연동을 처리해 나간다.
  - 장고 역시 이와 같은 방식으로 코딩(파이썬 코드)을 통해서 테이블을 생성하고 데이터베이스 연동 작업등을 처리한다.
  - 즉, 장고의 모델(Model)을 사용하면 기존의 SQL 쿼리문과 같은 것 없이 데이터 처리 및 DB 연동 작업을 할 수 있다.
  - 이것이 장고 프레임워크에서 데이터베이스 연동 및 데이터를 처리하는 방식.
