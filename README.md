
# Git 메모

Git 메모

(repoisitory 삭제하면 잔디 사라짐)

git bash 로 버전관리 할 폴더에서

git init 명령어 실행 -> 이 폴더는 이제 깃으로 관리한다 (버전관리한다)

gitignore : 사용자가 git에 등록되지 않길 우너하는 파일 또는 폴더들의 목록을 저장

->gitignore에 등록된 파일들은 커밋 시 자동으로 제외됨


깃(git)은 4가지 공간을 가지고 있음


Working directory : 작업하는 파일이 있는 디렉토리

Staging Area : git에 등록할 (커밋) 파일들이 올라가는 영역

Local Repository : 로컬 git 프로젝트의 메타데이터와 데이터 정보가 저장되는 영역

-------------------------------------------------------여기까지 로컬(내 컴퓨터)에 저장됨

Remote Repository : Github등의 서비스를 통한 온라인 상의 저장소


Repository : 저장소

git 저장소는 파일 변경 이력 별로 구분되어 저장

Local Repository : 내 pc에 저장되는 개인 공간

생성과정

1. 원하는 폴더 생성
2. 해당 폴더에서 git init 명령어 입력
3. .git 폴더 생성 확인

Remote Repository : 파일이 전용 서버(GitHub)에서 관리되며 여러 사람이 함께 공유
생성방법 : Github 통해서 생성

clone : Remote Repository를 복제해 내 pc에 local Repository로 저장하는 것

head : 작업 중인 위치(branch)를 가리키는 가상의 커서를 의미

add : 변경된 파일 중 repository에 올릴 파일들을 등록한다. (working dir -> Staging Area)

commit : add로 등록된 파일(stagin area 의 데이터)을 한 덩어리로 만들고 메시지를 추가해 로컬저장소에 올림

push : commit되어 로컬 저장소에서 변경이 된 파일들을 원격 저장소(Remote Repository)로 전달

pull : 원격저장소의 변경사항을 로컬저장소로 가져옴(fetch)과 동시에 내 작업 소스에 합친다(merge).
(pull=fetch+merge)

체크아웃 : 저장소에서 특정 커밋이나 브랜치로 돌아가고 싶을 때 사용

origin/main 은 Remote Repository 의 위치임

Branch : 기존에 만들어 놓은 버전(main)에서 복사해 새로운 가지를 만들어 다른 방향으로 작업을 이어나가는것

새 브랜치체크아웃을 해야 브랜치를 만든 후 새브랜치로 체크아웃 됨
이거 안하면 브랜치를 만들어도 기존의 체크아웃 되어있는 브랜치로 헤드가 유지되어 있어서
커밋을 하면 새 브랜치가 아닌 기존의 브랜치에 커밋이 됨

브랜치를 만들고 커밋을 하면 메인이 아닌 브랜치에 커밋이 됨

브랜치를 만든 상태에서 메인의 코드가 바뀌면 가지가 생김 (브랜치 코드가 바뀌면 브랜치 가지가 뻗어져나감)

머지 하면 로컬레포에 변경사항이 생김

conflict(충돌) : 같은 파일 같은 부분을 수정한 브랜치들을 Merge 할 때 발생
충돌이 발생 했을 땐 어느 한 개를 선택 해야함
	
fork : 다른사람의 원격 저장소에서 어떤 부분을 수정하거나 추가 기능을 넣고 싶을때
	해당 원격 저장소를 내 원격 저장소에 그대로 복제하는 것

Pull Request
다른 사람에게 내 브랜치를 Merge 해 달라고 요청
사례 1 : 한 원격 저장소에서 내 브랜치를 merge 하기 전 피드백 요청 (신입사원의 경우)

ISSUES : 프로젝트의 작업, 개선사항, 버그를 추적하고 커뮤니케이션 할 수 있는 github에서 	  제공하는 기능


README : 
![20220909_162122](https://user-images.githubusercontent.com/104514223/189294575-74c64a3a-fc65-4762-928a-c35495c91f03.png)

<code>
	<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>메인은 계속적으로 새 브랜치 영향 없이 진행</title>
</head>
<body>
    테스트
    <p>충돌이 날꺼야...!!</p>
</body>
</html>
</code>

- 1번 이슈
- 2번 이슈
- 3번 이슈
