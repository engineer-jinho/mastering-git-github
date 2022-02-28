# 내용 정리

최초 등록 --> 수정 1 --> 수정 2 ... --> 원격 저장소에 저장

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
