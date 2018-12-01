# 4. 원격 저장소

***

# Github URL 패턴

## 1. HTTPS

`https://github.com/[사용자아이디]/[저장소명]`

## 2. SSH

`git@github.com:[사용자아이디]/[저장소명].git`

git 연결을 보다 안전하고 빠르게 하기 위해서 SSH 방식을 권장합니다.

### 1. SSH Key 생성
콘솔에서 `ssh-keygen` 명령을 사용합니다. SSH Key 값은 `~/[사용자 폴더]/.ssh/` 폴더 밑에 `id_rsa.pub` 파일로 존재합니다.

### 2. Github 설정
* Github 홈페이지에 로그인 합니다. 
* Profile 중 Settings 메뉴를 선택합니다.
* Settings 화면 중 우측 사이드메뉴에서 `SSH and GPG keys` 메뉴를 선택합니다.
* SSH Keys 화면에서 `New SSH key` 버튼을 찾아서 클릭하고 `id_rsa.pub` 파일의 내용을 복사해 넣습니다.

### 3. 로컬 사용자 환경설정
Remote URL 설정이 HTTPS 방식이라면 SSH 방식으로 변경해야 합니다.

* origin의 Remote URL 변경방법
`$ git remote set-url origin git@github.com:[사용자아이디]/[저장소명].git`

* origin의 Remote URL 변경여부 확인
`$ git remote show origin`
