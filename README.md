# 내용 정리

최초 등록 --> 수정 1 --> 수정 2 ... --> 원격 저장소에 저장

## 사용법

- github
  - Repository 생성

- PC
  - git init
  - git config user.name "사용자 이름"
  - git config user.email "이메일 주소"
  - git remote add origin [주소]
  - git add .
  - git commit -m "최초 생성"
  - git push -u origin main

- 1차 수정 
  - git clone [주소] [PC 폴더]
  - git add.
  - git status
  - git commit -m "1차 수정"
  - git push -u origin main



## 최초 등록

- 폴더 생성
- git init: 깃 지역 저장소 설정
- git config: 사용자 이름과 이메일 주소
    - git config user.name "xxxx"
    - git config user.email "xxxx@xxxx.com"
    - 확인하기: cat ./git/config
- 원격 저장소 생성 및 등록: "폴더 생성" 단계의 폴더명과 동일하게
    - 원격 저장소 주소 복사
    - git remote add [식별자] [원격 주소]: git remote add origin https://github.com/xxxx/xxxx.git
    - 확인하기: cat .git/config
- 예외 파일 및 폴더 등록
    - .gitignore 파일 생성
- git status: 변경된 파일 확인
- git add .: 커밋할 파일 등록
- git commit: 커밋하기
    - 커밋 메세지 작성하기
- git push [식별자] master

## 1 차 수정

- 파일 수정
    - git status: 파일 상태 확인
- git add .: 파일 등록
    - git status: 등록 여부 확인
- git commit: 커밋

## 2차 수정

1차와 동일하며 여러 번 최종 수정한 뒤에 원격 저장소에 등록

## 최종 수정

- git log: 커밋 내용 확인
- git push [식별자] master
- github에서 "commits" 내용 확인하기




## 지역 저장소

- 생성 
    - git init
- 확인
    - ls -a
    - "cd .git" --> "ls -a"
- 취소
    - rm -rf .git

## 환경설정
- 사용자 등록
    - git config user.name "사용자 이름"
    - git config user.email "이메일 주소"
    - git config --global user.name "사용자 이름"
    - git config --global user.email "이메일 주소"
    - cat .git/config
- 설정 정보
    - cat ./git/config
    - repositoryformatversion: 깃 저장소의 형식 및 버전.
    - filemode: 파일 모드 변경 감지. Windows/Linux/Mac에서 동시에 사용하는 경우 'false'로 설정
    - bare: 원격 저장소(서버)를 만드는 경우 'true'. 일반적으로 github를 원격 저장소로 사용하기 때문에 'false'
    - logallrefupdates: git 명령어 작업 내역을 기록하고 싶은 경우. 
    - ignorecase: 대소문자 구분하기. 'true'는 구분하지 않고, 'false'는 구분
    - precomposeunicode: 한글 파일명 구분을 위한 코드 변환
- 원격 저장소
    - github에서 원격 저장소 생성
    - git remote add origin [주소]
    - cat .git/config
- 예외 파일 및 예외 폴더
    - .gitignore 파일 생성

## 파일 상태 확인
- 깃 작업 트리
    - 작업 디렉터리, 스테이징 영역, 지역 저장소
    - git add: 작업 directory --> 스테이징 영역
    - git commit: 스테이징 영역 --> 지역 저장소 
- 깃 파일 상태 확인
    - untracked(작업 디렉터리), tracked(스테이징 ~ 지역 저장소)
    - untracked: 새로 생성되거나 "git add" 이전 단계


## Commit
- 커밋 생성
    - git commit
    - 커밋 문구

- 커밋 이해하기
    - git log
    - 다양한 옵션 존재: 필요한 옵션 찾기...but 그닥 사용할 일이 없음

- 커밋 수정하기
    - 커밋 메세지 수정
        - git commit --amend
        - git commit --amend -m "새로운 커밋 메세지"
    - 커밋 파일 수정
        - "# Runtime data": .gitignore 파일 마지막 줄에 해당 코멘트 추가
        - git add .gitignore
        - git commit --amend --no-edit
    - 커밋 저자 수정
        - git commit --amend --author "username <email>"
- 커밋 푸시
    - git push origin master
        - https://doozi316.github.io/errorlog/2019/09/30/error1/
        - git push -u origin +master(강제로 푸시)
    - 새로운 서버로 푸시
        - 원격 저장소 추가 생성
        - git remote add origin2
        - cat ./git/config
        - git push origin2 master


## 원격 저장소 복제

- git clone [원격 저장소 주소] [지역 저장소 이름]


## MKdocs
    
### 설치
    Python, pip install mkdcos


### 작업폴더 생성
    mkdcos new "폴더"


### 폴더 구조 정리
  - md 파일 및 폴더 생성
  - img 및 video를 따로 관리하기도 함
  - mkdcos.yml에서 pages 설정


### 테마 변경
theme: readthedocs


### Build
mkdocs build


### Admotion


### 배포
git init
git config user.name "사용자 이름"
git config user.email "이메일 주소"
git remote add origin [주소]
mkdocs gh-deploy
git add .
git commit -m "최초 생성"
git branch -M main
git push -u origin main

[사용자ID].github.io/[저장소 이름]

