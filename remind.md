# GIT과 Github

## [1] Git이란?
- (분산) 버전 관리 프로그램

## [2] Git 시작하기
누가 어떠한 변경사항을 남겼는지 git이 자동으로 만들어주기 위해 get config 필요
global한 정보를 주었기 때문에 "최초" 한 번만 설정하면 된다!

```
git config --global user.name "이름"
git config --global user.email "메일 주소"
```

확인하기 위해서는
```
git config --global --list
```

## [3] GIT의 3공간
1. working directory -> 분장실
2. staging area -> 무대 
3. repository -> 사진 저장소

분장실 -> 무대 -> 사진 저장소로 우리가 사진을 찍어 내기 위해서

## [4] GIT 기본 명령어
### (1) git init
```
# 로컬 저장소를 만든다 -> 현재 작업중인 디렉토리를 GIT으로 관리한다.
git init
```
이후, `master` 표시가 뜨게 된다.

### (2) git add
working directory에서 작업이 완료된 파일을 무대(staging area) 위로 올린다.

```
git add 파일명
```
### (3) git commit
staging area 즉, 무대위에 있는 모델의 사진을 찍는다. 기록한다.

```
git commit -m "변경사항이 기록된 이유"
```
> 메시지를 남기는 이유?
버전 관리 프로그램 git이 자동으로 변경사항에 대한 "육하원칙"을 작성하기 위해 왜 바꾸었는지에 대한 정보가 필요해서 메시지를 남긴다.

### (4) git status
각 파일들의 상태를 알려준다. (Untracked, modified, New file, nth to commit)
```
git status
```

### (5) git log
변경사항들의 기록을 보여줘
```
git log
git log --oneline
```

=> 로컬 저장소 (내 컴퓨터에서 버전 관리하기)

## Github
서버컴퓨터처럼 원격에서 나의 변경사항 기록들을 가지고 있도록 할 수 있다!

### (1) repository 생성
1. 우측 상단 + 버튼 눌러서, repository 만든다!
2. URL 생성된다. -> 원격 저장소의 주소를 의미합니다.
3. 복사!

### (2) 로컬 저장소와 연결
```
# 원격 저장소 연결
git remote add origin /URL/

# 원격 저장소 연결을 확인
git remote -V
```
### (3) 로컬 저장소에서 변경사항을 원격저장소로 보내기
로컬 저장소의 커밋을 원격 저장소에 반영
```
git push origin master
```

# .gitignore

## `.gitignore` 란?
> .git + ignore -> 깃아, 이 파일/디렉토리는 무시해

.gitignore 에 적혀져 있는 파일 혹은 디렉토리는 더이상 버전 관리하지 못하도록 막아주는 역할을 합니다.

## 언제 필요한가요?
1. 민감한 개인정보가 담겨 있을 때,
2. OS (운영체제)에서 자동으로 만드는 불필요한 파일
3. 통합 개발환경 등에 사용되는 파일

## 어떻게 쉽게 작성하나요?
[gitignore.io](https://www.toptal.com/developers/gitignore/)

등을 활용하여, 자신의 개발환경에 맞게 복사 붙여넣기 하기

### 주의사항!
- 반드시! 이름을 `.gitignore ` 로 작성합니다. 
  - 앞에 붙은 점은 숨김파일이라는 의미이고, 점이 없으면 제대로 작동하지 않아요.

- `.gitignore` 파일은 `.git/` 폴더와 동일한 위치에 있어야 합니다.
  - 이를 확인하기 위해 ls -a 커맨드라인 명령어 사용하면 좋아요.

- 특히 제외하고 싶은 파일은 반드시 git add 전에 ignore 처리해야 합니다.

