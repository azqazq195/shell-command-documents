# mkdir

`mkdir` 명령어는 존재하지 않는 디렉토리를 생성하는 데 사용됩니다.

## Syntax

```Shell
mkdir [OPTION]... DIRECTORY...
```

## Options {id="options-mkdir"}

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

## Example {id="example-mkdir"}

```Shell
# 기본 디렉토리 생성
mkdir my_directory

# 여러 디렉토리 동시 생성
mkdir project_docs project_code project_tests

# 상위 디렉토리와 함께 여러 레벨의 디렉토리 생성
mkdir -p projects/my_project/docs

# 디렉토리 생성하며 파일 모드 설정
mkdir -m 755 secure_directory

# 생성된 디렉토리에 대한 메시지 출력
mkdir -v new_directory
```

<seealso>
    <category ref="official-documents">
        <a href="https://man7.org/linux/man-pages/man1/mkdir.1.html">mkdir man page</a>
    </category>
</seealso>