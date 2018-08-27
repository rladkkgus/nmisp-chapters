# 사이파이 수치 해석<br>Numerical Methods in SciPy

## 소개<br>Introduction
이 소프트웨어는 다양한 수치 해법을 [`Python`](https://ko.wikipedia.org/wiki/%ED%8C%8C%EC%9D%B4%EC%8D%AC) 언어와 그 확장 기능인`SciPy` 를 이용하여 설명하고자 함.<br>
This software aims to describe various numerical methods in [`Python`](https://en.wikipedia.org/wiki/Python_%28programming_language%29) programming language and its extesion `SciPy'.

## 설치 항목<br>Software to install

### 파이썬 프로그래밍 언어<br>Python Programming Language
#### [Anaconda 5.x Python 3.6.x version](https://www.continuum.io/downloads) <br>
* 명령행에서 실행해야 할 경우, 경로에 추가하도록 설정 To run from a command line, configure to add python to the PATH
* 경로 이름에 한글을 사용할 수 없음 Use ASCII characters for path name
* 윈도우즈의 경우, 설치 후 [가상 환경 생성, 전환 2회 이상](https://graspthegist.com/post/learn-conda-1/) 확인 추천<br>For Windows, after install, please check [creating a virtual environment](https://conda.io/docs/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands) and [switching between environment](https://conda.io/docs/user-guide/tasks/manage-environments.html#activating-an-environment) more than twice.

### 깃 버전 관리 소프트웨어<br>Git Version Control Software
#### CUI
아래 소프트웨어를 설치 Please install following software
* [Git for Windows](https://git-scm.com/download/win)

간단한 추천 사항 A few simple recommendations
* 명령행에서 사용 Command line interface<br>
* 실습실 환경에서는 credential manager 설치 삼가<br>Credential manager may not be a best choice for a computer lab
* 아래 IDE 가운데 Microsoft Visual Studio Code 선택시 다음과 같이 생각해 볼 수 있음<br>
To use Microsoft Visual Studio Code among IDEs below, an administrator may consider followings<br>

| 항목<br>Key | 값<br>Value |
|:-------:|:-------:|
| git 기본 편집기 <br> Default editor for Git | MS VS Code |
| 경로 환경 조정 <br> Adjusting Path environment | Use Git from the Windows Command Prompt |
| 터미널 에뮬레이터 <br>Terminal emulator | Use Windows' default console window |
| 자격 인증 관리자 활성화  <br> Enable Git Credential Manager | 전산 실습 환경의 경우, 선택 해제<br>If computer lab, unselect |

이후 MS vscode 에서도 한두가지 추가 설정을 실시하면 내장 터미널로 `git-bash` 를 사용할 수 있음<br>
With a few additional configurations in MS vscode, one could use `git-bash` as the integrated terminal.

#### GUI
아래 가운데 택일 Choose one from below 
* [SourceTree](https://www.sourcetreeapp.com/download/) 
* [Github Desktop](https://desktop.github.com/)

### 통합 개발 환경<br>Integrated Development Environment
아래 가운데 택일 Choose one from below 
#### Spyder
* Anaconda 5.x 와 함께 설치됨.<br>Anaconda 5.x includes spyder.
#### [PyCharm Community](https://www.jetbrains.com/pycharm/download/)
* PyCharm 을 실행시키기 위해 [Java Development Kit](http://www.oracle.com/technetwork/java/javase/downloads/index.html) 를 설치해야 할 수 있음 (2016 09)<br>
PyCharm may need [Java Development Kit](http://www.oracle.com/technetwork/java/javase/downloads/index.html) to run.
#### [Microsoft Visual Studio Code](https://code.visualstudio.com/download)
* Anaconda 설치 후 설치 선택 가능<br>
Installation [button](https://blogs.msdn.microsoft.com/pythonengineering/2018/02/15/visual-studio-code-is-now-shipping-with-anaconda/) available at the end of Anaconda installation<br>
* [다운로드](https://code.visualstudio.com/download) 받아서 설치도 가능<br>
Possible to [download](https://code.visualstudio.com/download) and install from the website<br>
[Setup Overview](https://code.visualstudio.com/docs/setup/setup-overview) / 
[Python Configuration Instruction](https://code.visualstudio.com/docs/python/python-tutorial)
* Windows 에서 `git-bash`를 내장 터미널로 사용하려면 다음과 같은 추가 설정이 필요함.\[[참고](https://code.visualstudio.com/docs/editor/integrated-terminal)\]<br>
In Windows, to use `git-bash` as the integrated terminal, following additional settings would eable it.\[[Ref](https://code.visualstudio.com/docs/editor/integrated-terminal)\]

1. File > Preferences > Settings[참고 Ref](https://code.visualstudio.com/docs/getstarted/settings)\]
2. 
```json
"terminal.integrated.shell.windows": **path to bash.exe here**
```

### 설치 동영상<br>Installation video
[![설치 동영상 Installation video](https://i.ytimg.com/vi/NAQn1jQws3Q/hqdefault.jpg)](https://www.youtube.com/embed/videoseries?list=PLA6B0Lmr9oJOuvxMPNjDcnAfmqw907Bqy)

## `jupyter` 노트북 실행시키는 법<br>How to start a `jupyter` notebook
이 저장소 는 주로 [`jupyter` 노트북](http://blog.ncsoft.com/?p=21870)으로 만들어져 있음.<br>
This repository is mostly written in [`jupyter` notebook](http://arogozhnikov.github.io/2016/09/10/jupyter-features.html).<br>
`jupyter` 노트북은 웹브라우저를 통해 프로그램 코드를 수정 실행하고 LaTex 수식을 포함한 문서 작성이 가능함.<br>
Through a web browser, `jupyter` notebook enables editing & running program codes and writing documents including LaTex equations.<br>

* 적당한 folder 를 만듦 (예를 들어 User/Documents/Python_Scripts/) <br> Make an appropriate folder (e.g., User/Documents/Python_Scripts/)
* Git 또는 SourceTree 를 이용하여 위 folder 아래 이 원격 저장소를 `git clone` <br> Using the Git or SourceTree, `git clone` this repository under the folder
* `cmd` 또는 `git bash` 실행한 후 `clone` 된 지역 저장소 folder로 이동 (예를 들어 `cd User/Documents/Solmech/`) <br> Start `cmd` or `git bash` and change working folder to the cloned folder (e.g. `cd User/Documents/Solmech/`)
* `cmd` 또는 `git bash` 에서 각각 `cd` 또는 `pwd` 로 `clone` 된 folder 인지 확인 <br>Check location using `cd` or `pwd` in `cmd` or `git bash`
* `jupyter notebook` 실행 <br>Run `jupyter notebook`

### 실행 동영상 (SourceTree) (한글자막있음)<br>Instruction video (SoureTree)(English caption available)
[![실행 동영상 (SourceTree) Instruction video (SourceTree)](https://i.ytimg.com/vi/W6ynqGKJFSs/hqdefault.jpg)](https://www.youtube.com/embed/videoseries?list=PLA6B0Lmr9oJO9HeSC74wqxECtwpUPJfdm)

## 알림 <br> Acknowledgement
이 소프트웨어는 대한민국 국토교통부 건설교통과학기술진흥원 교통물류연구사업의 지원을 받아 시작되었음 (18TLRP-B117133-03)<br>
This software was initially supported by the Korea Ministry of Land, Infrastructure, and Transportation. It was also supported by the Korean Agency for Infrastructure Technology Advancement. (18TLRP-B117133-03)
