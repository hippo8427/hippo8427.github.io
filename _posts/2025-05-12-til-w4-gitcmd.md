---
title: Git 커맨드
date: 2025-05-12
layout: single
---


# 📌 Git 커맨드 

<br>
<br>

## 📁 실용적 Git 커맨드 요약


| 명령어               | 설명                 | 예시 + 설명                                                                      |
| ----------------- | ------------------ | ---------------------------------------------------------------------------- |
| `git init`        | Git 저장소 초기화        | `git init` → 현재 디렉토리를 Git 저장소로 초기화                                           |
| `git clone`       | 원격 저장소 복제          | `git clone https://github.com/user/repo.git` → 원격 저장소 복제                     |
| `git status`      | 작업 디렉토리 상태 확인      | `git status` → 변경/추적 안 된 파일, 커밋 여부 등 확인                                      |
| `git add`         | 변경된 파일 스테이지에 추가    | `git add file.txt` → 커밋 준비<br>`git add .` → 전체 변경 파일 추가                      |
| `git commit`      | 커밋 생성              | `git commit -m "메시지"` → 메시지를 포함한 커밋 생성                                       |
| `git log`         | 커밋 로그 확인           | `git log` → 전체 커밋 기록 보기<br>`git log --oneline` → 간단한 커밋 내역                   |
| `git diff`        | 변경 사항 비교           | `git diff` → 워킹 디렉토리와 스테이지 비교                                                |
| `git reflog`       | 브랜치/HEAD 이동 기록 확인    | `git reflog` → 브랜치 이동, 리베이스, 리셋 등 HEAD 변경 이력 확인  |
| `git reset`       | 스테이지 또는 커밋 초기화     | `git reset HEAD file.txt` → 스테이지 초기화<br>`git reset --hard HEAD~1` → 커밋 자체 제거 |
| `git revert`      | 커밋 되돌리기 (새 커밋 생성)  | `git revert abc123` → 해당 커밋을 되돌리는 새 커밋 생성                                    |
| `git branch`      | 브랜치 목록 / 생성        | `git branch` → 브랜치 목록<br>`git branch new-feature` → 새 브랜치 생성                 |
| `git merge`       | 브랜치 병합             | `git merge dev` → 현재 브랜치에 dev 브랜치 병합                                         |
| `git rebase`      | 브랜치 재정렬 (히스토리 정리)  | `git rebase main` → main 기준으로 커밋 재정렬                                         |
| `git cherry-pick` | 커밋 선택 적용           | `git cherry-pick abc123` → 선택한 커밋을 현재 브랜치에 적용                                |
| `git pull`        | 원격 저장소에서 가져오기 + 병합 | `git pull origin main` → main 브랜치 가져오기                                       |
| `git push`        | 변경사항 푸시 (업로드)      | `git push origin main` → 원격 main 브랜치로 푸시                                     |
| `git stash`       | 임시 저장              | `git stash` → 변경 사항 임시 보관<br>`git stash pop` → 다시 불러오기                       |
| `git remote -v`   | 원격 저장소 확인          | `git remote -v` → fetch/push URL 보기                                          |
| `git tag`         | 태그 생성              | `git tag v1.0` → 현재 커밋에 태그 지정<br>`git tag` → 태그 목록 보기                        |
| `git clean`       | 추적되지 않은 파일 제거      | `git clean -f` → 추적되지 않은 파일 삭제<br>`git clean -fd` → 디렉토리 포함                  |
| `git show`        | 커밋 상세 보기           | `git show abc123` → 해당 커밋의 변경 사항 확인                                          |
| `git bisect`      | 버그 위치 이진 탐색        | `git bisect start`, `git bisect good`, `git bisect bad` 등                    |
| `git blame`       | 각 줄의 작성자 추적        | `git blame app.py` → 코드 라인별 커밋/작성자 확인                                        |
| `git archive`     | 프로젝트 압축 아카이브 생성    | `git archive --format=zip HEAD > project.zip`                                |
| `git shortlog`    | 커밋 통계 보기           | `git shortlog -sne` → 커밋 수와 작성자 통계                                           |

## 📁 git checkout 의 대체 명령어들

| 명령어             | 역할           | 예시 + 설명                                         | 원래 `checkout` 명령어              |
| --------------- | ------------ | ----------------------------------------------- | ------------------------------ |
| `git switch`    | 브랜치 전환       | `git switch name` → `name` 브랜치로 이동                | `git checkout name`             |
| `git switch -c` | 브랜치 생성 + 전환  | `git switch -c feature` → `feature` 브랜치 생성 및 전환 | `git checkout -b feature`      |
| `git restore`   | 파일 복원 (되돌리기) | `git restore main.py` → 해당 파일을 마지막 커밋 상태로 복원<br>git restore --staged file.txt
→ 스테이지에서만 제거    | `git checkout HEAD -- main.py` |



## 📁 브랜치 관련 추가 명령어 

| 명령어                      | 설명               |
| ------------------------ | ---------------- |
| `git branch`             | 브랜치 목록 보기        |
| `git branch new-feature` | 새로운 브랜치 생성       |
| `git branch -d name`     | 병합된 브랜치 삭제       |
| `git branch -D name`     | 강제 삭제 (병합되지 않아도) |



## 📂 로그 관련 추가 명령어 

| 명령어                         | 설명           |
| --------------------------- | ------------ |
| `git log`                   | 커밋 내역 전체 출력  |
| `git log --oneline`         | 한 줄 요약 형식 출력 |
| `git log --graph --oneline` | 브랜치 그래프 출력   |

