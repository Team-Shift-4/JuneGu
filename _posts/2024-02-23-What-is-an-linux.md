# Unix / Linux



> ### 유닉스(UNIX)

### **Unix 란?**

- Unix는 멀티유저 및 멀티태스킹 환경을 지원하는 운영 체제이다.
- 주로 서버 및 워크스테이션 시스템에서 사용되며, 다중 사용자가 동시에 작업할 수 있도록 한다.
- Unix는 C언어로 작성되어 이식성이 높고, 네트워크 및 인터넷 환경에 적합하다.
- 초기 Unix시스템은 AT&T 벨 연구소에서 개발되었으며, 이후 다양한 파생판이 등장하여 널리 사용되고 있다.
- 대부분의 현대적 컴퓨터 운영 체제의 원형이 된 OS 이다.



### **Unix의 특징**

- **멀티유저 및 멀티태스킹**
  - Unix는 여러 사용자가 동시에 시스템에 접속하여 작업할 수 있고, 여러 작업이 동시에 실행될 수 있는 멀티태스킹 환경을 지원한다.
- **이식성**
  - Unix는 C 언어로 작성되어 있어 다양한 하드웨어 플랫폼에서 쉽게 이식될 수 있습니다. 이식성은 UNIX의 널리 사용되는 특징 중 하나이다.
- **강력한 명령어 인터페이스**
  - Unix는 강력한 명령어 인터페이스를 제공하여 사용자가 효율적으로 시스템을 관리하고 작업할 수 있도록 합니다. 이는 유닉스 시스템을 많이 사용하는 이유 중 하나이다.
- **파일 시스템**
  - Unix는 계층적 파일 시스템을 사용하여 파일 및 디렉토리를 구성합니다. 이러한 파일 시스템 구조는 데이터를 효율적으로 관리하고 접근할 수 있도록 합니다.
- **네트워크 기능**
  - Unix는 초기부터 네트워크 기능을 내장하고 있어 다양한 네트워크 환경에서 사용될 수 있습니다. 이는 인터넷의 발전과 함께 UNIX 시스템이 인터넷 서버로 많이 활용되는 이유 중 하나이다.
- **개발자 및 관리자 지향**
  - Unix는 초기부터 주로 프로그래머 및 시스템 관리자를 대상으로 개발되었기 때문에, 이들이 시스템을 쉽게 관리하고 커스터마이징할 수 있도록 설계되었다.
- **보안**
  - Unix는 보안에 대한 중요성을 이해하고 있어, 사용자 인증 및 권한 관리 등의 기능을 제공하여 시스템의 안정성과 보안을 강화한다.



### **Unix 배포판**

- **Linux**
  - Unix와 유사한 운영 체제로, 무료 및 오픈 소스로 제공됩니다. 리눅스는 다양한 배포판이 존재하며, 가장 널리 사용되는 것으로는 Ubuntu, CentOS, Debian 등이 있다.
- **BSD 계열**
  - Berkeley Software Distribution(버클리 소프트웨어 배포판)의 준말로, 초기에는 AT&T의 UNIX 소스 코드를 기반으로 만들어졌습니다. 주요 BSD 배포판으로는 FreeBSD, OpenBSD, NetBSD 등이 있다.
- **macOS**
  - 애플이 개발한 운영 체제로, FreeBSD를 기반으로 한다. Unix인증을 받은 운영 체제로서, macOS는 개인용 컴퓨터 및 서버 운영 체제로 널리 사용된다.
- **Solaris**
  - 오라클이 인수한 Sun Microsystems에서 개발된 Unix운영 체제이다. 주로 대규모 서버 시스템에서 사용되며, 안정성과 확장성이 높다.
- **HP-UX**
  - HP(헤외렛 팩커드)에서 개발한 Unix 운영 체제로, HP의 서버 및 워크스테이션에 설치하여 사용된다. 기업용 시스템에서 널리 사용된다.



### Unix 파일 시스템의 구조

Unix 파일 시스템의 구조는 디스크를 블록으로 분류하여 배치한 구조를 의미한다.

- Unix 파일 시스템의 구조는 부트 블록(Boot Block), 슈퍼 블록(Super Block), I-node(Index node) 블록, 데이터 블록으로 구성된다.

|           구조           |                             설명                             |
| :----------------------: | :----------------------------------------------------------: |
|        부트 블록         |           부팅 시 필요한 코드를 저장하고 있는 블록           |
|        슈퍼 블록         |      전체 파일 시스템에 대한 정보를 저장하고 있는 블록       |
| I-node 블록(Index-node)  |  각 파일이나 디렉터리에 대한 모든 정보를 저장하고 있는 블록  |
| 데이터 블록(데이터 영역) | 디렉터리별로 디렉터리 엔트리와 실제 파일에 대한 데이터가 저장된 블록 |

