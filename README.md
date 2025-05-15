# 리팩토링 실습 - 타이타닉 생존자 분류

코드 스멜(Code Smell)이 많은 Jupyter Notebook을 모듈화하고, 가독성 높고, 테스트 가능한 코드베이스로 리팩토링하는 실습입니다.

## 설정

go 스크립트를 실행하여 필수 의존성을 설치합니다.
해당 스크립트는 Python 3와 Poetry를 설치하고, 호스트에 가상 환경(Virtual Environment)을 생성합니다.
이렇게 하면 IDE에서 Python 인터프리터를 손쉽게 설정할 수 있습니다.

```shell script
# mac users
scripts/go/go-mac.sh

# linux users
scripts/go/go-linux-ubuntu.sh

# Windows 사용자의 경우
# 1. Python3을 설치하지 않았다면 다운로드하고 설치하세요: https://www.python.org/downloads/release/python-31011/
#    - 설치 시, "Add Python to PATH" 옵션을 선택하세요.
# 2. Windows 탐색기 또는 검색에서 'Manage App Execution Aliases'로 이동하여, 'App Installer'의 python 항목을 비활성화하세요. 
#    이는 `python` 실행 파일이 PATH에서 인식되지 않는 문제를 해결합니다.
# 3. Powershell 또는 Command Prompt에서 Go 스크립트를 실행합니다.
.\scripts\go\go-windows.bat
# 참고: 만약 HTTPSConnectionPool read timed out 에러가 발생한다면, poetry 설치가 성공할 때까지 몇 번 더 실행해 보세요.
```

go 스크립트로 생성된 Python 가상 환경을 IDE에서 사용하도록 설정
- [PyCharm 설정 방법](https://www.jetbrains.com/help/pycharm/creating-virtual-environment.html#existing-environment)
- [VS Code 설정 방법](https://code.visualstudio.com/docs/python/environments)

## 실행할 수 있는 작업들

```shell script
# Activate virtual environment
poetry shell

# Start jupyter notebook
jupyter notebook

# Run model training smoke tests
scripts/tests/model-metrics-test.sh

# Train model
scripts/train-model.sh 
```
