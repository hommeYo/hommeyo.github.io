---
layout: post
title:  Sublimetext
date:   2018-07-03 15:00
description: sublimetext 사용법
comments: true
tags: sublimetext tool
share: true 
---

## Package Control

`View > Show Console`, `ctrl + '`

[package control][package control]

[package control]: https://packagecontrol.io/

### package control list
* BracketHighlighter (ST3)
* ConvertToUTF8
* IMESupport (WIN)
* SideBarEnhancements (ST3)
* SFTP
* TortoiseSVN
* Diffy
* Emmet
* Goto-CSS-Declaration
* Sass
* SASS Build
* SublimeOnSaveBuild
* Theme - DC
* Theme - Soda

<br>

## 사용자 설정
`preferences > Settings - User`
* "always_show_minimap_viewport": true, // 미니맵에서 현재 위치 표시
* "bold_folder_labels": true, // 폴더 굵게 표시
* "build_on_save": 0, // SublimeOnSaveBuild (sublimetext2)
* "font_size": 13,
* "highlight_line": true, // 현재 줄 강조
* "soda_folder_icons": true, // Theme - Soda icons
* "theme": "DC_3.sublime-theme",  // Theme - DC
* "trim_trailing_white_space_on_save": true,  //저장 시 줄끝 공백 제거
* "word_wrap": true //자동 줄 바꿈 사용

`preferences > Key bindings - User`
* { "keys": ["ctrl+shift+alt+s"], "command": "toggle_side_bar" }

<br>

## 프로젝트 편집

`.sublime-project` 파일내 설정

``` json
{
  "folders": [{
    "file_exclude_patterns": [ // 제외할 파일
      "*.ico"
    ],
    "folder_exclude_patterns": [ // 제외할 폴더
      "test"
    ],
    "path": "E:\\work\\example-project1" // 프로젝트 경로
  }],
  "settings": {
    "tab_size": 2 // 탭 크기
  }
}
```

<br>

## Keyboard Tip

단축키 | 설명
--- | ---
cmd + x | 줄 잘라내기
cmd + Shift + d |   줄 복사
cmd + q (Win - Alt + F4) | 좌측에 작업 중이던 모든 폴더를 지워지지 않고 어플을 종료
cmd + / | 주석 처리/취소
Ctrl + Shift + UP/DOWN | 다중 편집 가능한 상태로 줄 선택(다중편집 모드)
cmd + Ctrl + UP/DOWN | 현재라인 이동
cmd + f | 검색
cmd + Alt + f | 바꾸기
cmd + Shift + f | 특정 폴더나 파일에서 내용 검색
cmd + Shift + v | 들여쓰기 맞춰서 붙혀넣기
cmd + t, cmd + p | 파일명으로 탭 찾기
Ctrl + g | 입력한 라인으로 이동
cmd + i | 현재 단어 찾기
cmd + Shift + g | 현재 단어 모두 찾아서 선택영역으로 만듦
Ctrl + Shift + m | 괄호 안의 내용을 모두 선택
cmd + option + LEFT/RIGHT | 탭 이동
Ctrl + m | 여는 괄호/ 닫는 괄호로 이동
cmd + Shift + t | 마지막에 닫은 탭 다시 오픈
cmd + Shift + p | 명령어 팔레트(Command Palette)
Ctrl + ` | 콘솔 보기(Show Console)
cmd + Alt + 1,2,3,4 | 세로분할 갯수
cmd + Alt + 5 | 그리드로 보기
Ctrl + 1,2,3,4 | 세로분할된 창 선택
Ctrl + Shift + 1,2,3,4 | 현재 탭을 세로분할된 창으로 이동
{:.wide.inner-borders}

<br>

## Emmet 사용법

### HTML 문서 기본형 축약코드

명령어 | 설명
--- | ---
doc | HTML5 문서 기본 골격 [DTD 제외]
doc4 | HTML4 문서 기본 골격 [DTD 제외]
html:4t | HTML4 문서 관용모드 기본 골격
html:4s | HTML4 문서 엄격모드 기본 골격
html:xt | XHTML1 문서 관용모드 기본 골격
html:xs | XHTML1 문서 엄격모드 기본 골격
html:5 또는 ! | HTML5 문서 기본 골격
{:.wide .inner-borders}

### 또 다른 HTML 문서 기본형 축약코드

명령어 | 설명
--- | ---
!!!4t | HTML4 관용모드 DTD
!!!4s | HTML4 엄격모드 DTD
!!!xt | XHTML1 관용모드 DTD
!!!xs | XHTML1 엄격모드 DTD
!!! | HTML5 DTD
{:.wide .inner-borders}

### HTML 에서 Emmet 활용

* div>h3+(ul>li>a)+(dl>dt+dd) 그룹핑
* div>h3+ul>li>a^^dl>dt+dd 캐럿기호를 사용한 부모요소 접근
* p[class="a b”] or p.a.b
* input:text
* #page>#nav>ul>li[class="item-\$$"]\*5
  \$$ // 01 ~
  \$$@- // 5부터 거꾸로~
  \$$@5 // 5부터 시작해서 증가
  \$$@-5"]\*5 // 5부터 시작하여 거꾸러~
* #page>#nav>ul>li[class="item-\$$@5"]{목록아이팀}\*5
  {} // 태그 내부 내용 입력
* a>{click}+strong{me!}
* p>a{clcik}+{이것은 emmet입니다}
* p\*2>lorem4
* p>lorem4.text\*2

<br>

## 참고 URL
* https://jeonghakhur.gitbooks.io/sublime-text3/content/
* https://opentutorials.org/module/406/3595

<br>
<br>
<br>
<br>
<br>






