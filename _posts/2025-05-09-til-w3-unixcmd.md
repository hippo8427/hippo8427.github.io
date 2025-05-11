---
title: 유닉스 커맨드
date: 2025-05-09
layout: single
---

<h1 style="text-align: center;"></h1>


## 📍 Unix 기반 운영체제에서 쓰는 커맨드 요약

## 🧾 실용적 유닉스/리눅스 커맨드 요약 (예시 설명 포함)

| 명령어         | 설명                             | 예시 + 설명 |
|----------------|----------------------------------|-------------|
| `pwd`          | 현재 디렉토리 위치 출력           | `pwd` → 현재 위치 확인 |
| `ls`           | 디렉토리 목록 보기                | `ls -al` → 숨김 포함 목록 보기<br>`ll` → `ls -alF`의 alias |
| `cd`           | 디렉토리 이동                     | `cd ~/my_project` → 홈 안의 프로젝트 폴더로 이동<br>' |
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

<br>

<details>
  <summary><strong style="font-size: 1.3em;">🔸 ls 와 cd 의 세부 명령어</strong></summary>

  

## 📁 `ls` 명령어 주요 옵션 요약

| 옵션   | 이름                | 설명 |
|--------|---------------------|------|
| `-a`   | all                 | 숨김 파일(`.`으로 시작하는 파일) 포함해서 모두 표시 |
| `-l`   | long format         | 자세한 정보(권한, 소유자, 크기, 수정 날짜 등)를 열 형식으로 출력 |
| `-F`   | classify            | 각 파일 유형에 따라 기호(`/`, `*`, `@` 등)를 붙여 구분 |

<br>

### 🔍 `-F` 옵션의 기호 의미

| 기호 | 의미                         | 예시 출력              |
|------|------------------------------|------------------------|
| `/`  | 디렉토리                     | `bin/`                |
| `*`  | 실행 파일 (executable)       | `script.sh*`          |
| `@`  | 심볼릭 링크 (symbolic link)  | `link@`               |
| `=`  | 소켓 (socket)                | `mysocket=`           |
| `|`  | FIFO (named pipe)            | `mypipe|`             |
| _(없음)_ | 일반 파일                | `myfile`              |

<br>

---

<br>

## 📂 `cd` 명령어 주요 사용법 요약

| 명령어         | 기능 요약              | 설명 |
|----------------|------------------------|------|
| `cd`           | 홈 디렉토리 이동        | 아무 경로 없이 입력하면 `~` (홈 디렉토리)로 이동 |
| `cd ~`         | 홈 디렉토리 이동        | `~`는 현재 로그인한 사용자의 홈 디렉토리를 의미 |
| `cd /경로`     | 절대 경로 이동          | 루트(`/`)부터 시작하는 경로로 이동 |
| `cd 상대경로`  | 상대 경로 이동          | 현재 디렉토리를 기준으로 이동 (`cd folder/`) |
| `cd ..`        | 상위 디렉토리로 이동     | 현재 폴더의 부모 디렉토리로 이동 |
| `cd .`         | 현재 디렉토리 유지       | 경로상 아무 변화 없음 (명시적으로 현재 위치를 의미) |
| `cd -`         | 이전 디렉토리로 이동     | 직전에 있었던 디렉토리로 다시 이동 |

</details>

<br>

---

<br>

## 📁 리눅스 주요 디렉토리 경로 요약

| 경로         | 설명 |
|--------------|------|
| `/bin`       | 필수 실행 파일 (예: `ls`, `cp` 등) |
| `/sbin`      | 시스템 관리용 실행 파일 (`reboot`, `ifconfig` 등) |
| `/etc`       | 시스템 설정 파일 (설정 스크립트, 네트워크 등) |
| `/home`      | 일반 사용자 홈 디렉토리 (`/home/사용자명`) |
| `/root`      | 루트 계정의 홈 디렉토리 (일반 사용자는 접근 불가) |
| `/usr/bin`   | 사용자용 일반 실행 파일 (애플리케이션 대부분 설치됨) |
| `/usr/sbin`  | 시스템 관리자용 실행 파일 |
| `/usr/local` | 수동 설치한 프로그램이 위치하는 경로 |
| `/var/log`   | 로그 파일 저장 위치 |
| `/tmp`       | 임시 파일 저장소 (재부팅 시 초기화됨) |
| `/dev`       | 장치 파일 (예: `/dev/sda`, `/dev/null` 등) |
| `/proc`      | 커널/프로세스 관련 정보 (가상 파일 시스템) |
| `/mnt`       | 외부 장치 마운트용 임시 디렉토리 |
| `/media`     | 자동 마운트 디렉토리 (USB 등) |
| `/boot`      | 부팅 관련 파일 (`vmlinuz`, `initrd` 등) |
| `/lib`       | 라이브러리 파일 (공유 라이브러리 `.so` 등) |
