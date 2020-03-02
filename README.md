# webhook

* github 에서 webhook 설정할 수 있는 방법을 설명한다. 

## 사용법

### github 셋팅
* Settings -> Webhooks -> add Webhook 로 들어가면 
  * Payload URL: Jenkins URL을 입력해준다. 예) http://{공인IP:포트}/github-webhook/ 
  * Content-Type: Json 으로 설정한다. 
  * secret 은 무엇을 의미하는지 모르겠다. 제킨스에서 github 연동하면 자동으로 secret 값이 입력이 되긴 한다.
  * 그 아래 라디오 버튼은 어떤 이벤트를 보낼 것인지를 나타내는데 알아서 선택하자 
  * 여기까지가 github 에서의 셋팅이다. 
  
### jenkins 셋팅

* 새로운 잡을 만들어 준다.
* git 소스 위치 지정한다. 
* 빌드 유발 탭에 `GitHub hook trigger for GITScm polling` 체크박스을 체크해준다. 

### 마무리

* 여기서 소스 아무거나 업데이트하고 푸시하면 jenkins 잡이 잘 작동된다. 
* 근데 이상하게 wiki update 시 푸시하라고 체크해뒀는데 작동하지 않는다. 
