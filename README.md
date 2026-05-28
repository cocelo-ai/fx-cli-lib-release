# fx-cli v1.2.1

**ARM64/AMD64 Ubuntu 환경에서 Python 3.10/3.11을 지원하는 릴리스 패키지입니다.**

## 다운로드

```bash
export lib_ver=1.2.1
export py_ver=$(python3 -c 'import sys; print(f"{sys.version_info.major}{sys.version_info.minor}")')
export arch=$(dpkg --print-architecture)

git clone -b "v${lib_ver}_py${py_ver}_${arch}" git@github.com:cocelo-ai/fx-cli-lib-release.git
```

## 설치

다운로드한 `.deb` 파일을 사용하여 다음 명령어로 설치합니다.

```bash
sudo apt install ./fx-cli_${lib_ver}_py${py_ver}_${arch}.deb
```

만약 사용 중인 환경에서 `apt install`이 정상적으로 동작하지 않는 경우, 아래 명령어를 사용합니다.

```bash
sudo dpkg -i fx-cli_${lib_ver}_py${py_ver}_${arch}.deb
sudo apt-get install -f
```

## 설치 확인

설치가 정상적으로 완료되었는지 확인하려면 다음 명령어를 실행합니다.

```bash
python3 -c "import fx_cli; print('fx_cli import success')"
```

## 참고 사항

* 대상 플랫폼: ARM64/AMD64 Ubuntu
* 지원 Python 버전: Python 3.10 또는 Python 3.11
* 본 패키지에 포함되는 항목:

  * C++ 라이브러리
  * Python 바인딩 모듈 (`fx_cli`)
