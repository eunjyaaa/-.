# git의 기초
1. 일반 디렉토리를 git이 버전 관리할 수 있게 한다.
```bash
git init
```
★ 디렉토리별 딱 한 번만 한다.

2. git의 3요소
   - working directory: 작업공간, 분장실
   - staging area: 대기공간, 무대 위
   - repository: 버전이 기록되는 공간, 사진찍은 목록
  
3. 3요소를 넘나들기 위해서 쓰는 git 명령어
   - working directory -> staging area
    ```bash
    git add 파일명
    ```
   - staging area -> repository
    ```bash
    git commit -m "버전을 기록하는 이유"
    ```

4. 상태와 기록을 확인하기 위한 명령어
   - 파일 상태 확인
    ```
    git status
    ```
   - 버전 기록을 보기 위한 명령어
    ```
    git log
    ```
    ```
    git log --oneline
    ```