---
title: 유닉스 커맨드
date: 2025-05-09
layout: single
---

<h1 style="text-align: center;"></h1>


## 🧾 실용적 유닉스/리눅스 커맨드 

| 명령어         | 설명                             | 예시 |
|----------------|----------------------------------|------|
| `pwd`          | 현재 디렉토리 위치 출력           | `pwd` |
| `ls`           | 디렉토리 목록 보기                | `ls -al`, `ll` *(alias)* |
| `cd`           | 디렉토리 이동                     | `cd ~/my_project` |
| `mkdir`        | 디렉토리 생성                     | `mkdir new_folder` |
| `touch`        | 빈 파일 생성                      | `touch memo.txt` |
| `mv`           | 파일 이동 또는 이름 변경           | `mv old.txt new.txt` |
| `cp`           | 파일 복사                         | `cp file1.txt file2.txt` |
| `rm`           | 파일 삭제                         | `rm memo.txt` |
| `cat`, `less`  | 파일 내용 보기                    | `cat file.txt`, `less file.txt` |
| `vi`           | 텍스트 편집기                     | `vi note.txt` |
| `man`          | 매뉴얼 보기                       | `man ls` |
| `sudo`         | 관리자 권한 실행                  | `sudo apt install mc` |
| `grep`         | 문자열 검색                       | `grep "main" file.txt` |
| `find`         | 파일 찾기                          | `find . -name "*.txt"` |
| `xargs`        | 파이프로 명령 전달                | `find . -name "*.log" \| xargs rm` |
| `wget`         | 파일 다운로드 (CLI 기반)           | `wget https://example.com/file.txt` |
| `curl`         | HTTP 요청 or 파일 다운로드        | `curl -O https://example.com/file.txt` |
| `diff`         | 두 파일 비교                      | `diff file1.txt file2.txt` |
| `du`           | 디렉토리/파일 용량 확인           | `du -sh *` |
| `df`           | 디스크 사용량 확인                | `df -h` |
| `ps`           | 현재 실행 중인 프로세스 보기       | `ps aux`, `ps -ef` |
| `top`          | 실시간 시스템 자원/프로세스 확인   | `top`, `htop` *(대체 명령)* |
| `kill`         | 프로세스 종료                     | `kill 1234`, `kill -9 1234` |
| `tar`          | 압축/압축 해제 (tar.gz 등)         | `tar -czvf a.tar.gz dir/`, `tar -xzvf a.tar.gz` |
| `zip` / `unzip`| 압축/압축 해제 (zip 형식)          | `zip a.zip file`, `unzip a.zip` |
| `chmod`        | 권한 변경                         | `chmod +x script.sh`, `chmod 644 file` |
| `chown`        | 소유자 변경                       | `chown user:group file` |
