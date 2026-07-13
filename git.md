### 버전 관리

- 세이브 포인트 버전 관리2
- 변경 날짜 저장
- 수정 부분만 저장
- 용량 관리

### “분산” 버전 관리

- 중앙 vs 분산
    - (중앙)모든 버전을 서버 중앙에서 하나로 관리
        - 서버에서 내용을 받아서 수정을 하고 다시 올린다거나,  ,ㅎㅎ
        - 대기업에서 사용하긴 함
    - (분산) 어디서든 개발 가능~
        
        ⇒ git hub/ git lab (저장공간 서비스 주최)
        
        - git은 시스템
        - 동시에 다양한 작업 수행 가능~
        - 장애 시 복구 가능~
        - 인터넷 환경이 아니어도 작업 가능~!
- 코드 버전 관리
- 개발 과정 파악
- 이전 버전과 변경 사항 비교
    
    

### GIT 영역 (가상)

- Working Directory (작업 공간)
- Staging Area (저장하기 전 확인하는 중간 공간)
- Repository (저장 공간)
- commit
    - 변경된 파일 저장

### GIT 동작

- git init
    - 로컬 저장소 설정 (초기화) ; 영역 선포 (최초 1회)
    - git 버전 관리 시작할 디렉토리에서 진행
- git add
    - working directory → staging area
- git commit
    - staging area → repo
    - -m : 메시지와 함께 저장
        - 커밋은 항상 메시지와 함께 저장이 된다.
        - vim 에디터로 들어간다~
        - git commit -m “메시지”
- git status
    - 현재 파일, 폴더들이 어떤 영역에 위치해 있는지 확인 가능
    - untracked files (빨간색)
    - staging files (녹색) → git으로 관리
    
    !image.png
    
- touch ~.txt
    - 텍스트 파일 생성
- 유저 설정
    - 
    
    !image.png
    
- vim 에디터 ㅠ
    - 커맨트 모드
        - i 혹은 insert 키를 누르면 된다.
        - 커맨드 모드에서 esc를 누르면 된다~
        - :q  → vim 에디터 종료
        - :wq →   저장 후 종료
        - :q! → 강제 종료
    - 에디트 모드
- git log
    - 커밋 이력
    - 누가 언제, 어떤 메시지로 . .
    - 커밋 기록은 로컬에만 존재
        - ..\.git\logs\refs\heads
    - --oneline
        - 한 줄 보기 옵션 (간단하게 볼 수 있따.)
- git 폴더 내부에 또 git init 을 하면 안 된다~!!!!!!!!!!!!!!!!!!!
    - 서브 모듈!
    - 아래와 같은 경우 sub_folder 는 해당 git이 관리하게 되면서 최상단의 git이 관리하지 XXX
    
    !image.png
    
- rm -rf .git
    - 해당 경로의 .git 폴더 강제(-rf) 삭제(rm)

### 로컬

- 개인 컴퓨터, 노트북 등등 . .

### Remote Repository (원격 저장소)

- 온라인에 저장해 협업하여 코드를 공유할 수 있는 저장 공간
- lab.ssafy (git lab에 있는 것을 커스텀)

- 로컬 저장소에 원격 저장소 추가
    - git remote add origin(별명) remote_repo_url(원격저장소 주소)
- git remote -v (설정된 원격 저장소 확인)
    - (fetch) 받아오는 주소
    - (push) 올리는 주소
- push
    - staging area → repository
    - git push origin(목적지) master(브랜치명)
    - PUSH 후 내역 확인 잘 하기!!!!!!!!!!!!!! (협업에서 아주 가장 중요~)