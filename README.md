## Django project with Nginx

### With Amazon EC2

### With Ubuntu Instance

AWS EC2 Ubuntu 인스턴스를 만들고, Django 를 설치 한 뒤에 git 과 연동하여 로컬에서 개발한 내용을 aws에 적용하는 과정을 진행. -> 21/8/23

### Django Project

<img src="https://user-images.githubusercontent.com/63331153/130817299-aa76ff89-76c4-46d4-90b6-6c2290e83b8d.png">

Web Client -> Django 서버로 API를 호출하는 앱이나 웹.

WebServer -> Nginx or Apache ( 클라이언트로 부터 요청을 받아 웹 어플리케이션으로 전달하고, 그에 대한 응답을 다시 클라이언트로 전달하는 역할. sender 의 역할만 한다고 생각하면 된다. {사실상 static data는 전달안하고 그냥 넘겨줌})

Socket -> 웹서버와 WSGI( Web Server Gateway Interface ) 사이에 데이터를 주고 받기 위한 인터페이스. 소켓은 간단하게, 네트워크를 사용한 Http 소켓이 될수 있으며, 파일을 사용한 소켓이 될 수도 있다.

WSGI -> 웹서버와 웹 프레임워크사이에 통신을 담당하는 인터페이스. ( using uWSGI )

pyenv , virtualenv 를 이용하여 django 프로젝트를 만드는 가상 환경을 만듬.

requirements.txt 생성하여, dependency 관계 세팅

### Docker Image

<img src="https://user-images.githubusercontent.com/63331153/130815561-2e3ad6e8-c53e-41ff-8dd0-8a3c3d163678.png">

<img src="https://user-images.githubusercontent.com/63331153/130816611-82cbc942-caef-4a52-8ea7-9160d87549d1.png">