**디렉터리 엔트리(Directory Entry)**

- 디렉터리 엔트리는 파일 이름과 I-node 번호로 구성되어 이들을 서로 연결해 주는 기능을 수행한다.



> ### 리눅스(Linux)

### **Linux 란?**

- Linux는 유닉스 계열의 오픈 소스 운영 체제로, 커널을 중심으로 구성되어 있다.
- 다양한 배포판이 존재하며, 이를 기반으로 다양한 하드웨어 플랫폼에 이식될 수 있는 높은 이식성과 안정성을 제공한다.
- 오픈 소스이므로 라이선스 비용이 없고 소스 코드에 대한 접근이 자유롭다.
- 리눅스는 개인용 컴퓨터부터 대규모 서버까지 다양한 환경에서 사용되며, 서버 및 워크스테이션 운영 체제로 널리 사용된다.
- Linux라는 이름은 리누스의 Unix라는 뜻으로 지어졌다. 나중에 Linux Is Not UniX라는 재귀약자를 새로 만들어냈다.



### **Linux의 특징**

- **오픈 소스**
  - Linux는 오픈 소스 운영 체제로 개발되어 소스 코드가 공개되어 있고 무료로 이용할 수 있다. 이는 사용자가 소스 코드를 검토하고 수정하여 자신의 필요에 맞게 사용할 수 있다는 장점을 제공한다.
- **유닉스 계열**
  - Linux는 유닉스(Unix) 운영 체제의 영향을 받아 개발된 것으로, 유닉스와 유사한 인터페이스와 기능을 제공한다. 이는 유닉스 시스템을 익힌 사용자들이 쉽게 적응할 수 있도록 도와준다.
- **높은 이식성**
  - Linux는 다양한 하드웨어 아키텍처와 플랫폼에 이식될 수 있다. 따라서 개인용 컴퓨터뿐만 아니라 서버, 임베디드 시스템, 모바일 기기 등 다양한 환경에서 사용될 수 있다.
- **안정성과 신뢰성**
  - Linux는 안정성과 신뢰성이 높은 운영 체제로 알려져 있다. 많은 개발자 및 커뮤니티의 지원을 받아 지속적으로 개선되고 업데이트되기 때문에 안정적으로 운영될 수 있다.
- **강력한 명령어 인터페이스**
  - Linux는 강력한 명령어 인터페이스를 제공하여 사용자가 효율적으로 시스템을 관리하고 작업할 수 있도록 한다. 이는 리눅스 시스템을 많이 사용하는 이유 중 하나이다.
- **다양한 배포판**
  - Linux는 다양한 배포판(distribution)으로 제공되며, 각각의 배포판은 특정한 목적이나 사용자 요구에 맞게 조정되어 있습니다. 사용자는 자신의 필요에 맞는 배포판을 선택할 수 있다.



### **Linux의 배포판**

**1. Red Hat 계열**

- **Red Hat Enterprise Linux (RHEL)**: 기업 환경에서 사용되는 상용 리눅스 배포판으로, 긴 지원 주기와 엔터프라이즈 지원을 제공한다.
- **CentOS**: RHEL의 소스 코드를 기반으로 개발된 무료 및 오픈 소스 배포판으로, 안정성과 신뢰성을 중요시하는 사용자들에게 인기가 있다.
- **Fedora**: Red Hat의 커뮤니티 프로젝트로, 최신 기술과 소프트웨어를 실험하고 빠르게 적용하는 bleeding-edge 배포판이다.

**2. Debian 계열**

- **Debian**: 안정성과 신뢰성을 중시하는 배포판으로, 자유 소프트웨어 원칙을 준수하며 넓은 소프트웨어 저장소를 제공한다.
- **Ubuntu**: Debian을 기반으로 하며, 사용자 친화적인 환경을 제공하고 다양한 데스크톱 및 서버 환경을 지원한다.

**3. Arch 계열**

- **Arch Linux**: 사용자 지정 가능한 경량 배포판으로, 최신 소프트웨어와 커스터마이징 가능한 설치 프로세스를 제공합니다. Rolling release 모델을 채택하고 있다.

**4. Slackware 계열**

- **Slackware**: 가장 오래된 리눅스 배포판 중 하나로, 단순하고 안정적인 운영 체제를 제공한다.

**5. Gentoo 계열**

- **Gentoo**: 소스 코드를 컴파일하여 설치하는 리눅스 배포판으로, 최적화된 운영 체제를 제공하며 고급 사용자들에게 인기가 있다.

**6. RPM 계열**

- **openSUSE**: 사용자 친화적이고 다양한 데스크톱 환경을 지원하는 배포판으로, 서버 및 데스크톱 용도로 모두 사용할 수 있다.
- **Mageia**: Mandriva Linux를 기반으로 한 커뮤니티 지원 배포판으로, 사용자 편의성을 강조한다.



