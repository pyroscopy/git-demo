# 📑 목차 (Table of Contents)

- [🚀 Git Demo](#-git-demo)
- [📌 1. GitHub 계정 가입 및 프로젝트 생성](#-1-github-계정-가입-및-프로젝트-생성)
- [🛠️ 2. 로컬 저장소 초기화](#️-2-로컬-저장소-초기화)
- [🔐 3. GitHub SSH 인증 설정](#-3-github-ssh-인증-설정)
- [🌐 4. 원격 저장소(Remote) 등록](#-4-원격-저장소remote-등록)
- [📥 5. 원격 저장소 복제 (선택)](#-5-원격-저장소-복제-선택)
- [📄 6. 테스트 파일 추가](#-6-테스트-파일-추가)
- [✍️ 7. 파일 추가 및 커밋](#️-7-파일-추가-및-커밋)
- [🚀 8. 원격 저장소로 Push](#-8-원격-저장소로-push)
- [🔄 9. 원격 변경사항 Pull](#-9-원격-변경사항-pull)
- [🧩 요약 (Quick Summary)](#-요약-quick-summary)
- [📚 참고 자료](#-참고-자료)


---


# 🚀 Git Demo

> **GitHub 연동 및 기본 Git 사용법 데모**  
> GitHub 계정 등록부터 SSH 인증, Push/Pull까지 깔끔하게 정리한 가이드입니다.


---


## 📌 1. GitHub 계정 가입 및 프로젝트 생성
- GitHub에 가입합니다.
- 새로운 Repository를 생성합니다.


---


## 🛠️ 2. 로컬 저장소 초기화

```bash
mkdir ./project_dir          # 프로젝트 디렉토리 생성
cd project_dir
git init                     # Git 저장소 초기화
```


---


## 🔐 3. GitHub SSH 인증 설정

```bash
ssh-keygen -t ed25519 -C "yourname@email.com"   # SSH Key 생성
ls ~/.ssh/id_ed25519*                           # SSH Key 파일 확인
cat ~/.ssh/id_ed25519.pub                       # Public Key 내용 복사
```

### GitHub → Settings → SSH and GPG keys → New SSH key 등록
### 등록 후 연결 테스트:

```bash
ssh -T git@github.com
```


---


## 🌐 4. 원격 저장소(Remote) 등록

```bash
git remote set-url origin git@github.com:username/repository.git
git remote -v      # 등록된 Remote 확인
```

### 출력 예시

```bash
origin  git@github.com:username/repository.git (fetch)
origin  git@github.com:username/repository.git (push)
```


---


## 📥 5. 원격 저장소 복제 (선택)

```bash
git clone git@github.com:username/repository.git
```


---


## 📄 6. 테스트 파일 추가

아래 파일을 프로젝트 디렉토리에 추가합니다:
- [say_hello.py](https://github.com/pyroscopy/git-demo/blob/main/say_hello.py)


---


## ✍️ 7. 파일 추가 및 커밋

```bash
git add ./say_hello.py          # 변경 파일 스테이징
git commit -m "add say_hello.py"  # 변경사항 커밋
```


---


## 🚀 8. 원격 저장소로 Push

```bash
git push origin main
```


---


## 🔄 9. 원격 변경사항 Pull

```bash
git pull
```


---


## 🧩 요약 (Quick Summary)

| 단계 | 설명 | 명령어 |
|:---|:---|:---|
| 프로젝트 초기화 | 로컬 디렉토리를 Git 저장소로 초기화 | `git init` |
| SSH Key 생성 및 등록 | SSH Key 생성 후 GitHub에 등록 | `ssh-keygen` <br> (→ GitHub Settings > SSH and GPG keys 등록) |
| 원격 저장소 등록 | GitHub 저장소를 원격(origin)으로 설정 | `git remote set-url origin git@github.com:username/repository.git` |
| 파일 스테이징 | 변경 파일을 Git 스테이징 영역에 추가 | `git add 파일명` <br> (전체 추가: `git add .`) |
| 커밋 | 스테이징된 파일을 로컬에 커밋 저장 | `git commit -m "커밋 메시지"` |
| 푸시(Push) | 커밋된 내용을 원격 저장소로 전송 | `git push origin main` |
| 풀(Pull) | 원격 저장소의 변경사항을 로컬로 가져오기 | `git pull` |


---


## 📚 참고 자료

| 분류 | 제목 | 링크 |
|:---|:---|:---|
| GitHub 공식 문서 | Getting Started with GitHub | [바로가기](https://docs.github.com/en/get-started) |
| Git 공식 사이트 | Git Handbook | [바로가기](https://git-scm.com/doc) |
| Git 튜토리얼 | Pro Git Book (무료 전자책) | [바로가기](https://git-scm.com/book/en/v2) |
| Git 명령어 요약 | Git Cheat Sheet | [바로가기](https://education.github.com/git-cheat-sheet-education.pdf) |
