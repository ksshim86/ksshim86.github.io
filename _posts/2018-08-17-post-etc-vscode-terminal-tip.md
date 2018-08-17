---
layout: single
title: "Visual Studio Code 터미널 여러 개 사용하기"
date: 2018-08-17 17:10:00
categories: 
  - etc
tags:
  - vscode
  - Visual Studio Code
  - terminal
---
소스를 커밋하기 위해 `Git bash` 를 열어야 할 때도 있고, 서버를  
실행하기 위해 `Ruby cmd`를 열어야 할 때도 있고,  
그냥 `cmd` 를 열어야 할 때도 있는데 따로 프로그램으로 열기  
귀찮아 `vscode` 에서 여러 개 사용하는 방법을 찾아서 정리해보았다. 

## 1. 'Shell Launcher' 확장 프로그램 설치
* 링크: <https://marketplace.visualstudio.com/items?itemName=Tyriar.shell-launcher>
* 설치 후, `vscode` 재시작

## 2. 사용자 설정 추가
* 사용자 설정 파일 열기
  1. 파일 > 기본 설정 > 설정  
  2. 단축키: `Ctrl + Comma`
  3. `Ctrl + P` > `settings.json`
* 코드 추가
~~~
"shellLauncher.shells.windows": [
    {
        "shell": "C:\\Windows\\sysnative\\cmd.exe",
        "label": "cmd"
    },
    {
        "shell": "C:\\Ruby24-x64\\bin\\setrbvars.cmd",
        "label": "Ruby"
    },
    {
        "shell": "C:\\Program Files\\Git\\bin\\bash.exe",
        "label": "Git bash"
    }
]
~~~
`shell` 에 추가할 터미널 경로를 입력하고, `label` 에는 선택할 때 보일 명칭을 입력 후 저장

## 3. 단축키 설정 추가
* 단축키 설정 파일 열기
  1. 파일 > 기본 설정 > 바로 가기 키 
  2. 단축키: `Ctrl + K` `Ctrl + S`
  3. `Ctrl + P` > `keybindings.json`
* 코드 추가
~~~
{
    "key": "ctrl+shift+t",
    "command": "shellLauncher.launch"
}
~~~
`key` 에 원하는 단축키 입력하고 저장