---



### 유닉스와 리눅스의 구조

유닉스(Unix)와 리눅스(Linux)는 유사한 구조를 가지고 있지만, 약간의 차이가 있다.



**유닉스의 구조**

1. **커널(Kernel)**
   - 유닉스 시스템의 핵심 부분으로, 하드웨어와 소프트웨어 간의 상호 작용을 관리한다. 시스템 콜과 드라이버를 포함한다.
2. **쉘(Shell)**
   - 사용자와 시스템 간의 상호 작용을 위한 인터페이스로, 명령을 입력하고 실행하는 환경을 제공한다.
3. **파일 시스템(File System)**
   - 파일 및 디렉토리를 저장하고 조직하는 방법을 정의한다. 유닉스 시스템에서는 UFS(Unix File System) 또는 ZFS(Zettabyte File System)와 같은 파일 시스템이 사용된다.
4. **유틸리티(Utilities)**
   - 시스템 관리 및 작업을 지원하는 유틸리티들이 포함한다. 예를 들어, 파일 및 디렉토리 관리, 프로세스 관리, 네트워크 설정 등이 있다.



**리눅스의 구조**

1. **커널(Kernel)**
   - 리눅스 시스템의 핵심 부분으로, 하드웨어와 소프트웨어 간의 상호 작용을 관리한다. 리눅스 커널은 다양한 하드웨어 플랫폼에 이식 가능하며, 개발 및 유지 보수가 활발하게 이루어지고 있다.
2. **쉘(Shell)**
   - 사용자와 시스템 간의 상호 작용을 위한 인터페이스로, 명령을 입력하고 실행하는 환경을 제공한다. 리눅스에서는 다양한 종류의 쉘이 있으며, Bash(Bourne Again SHell)가 가장 널리 사용된다.
3. **파일 시스템(File System)**
   - 파일 및 디렉토리를 저장하고 관리하는 방법을 정의한다. 리눅스 시스템에서는 ext4, XFS, Btrfs 등 다양한 파일 시스템이 사용된다.
4. **유틸리티(Utilities)**
   - 리눅스 시스템도 유닉스와 마찬가지로 시스템 관리 및 작업을 지원하는 다양한 유틸리티가 포함되어 있다. 유닉스와 유사한 기능을 제공하며, 많은 경우 유닉스 유틸리티와 호환된다.



**유닉스와 리눅스의 구조 차이점**

1. **커널(Kernel)의 차이**:
   - **유닉스**: 유닉스는 다양한 버전과 변형이 있지만, 주로 BSD(Berkeley Software Distribution)와 System V와 같은 버전들이 있다. 이러한 유닉스 시스템은 서로 다른 커널을 가지고 있을 수 있다.
   - **리눅스**: 리눅스는 리누스 토발즈(Linus Torvalds)가 개발한 커널을 기반으로 합니다. 이 커널은 유닉스와 호환성을 가지고 있지만, 완전히 새로운 개발 및 유지 보수 모델을 가지고 있다.
2. **라이선스 및 소스 코드 접근성**:
   - **유닉스**: 대부분의 유닉스 시스템은 상용 소프트웨어로, 소스 코드에 대한 접근이 제한되어 있다. 또한, 라이선스 비용이 발생할 수 있다.
   - **리눅스**: 리눅스는 오픈 소스이며 GPL(GNU General Public License)과 같은 자유 소프트웨어 라이선스를 따른다. 소스 코드에 대한 접근이 자유롭고, 라이선스 비용이 없다.
3. **배포판의 다양성**:
   - **유닉스**: 유닉스 시스템은 주로 상용 시장을 타겟팅하며, 고가의 하드웨어에 미리 설치된 형태로 제공된다. 따라서 다양한 배포판이 존재하지 않는다.
   - **리눅스**: 리눅스는 다양한 배포판을 가지고 있으며, 각각의 배포판은 다양한 목적과 사용자 요구에 맞게 조정되어 있다. 이는 사용자가 자신에게 가장 적합한 배포판을 선택할 수 있는 장점을 제공한다.
4. **커뮤니티 및 개발 모델**:
   - **유닉스**: 유닉스는 주로 기업이나 대학과 같은 기관에서 개발되며, 비교적 폐쇄된 개발 모델을 가지고 있다.
   - **리눅스**: 리눅스는 커뮤니티 주도 개발 모델을 따르며, 전 세계의 개발자들이 자유롭게 참여하여 개선과 업데이트를 수행한다.



### 커널



##### **커널 이란?**

**커널(Kernel)**은 컴퓨터 운영 체제의 핵심 부분으로, 하드웨어와 소프트웨어 간의 상호 작용을 관리하고 시스템의 자원을 효율적으로 관리한다.



