# rm

`rm` 명령어는 파일이나 디렉토리를 제거하는 데 사용됩니다. 지정된 각 파일을 제거하며, 기본적으로 디렉토리는 제거하지 않습니다. 사용자가 보호 기능을 활성화할 옵션이 제공되어, 실수로 중요한 파일이나 디렉토리를
삭제하는 것을 방지할 수 있습니다.

## Syntax

```Shell
rm [OPTION]... [FILE]...
```

## Options {id="options-rm"}

-f, --force
: 존재하지 않는 파일과 인수를 무시하고, 물음 없이 진행

-i
: 모든 제거 작업 전에 물음

-I
: 세 개 이상의 파일을 제거하거나 재귀적으로 제거할 때 한 번 물음

--interactive[=WHEN]
: WHEN에 따라 물음: never, once(-I), always(-i)

--one-file-system
: 재귀적으로 제거할 때 다른 파일 시스템의 디렉토리는 건너뜀

--no-preserve-root
: '/'를 특별히 취급하지 않음

--preserve-root[=all]
: '/'를 제거하지 않음, 'all'이면 부모와 다른 장치에 있는 명령줄 인수를 거부

-r, -R, --recursive
: 디렉토리와 그 내용을 재귀적으로 제거

-d, --dir
: 빈 디렉토리를 제거

-v, --verbose
: 진행 중인 작업 설명

## Example {id="example-rm"}

```Shell

# 단일 파일 제거
rm myfile.txt

# 여러 파일 동시에 제거
rm file1.txt file2.txt file3.txt

# 디렉토리 재귀적으로 제거
rm -r my_directory

# 제거 전에 사용자 확인 요청
rm -i file_to_remove.txt

# 디렉토리 및 내부 파일 강제 제거
rm -rf my_directory
```

<seealso>
    <category ref="official-documents">
        <a href="https://www.gnu.org/software/coreutils/rm">rm man page</a>
    </category>
</seealso>
