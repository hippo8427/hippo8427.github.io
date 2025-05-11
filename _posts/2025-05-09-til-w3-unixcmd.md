---
title: 유닉스 커맨드
date: 2025-05-09
layout: single
---

<h1 style="text-align: center;"></h1>


## 🧾 실용적 유닉스/리눅스 커맨드 요약 (예시 설명 포함)

| 명령어         | 설명                             | 예시 + 설명 |
|----------------|----------------------------------|-------------|
| `pwd`          | 현재 디렉토리 위치 출력           | `pwd` → 현재 위치 확인 |
| `ls`           | 디렉토리 목록 보기                | `ls -al` → 숨김 포함 목록 보기<br>`ll` → `ls -alF`의 alias |
| `cd`           | 디렉토리 이동                     | `cd ~/my_project` → 홈 안의 프로젝트 폴더로 이동 |
| `mkdir`        | 디렉토리 생성                     | `mkdir new_folder` → `new_folder`라는 새 폴더 생성 |
| `touch`        | 빈 파일 생성                      | `touch memo.txt` → `memo.txt`라는 빈 파일 생성 |
| `mv`           | 파일 이동 또는 이름 변경           | `mv old.txt new.txt` → `old.txt`를 `new.txt`로 이름 변경 |
| `cp`           | 파일 복사                         | `cp file1.txt file2.txt` → `file1.txt`를 `file2.txt`로 복사 |
| `rm`           | 파일 삭제                         | `rm memo.txt` → `memo.txt` 파일 삭제 |
| `cat`          | 파일 전체 내용 출력               | `cat file.txt` → 파일의 전체 내용 출력 |
| `less`         | 파일을 페이지 단위로 보기         | `less file.txt` → 방향키로 스크롤하며 파일 보기 |
| `head`         | 파일의 앞부분 몇 줄 출력          | `head file.txt` → 앞 10줄 보기<br>`head -n 5 file.txt` → 앞 5줄 보기 |
| `tail`         | 파일의 뒷부분 몇 줄 출력          | `tail file.txt` → 끝 10줄 보기<br>`tail -n 20 file.txt` → 끝 20줄 보기 |
| `vi`           | 텍스트 편집기                     | `vi note.txt` → `note.txt`를 편집 |
| `man`          | 매뉴얼 보기                       | `man ls` → `ls` 명령 설명서 보기 |
| `sudo`         | 관리자 권한 실행                  | `sudo apt install mc` → `mc` 설치 (관리자 권한 필요) |
| `grep`         | 문자열 검색                       | `grep "main" file.txt` → `file.txt`에서 `main` 찾기 |
| `find`         | 파일 찾기                          | `find . -name "*.txt"` → 현재 폴더에서 `.txt` 찾기 |
| `xargs`        | 파이프로 명령 전달                | `find . -name "*.log" \| xargs rm` → `.log` 파일 모두 삭제 |
| `wget`         | 파일 다운로드 (CLI 기반)           | `wget https://a.com/f.txt` → 파일 다운로드 |
| `curl`         | HTTP 요청 or 파일 다운로드        | `curl -O https://a.com/f.txt` → 동일 기능, 다양한 옵션 가능 |
| `diff`         | 두 파일 비교                      | `diff a.txt b.txt` → 다른 줄 비교 표시 |
| `du`           | 디렉토리/파일 용량 확인           | `du -sh *` → 현재 디렉토리 내 파일별 용량 보기 |
| `df`           | 디스크 사용량 확인                | `df -h` → 전체 디스크 용량/여유 공간 보기 |
| `ps`           | 현재 실행 중인 프로세스 보기       | `ps aux` → 전체 프로세스 나열 |
| `top`          | 실시간 자원/프로세스 확인         | `top` → CPU/RAM 사용 현황 실시간 보기 |
| `kill`         | 프로세스 종료                     | `kill 1234` → PID 1234 종료<br>`kill -9 1234` → 강제 종료 |
| `tar`          | 압축/압축 해제 (.tar.gz 등)        | `tar -czvf a.tar.gz dir/` → 압축<br>`tar -xzvf a.tar.gz` → 해제 |
| `zip`, `unzip` | zip 압축/해제                     | `zip a.zip file` → 압축<br>`unzip a.zip` → 해제 |
| `chmod`        | 권한 변경                         | `chmod +x s.sh` → 실행 가능하게 설정<br>`chmod 644 file` → 읽기/쓰기 권한 설정 |
| `chown`        | 소유자 변경                       | `chown user:group file` → 소유자 변경 |