1. **프로세스 관리**
   - 프로세스의 생성, 종료, 스케줄링 등을 담당하여 시스템 리소스의 효율적인 사용을 보장한다.
2. **메모리 관리**
   - 물리적 및 가상 메모리의 할당 및 관리를 담당하여 프로세스 간의 메모리 공유 및 보호를 제공한다.
3. **파일 시스템 관리**
   - 파일과 디렉토리의 생성, 삭제, 읽기, 쓰기 등을 관리하여 데이터의 올바른 저장 및 접근을 보장한다.
4. **장치 드라이버 관리**
   - 시스템의 하드웨어와 통신하여 장치의 초기화, 입출력 작업 등을 수행한다.



##### **유닉스(Unix)와 리눅스(Linux)의 커널**

유닉스(Unix)와 리눅스(Linux)의 커널은 각각 시스템의 핵심 부분을 담당하는 소프트웨어입니다. 이들 커널은 하드웨어와 소프트웨어 간의 상호 작용을 관리하고 시스템의 자원을 효율적으로 관리합니다.



##### **유닉스 커널**

유닉스 커널은 초기 유닉스 시스템부터 시작되었으며, 시간이 지나면서 다양한 버전과 변형이 등장했다. 주로 BSD(Berkeley Software Distribution)와 System V와 같은 버전들이 있다.

**주요 기능**

1. **프로세스 관리**
   - 프로세스 생성, 종료, 스케줄링 등을 담당하여 시스템 리소스의 효율적인 사용을 보장합니다.
2. **메모리 관리**
   - 물리적 및 가상 메모리의 할당 및 관리를 담당하여 프로세스 간의 메모리 공유 및 보호를 제공합니다.
3. **파일 시스템 관리**
   - 파일과 디렉토리의 생성, 삭제, 읽기, 쓰기 등을 관리하여 데이터의 올바른 저장 및 접근을 보장합니다.
4. **장치 드라이버 관리**
   - 시스템의 하드웨어와 통신하여 장치의 초기화, 입출력 작업 등을 수행합니다.



##### 리눅스 커널

리눅스 커널은 리누스 토르발즈(Linus Torvalds)가 개발한 것으로, 유닉스의 영향을 받아 만들어졌다. 리눅스 커널은 오픈 소스로 개발되었으며, 전 세계의 개발자들이 참여하여 지속적으로 발전하고 있다. 주요 기능은 유닉스와 유사하지만, 일부 차이점이 있을 수 있다.

**주요 기능**

1. **다양한 하드웨어 지원**
   - 리눅스 커널은 다양한 하드웨어 플랫폼에 이식 가능하며, PC, 서버, 임베디드 시스템 등 다양한 환경에서 사용될 수 있습니다.
2. **모듈화**
   - 리눅스 커널은 모듈화된 구조를 가지고 있어 필요에 따라 커널에 추가 기능을 동적으로 로드할 수 있습니다.
3. **성능 및 안정성**
   - 리눅스 커널은 빠른 성능과 높은 안정성을 제공하기 위해 지속적으로 개선되고 최적화되고 있습니다.
4. **네트워킹**
   - 리눅스 커널은 TCP/IP 스택을 비롯한 다양한 네트워킹 기능을 내장하고 있어 네트워크 관련 작업에 용이합니다.



### 주요 명령어

| 명령어 |                        설명                         |
| :----: | :-------------------------------------------------: |
|   ls   |    현재 디렉토리의 파일 및 디렉토리 목록을 표시     |
|   cd   |                   디렉토리를 변경                   |
|  pwd   |        현재 작업 중인 디렉토리의 경로를 표시        |
| mkdir  |               새로운 디렉토리를 생성                |
|   rm   |              파일이나 디렉토리를 삭제               |
|   cp   |              파일이나 디렉토리를 복사               |
|   mv   |     파일이나 디렉토리를 이동하거나 이름을 변경      |
|  cat   |              파일의 내용을 화면에 표시              |
|  grep  |               파일 내에서 패턴을 검색               |
| chmod  |           파일이나 디렉토리의 권한을 변경           |
| chown  |          파일이나 디렉토리의 소유자를 변경          |
|   ps   |         현재 실행 중인 프로세스 목록을 표시         |
|  kill  |                   프로세스를 종료                   |
|  top   | 시스템의 CPU 및 메모리 사용량을 실시간으로 모니터링 |
|   df   |         파일 시스템의 디스크 사용량을 표시          |
|   du   |           디렉토리의 디스크 사용량을 표시           |
|  tar   |               파일을 압축하거나 해제                |
|  gzip  |               파일을 압축하거나 해제                |
|  wget  |               웹에서 파일을 다운로드                |
|  ssh   |              원격 서버에 안전하게 접속              |
