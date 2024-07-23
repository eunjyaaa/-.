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

