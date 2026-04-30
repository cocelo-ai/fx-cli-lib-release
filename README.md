# fx-cli v1.0.1

Release package for **ARM64 Ubuntu (py3.10/py3.11) support**.

## Download
```bash
export lib_ver=1.0.1
export py_ver=310

git clone -b fx-cli_${lib_ver}_py${py_ver}_arm64 git@github.com:cocelo-ai/fx-cli-lib-release.git
```
## Install

Download the `.deb` file from the **Assets** section, then install it with:

```bash
sudo apt install ./fx-cli_{lib_ver}_py{py_ver}_arm64.deb
```

If apt install does not work in your environment, use:
```bash
sudo dpkg -i fx-cli_{lib_ver}_py{py_ver}_arm64.deb
sudo apt-get install -f
```

## Verify Installation
```bash
python3 -c "import fx_cli; print('fx_cli import success')"
```

## Notes
- Target platform: ARM64 Ubuntu
- Python requirement: Python 3.10 or Python 3.11
- This package installs:
  - C++ library
  - Python binding module (`fx_cli`)
