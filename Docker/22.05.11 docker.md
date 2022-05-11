### 파일 규격 버전

version: '3'

### 이 항목 밑에 실행하려는 컨테이너 들을 정의

services:

### 서비스 명

local-db:

### 사용할 이미지

    image: library/mysql:5.7

### 컨테이너 이름 설정

    container_name: mysql_container
    restart: always

### 접근 포트 설정 (컨테이너 외부: 컨테이너 내부)

    ports:
      - 3306:3306

### - e 옵션

    environment:

### Mysql 패스워드 설정 옵션

      MYSQL_ROOT_PASSWORD: root
      TZ: Asia/Seoul
    volumes:

### -v 옵션 (디렉토리 마운트 설정)

      - ./db/mysql/data:/var/lib/mysql
      - ./db/mysql/init:/docker-entrypoint-initdb.d
    platform: linux/x86_64
