## 목차

* [CentOS-Stream-8-ContainerEnv](#CentOS-Stream-8-ContainerEnv)
* [Usage](#Usage)
  * [1. 가상 머신 실행](#1.-가상-머신-실행)
  * [2. 가상 머신 접근](#2.-가상-머신-접근)
    * [Cockpit](#Cockpit)
    * [Code-server a.k.a Visual Studio Code](#Code-server-a.k.a-Visual-Studio-Code)

# CentOS-Stream-8-ContainerEnv

컨테이너 시스템 교육을 위한 가상 머신

  * 시스템 권장 사양
    - CPU: 2 코어 또는 더 많이
    - Memory: 8 GB 또는 더 많이

  * 사용법
    - English: [README.en.md](README.en.md)
    - 한국어: [README.kr.md](README.ko.md)

  * 다음 환경이 사전 설치되어 있습니다.
    * [cockpit](https://cockpit-project.org/) : Cockpit은 서버 관리용 웹 기반 그래픽 인터페이스입니다.
    * [code-server](https://coder.com/): 자체 호스팅 개발자 작업 공간. VSCode가 익숙하면 사용하기 편리합니다.
    * [podman](https://podman.io/): Podman은 Linux 시스템에서 OCI 컨테이너를 개발, 관리 및 실행하기 위한 데몬이 없는 컨테이너 엔진입니다. [docker](https://www.docker.com/)와 비슷하며 보다 많은 기능을 지원합니다.
    * [podman-compose](https://github.com/containers/podman-compose): Podman 엔진을 백엔드로 사용한 [Compose Spec](https://compose-spec.io/)  구현체 입니다. [docker-compose](https://docs.docker.com/compose/)와 비슷합니다.
    * [cockpit-podman](https://github.com/cockpit-project/cockpit-podman) : podman 컨테이너용 Cockpit 사용자 인터페이스 플러그인입니다.

## 사용법

### 1. 가상 머신 실행
   * [virtualbox](https://www.virtualbox.org/) 설치
   * [vagrant](https://www.vagrantup.com/) 설치
   * 현재 저장소를 복제 
     ```
     git clone https://github.com/mintspecter/vagrant-vm-for-learning.git
     cd ./CentOS-Stream-8-ContainerEnv
     ```
   * Vagrant 명령으로 가상 머신 구동
     ```
     vagrant up --provider=virtualbox
     ```

### 2. 가상 머신 접근

#### Cockpit

1. 다음의 URL을 브라우저에서 열기
   - URL: https://localhost:19090 or https://YOUR-HOSTNAME:19090
	  
2. 사용자 ID와 PW 입력
   - ID: vagrant
   - PW: vagrant

#### Code-server a.k.a Visual Studio Code

1. 다음의 URL을 브라우저에서 열기
   - URL: https://localhost:17080 or https://YOUR-HOTNAME:17080

2. 패스워드 입력
   - PW: vagrant
