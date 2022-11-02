# mes_on_k8s
MES 용 쿠버네티스 매니페이스 파일 작업

### 4개의 서버로 구성됨
* eureka : rest-serivce 와 api-gateway Pod의 endpoint를 관리하는 서버
* api-gateway : eureka 에서 rest-serivce 의 endpoint 를 받아서 frontend service 에서 오는 요청을 rest-service 로 라우팅하는 서버
* rest-service : 백엔드에서 DB와 통신하며 RestAPI를 제공하는 서버
* fron-service : 사용자 UI 환경의 서비스