# run

## Syntax

```Shell
docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]
```

## Options {id="options-run"}

--name
: docker container 이름을 지정합니다.
: `--name container-name`

-p
: `127.0.0.1:80:8080/tcp`

-P, --publish-all
: 노출된 모든 포트를 호스트에 개시

--expose
: 컨테이너 포트 노출
: `--expose 80`

-v, --volume
: docker의 볼륨 폴더를 지정합니다. `<host-path>:<container-path>`
: `--read-only` 읽기 전용

-m, --mount
: volume 옵션보다 mount 옵션을 권장
: `--mount type=bind,source=<path>,target=<path>`
: `--mount type=bind,source=<path>,target=<path>,readonly`
