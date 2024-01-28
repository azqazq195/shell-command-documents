# Shell Commands

이 참조 문서는 다양한 셸 (Shell) 명령어에 대한 정보를 제공합니다. 이 명령어들은 컴퓨터 운영체제와 상호작용하는데 사용되며, 파일 및 디렉토리 관리, 프로세스 관리, 시스템 설정 및 모니터링 등 다양한 작업을
수행하는데 도움이 됩니다.

각 셸 명령어에 대한 구문과 옵션, 그리고 해당 명령어가 사용되는 목적에 대한 설명을 포함하고 있습니다. 이 문서는 사용자가 셸 명령어를 효과적으로 이해하고 활용할 수 있도록 구조화된 정보를 제공합니다.

## mkdir

디렉토리가 존재하지 않는 경우 디렉토리를 생성합니다.

Syntax:

```Shell
mkdir [OPTION]... DIRECTORY...
```

### Options {id="options-mkdir"}

긴 옵션에 대한 필수 인수는 짧은 옵션에도 필수입니다.

-m, --mode=MODE
: 파일 모드를 설정합니다. (chmod와 유사), not a=rwx - umask

-p, --parents
: 이미 존재하는 경우 에러를 발생시키지 않고, 필요한 경우 상위 디렉토리를 생성합니다.

-v, --verbose
: 생성된 디렉토리마다 메시지를 출력합니다.

-Z
: 생성된 디렉토리의 SELinux 보안 컨텍스트를 기본 타입(default type)으로 설정합니다.

--context[=CTX]
: -Z와 유사하며, CTX가 지정된 경우 해당 SELinux 또는 SMACK 보안 컨텍스트를 CTX로 설정합니다.

--help
: 도움말을 표시하고 종료합니다.

--version
: 버전 정보를 출력하고 종료합니다.

### Example {id="example-mkdir"}

```Shell
mkdir folder-name
mkdir -p ./parent/child-name
```

<seealso>
    <category ref="official-documents">
        <a href="https://man7.org/linux/man-pages/man1/mkdir.1.html">mkdir</a>
    </category>
</seealso>
