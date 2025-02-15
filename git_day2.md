# 작업환경 세팅하기

1. 강의장 컴퓨터
2. 원격 저장소
3. 집 컴퓨터

## (1) git clone

git아, 원격저장소에 올라와 있는 모든 파일과 변경사항의 기록들을 복제해줘!
```
git clone 원격저장소URL
```

(주의) git clone 하는 위치는 git으로 관리되지 않는 폴더, 즉 바탕화면/홈폴더

## (2) git pull 
원격저장소에서 로컬 저장소로 변경사항의 기록을 가지고 옴. 
(만일 업데이트가 있다면 !)
```
git pull origin master
```
## (3) 두 저장소의 변경사항 기록이 맞지 않다면?
- `[rejected]` -> 내가 가지고 있는 commit들의 내역과 원격저장소의 내역이 맞지 않으면, push 불가능
- pull로 변경사항의 내역을 가지고 온 다음, `수정 -> add -> commit` 
  - 충돌을 수정한 또 하나의 커밋을 쌓는다.
- 수정 이후, `push`하면 된다.
  
## (4) 하나의 원격 저장소를 공유하는 두 로컬 작업소에서..
- 공동 작업자를 추가하고, 편집 권한을 얻게 된 유저는 `git clone`을 통해 복제한다.
- 복제된 폴더를 열어서 작업 후 `add, commit, push`를 통해 변경 사항 기록한다.
- 다른 유저는 편집하고자 할 때 `pull origin master`을 통해 변경 사항을 가져와서 이어서 편집한다.
> 만일 수정사항에 충돌이 발생한다면?
  - `pull`해서 변경 사항을 알맞게 수정한 이후, `add, commit`하고 마지막으로 `push`하여 충돌을 수정한다!

## 브랜치 목록 확인
```
git branch
```
## 새로운 브랜치 생성
```
git branch 신규브랜치명
```
## 평행세계로 이동!
```
git switch 브랜치명
```
## 특정 브랜치 삭제
```
git branch -d 브랜치명
git branch -D 브랜치 명 # 병합 안된 브랜치도 강제 삭제
```
## 브랜치 정보 확인하기
```
1. branch 정보 확인하기
git branch
2. 평행세계 정보 시각적으로 확인하기
git log --oneline --graph -all
```

## 브랜치 병합하기
- 작업이 완료된 브랜치를 master 브랜치 상용브랜치로 병합합니다.
이때, 꼭 master로 이동해서 실행 (master 상태에서 병합할 것!)
```
git merge 병합하고자 하는 브랜치
```
> 만약 충돌나면? conflict 해결하고 다시 수정후, 커밋한다.