# 개요
Google Drive에 업로드 할 수 있는 모듈을 만든다.

# 사용 방법
https://console.cloud.google.com/ 접속하여, credentials.json을 발급 후 프로젝트 폴더에 저장한다.

프로젝트를 실행한다.
```bash
go run main.go test.txt
```

```bash
Go to the following link in your browser then type the authorization code: 
https://accounts.google.com/o/oauth2/auth?access_type=offline&client_id=....
```
위 링크에 접속하여 구글계정 로그인을 한다.
그 후 URL을 보고 code 부분의 HERE만 복사하여 붙여넣는다.
```bash
http://localhost/&code=HERE
```
여기까지 진행하면 token.json이 생성됐다. 이제 사용할 준비가 완료됐다.

```bash
go run main.go FILE_NAME
```