---
layout: post
title: 개발자를 위한 macOS(>= Sequoia) 설정
author: 한상곤
tags: article
---

> 새로운 마음으로 시작하고 싶은 개발자들을 위한 작은 가이드 입니다. 새로운 시작을 위해 가장 중요한 것은 백업입니다. 백업부터 투철하게 하세요. AWS 인증키나 1password 백업파일, 기존에 사용하시던 설정(`.zshrc`, `init.el`, `vscode` 등...)은 어딘가(`Dropbox` or `github`)에 반드시 보관해 주세요. Dropbox 동기화가 최신으로 되어 있는지도 확인하세요. `포멧(Erase)`은 돌아오지 않아요. 백업 및 클라우드에 모든 파일이 동기화 되셨나요? 이제 시작해보죠! - 2025.09.17

운영체제를 새롭게 설치하거나 부득이한 사정으로 인해서 운영체제의 업데이트가 아닌 모든 과정을 다시 설정해야 경우가 있습니다. 대부분의 개발자들이 기존에 사용하던 환경을 뒤로하고, 모든 환경을 새롭게 구성하는 것은 쉽지 않은 결정입니다. 그래서 대부분의 개발자들은 시스템의 문제를 해결할 수 없거나, 발생할 수 있는 오류의 가짓수를 줄이기 위한 노력의 일환으로 클린 설치(모든 것을 삭제하고 새롭게 설치하는 것)를 진행합니다. 따라서, 별다른 이유가 없다면 클린 설치나 초기화를 하지 않기를 권해드립니다.

## 클린 설치를 위한 변경사항 안내

더 이상 USB를 사용한 설치 디스크를 만들어서 진행하지 않아도 됩니다. 설정에서 제공되는 `macOS` 업그레이드(upgrade)를 선택하신 후에, 초기화(`System Settings > General > Transfer or Reset > Erase All Content and Settings`)를 선택하시면 됩니다. 이후 과정은 macOS의 안내에 따라 진행하시면 됩니다.

### 클린 설치시 주의사항

> USB를 사용하여 설치 디스크를 만들어서 진행하고 싶다면, USB 설치 디스크를 선호하시는 분들은 가장 뒷부분의 Appendix를 참고해주세요.  

`Ventura` 버전부터 초기화 기능이 강력하기 때문에 USB 설치 디스크를 만들어서 클린 설치를 해야 할 이유가 거의 없지만, USB 클린 설치를 원하시는 분들은 별도의 진행절차를 확인해주세요. 하지만 가능하면 USB 설치는 권해드리지 않습니다. 왜냐하면, USB 설치시 발생할 수 있는 특이사항(하드웨어 인증)의 경우 대처가 힘들 수 있습니다. 가능하시면 업데이트 이후 초기화를 선택하시길 권해드립니다. USB로 새로운 운영체제를 설치하는 건 `Intel` 하드웨어 기반의 macOS 사용자 뿐만 아니라 모든 macOS 사용자에게 권해드리지 않습니다.

## 운영체제 설정

> 제가 개인적으로 사용하는 시스템 설정입니다. 간략하게 해당 설정을 적용/미적용 하는 이유를 적어두었으니 참고하시면 좋을 듯 합니다.

### 시스템 설정(System Settings)

- General   
  - `About > Name`은 iCloud에 표시될 기기이름
  - `AirDrop & Handoff > Allow Handoff between this Mac and your iCloud devices`를 선택, Mac과 iPhone, iPad간에 작업을 이어서 진행할 수 있음
  - `Date & Time > 24-hour time` 등과 같이 자주 사용하시는 옵션을 선택
  - `Language & Region > Preferred Languages > 'English - Primary', 'Korean'` 로 설정, 개발 과정에서 오류 및 에러가 한글로 출력되지 않도록 하기 위해서 영어를 Primary로 설정
  - `Sharing > Local hostname`은 Terminal에 표시, 될 수 있으면 짧고 적당한(?) 것으로 변경
   
- Appearance
  - `Apperance > Dark`를 선택, 밝은색을 원하시면 Light를 선택
  
- Menubar
  - `Spotlight`, `Wi-Fi`, `Bluetooth`, `Battery(Battery Options... > Show Percentage)`, 
  - `Focus`, `Screen Mirroring`, `Display`, `Now Playing`는 `Show When Active`로 설정
  - `Sound > Always Show`로 설정

- Apple Intelligence & Siri
  - `Listen for "Siri야" > On`, `Keyboard shortcut > Off`, `Language > Korean`

- Desktop & Dock
  - `Show suggested and recent apps in Dock > Off`, 최근 사용한 애플리케이션을 Dock에 표시하는 옵션으로 Dock이 복잡해지는 것을 좋아하지 않아서 사용하지 않음
  - `Stage Manager > Off`, `Stage Manager > Show recent apps in Stage Manager > On`
  - `Widgets > iPhone Widgets > Off`
  - `Mission Control > Automatically rearrange Spaces based on mst recent use > Off`, Space를 변경할 때, 최근에 사용된 Space를 중심으로 배치되는데 개발할 때 좌우 Space를 고정해서 사용하는 것을 선호하기 때문에 사용하지 않음

- Spotlight
  - `Results from System > Phone Apps > Off`, iPhone과 연동되는 앱을 Spotlight에서 검색하지 않음

- Keyboard
  - `Keyboard Shortcuts... > Modifier Keys.. > Caps Lock`, Emacs를 사용하신다면 `Control`로 변경하는게 훨씬 편리함
  - `Text Input > Edit`를 선택해서 Show Input menu in menu bar를 제외하고 모든 옵션의 선택을 해제, `Use smart quotes and dashes`를 해제하시면 사소한 실수를 줄일 수 있음
  - `Text Replacements...`에 등록된 모든 것들을 제거
- Trackpad
  - `Point & Click > Tap to click`을 선택, 트랙패드를 탭하는 것으로 클릭을 대체

- Finder 설정
  - `Finder > Finder Settings > General > New Finder windows show`를 자신의 홈 폴더를 선택
  - `Sidebar` 에서 필요하거나 불필요한 폴더를 선택해서 Finder 왼쪽의 즐겨찾기 목록을 수정
  - `Advanced > Show all filename extensions`를 선택, 저는 확장자를 확인해야 될 일이 많으시면 해당 옵션을 선택
  - `Keep folders on top > In windows when sorting by name`, 파인더의 정렬을 사용할 때, 폴더를 우선 정렬하고 싶으시면 해당 옵션을 선택
  - `When performing a search`에서 `Search the Current Folder`을 선택하시면 폴더 내부를 검색할 수 있음

### 한/영 변환키를 Shift+Space(`⇧+Space`)로 변경하는 방법

> (2023.09) Sonoma 경우 Fn+Shift+Space가 적용되지 않는 듯 합니다. 그래서 아래 Xcode를 설치하시고 파일을 직접 수정하시면 됩니다. 그리고 Fn키가 없는 키보드를 사용중인 iMac 사용자의 경우 아래 방법으로 Shift+Space 한영전환이 가능합니다.

> (2024.09) @adhrinae님이 트윗으로 좋은 방법 알려주셔서을 알려주셨는데, Sonoma에서는 적용되지 않습니다.
  
- `plist`를 수정하기 위해서 가장 좋은 방법은 Xcode를 설치하는 것 (여타의 다른 소프트웨어를 사용하셔도 됩니다만 개인적으로 Xcode를 권장)
- `Finde`r에서 `Go > Go to Folder(Command + Shift + G)`를 선택하여 `~/Library/Preferences/com.apple.symbolichotkeys.plist`를 선택
- 해당 파일의 내용 중에서 <key>61</key>을 찾아서 <item 2>786,432</item2>의 <number>131072</number>로 변경하고 파일을 저장
- 저장 후에 맥을 재시동
  
## 프로그램 설치

### App Store 프로그램 설치
 
 - Apple에서 제공하는 앱인 `Xcode`, `Page`, `Numbers`, `Keynote` 등은 App Store를 사용해서 설치
 - KakaoTalk 등과 같은 App Store에서 제공하는 프로그램도 App Store를 사용해서 설치

### brew를 사용한 프로그램 설치

> Homebrew(이하 brew)는 macOS에서 가장 널리 사용되는 패키지 관리자입니다. brew를 사용하면, 다양한 오픈소스 프로그램을 손쉽게 설치할 수 있습니다. brew는 공식 홈페이지(https://brew.sh/)에서 설치 방법을 확인할 수 있습니다.

- brew 설치는 아래와 같이 진행

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew update
```

- brew를 사용한 프로그램 설치

> docker 처럼 Formulae와 Casks에 동일한 이름의 패키지가 존재하고, Casks를 기반으로 설치해야 할 경우 brew install docker --cask로 설치하시면 됩니다.

```bash
brew install --cask dropbox iterm2 visual-studio-code keepingyouawake jetbrains-toolbox gitkraken docker
```

- brew로 프로그램 검색

```bash
brew search ocaml
==> Formulae
ocaml ocaml-findlib ocaml-num ocaml-zarith ocamlbuild ocm

==> Casks
local
```

### iterm2 설정

> iTerm2는 macOS에서 가장 널리 사용되는 터미널 프로그램입니다. iTerm2를 사용하면, 다양한 기능을 활용할 수 있습니다. iTerm2는 공식 홈페이지(https://iterm2.com/)에서 설치 방법과 다양한 기능을 확인할 수 있습니다.
   
- `iterm2 > Preferences`에서 몇가지 환경설정을 진행   
  - `Appearance > Theme`, Dark 혹은 원하시는 Theme를 선택
  - `Appearance > Windows > Hide scrollbars`을 선택
  - `Appearance > Windows > Show line under title bar when the tab bar is not visible`을 사용하지 않음을 선택
  - `Appearance > Panes > Side margins`와 `Top & bottom margins`을 15 정도로 설정
  - `Profiles > Text > Font`는 D2Coding을 선택
    - ZSH의 테마를 설정하시면 Powerline 폰트가 필요할 경우가 있는데, D2Coding을 선택하시면 큰 문제 없이 사용할 수 있음
  - `Profiles > Session > Status bar enabled`는 CPU나 RAM 등의 정보를 터미널에 표시하는 것으로 필요한 것을 추가해서 사용

### Zsh 설정

> zsh는 macOS에서 기본으로 제공하는 쉘입니다. zsh를 사용하면, 다양한 기능을 활용할 수 있습니다. zsh는 공식 홈페이지(https://www.zsh.org/)에서 설치 방법과 다양한 기능을 확인할 수 있습니다.

- `oh-my-zsh`을 설치

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

- zsh 플러그인을 설치

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```
- `~/.zshrc` 파일의 plugins 항목에 `git`, `zsh-syntax-highlighting`, `zsh-autosuggestions`을 추가

## 필요한 개발 환경 설정

### (애증의) Ruby

- Ruby의 경우 사용하시는 버전이 각자 다르기 때문에 버전 관리자를 먼저 설치
```
brew install rbenv
```

- `.zshrc`에 `eval "$(rbenv init - zsh)"`를 입력
- rbenv를 사용해서 Ruby 설치

```bash
// Ruby
$ rbenv install 3.4.6
$ rbenv rehash
$ rbenv global 3.4.6
$ ruby -v
ruby 3.4.6 (2025-09-16 revision dbd83256b1) +PRISM [arm64-darwin25]
```

### Haskell

> 즐거운 프로그래밍 언어인 Haskell도 brew를 사용해서 손쉽게 설치 가능합니다. :D

```bash
$ brew install ghcup
$ ghcup install stack
$ ghcup set stack
$ ghcup install ghc
$ ghcup set ghc
$ ghcup install hls
$ ghcup set hls
$ ghcup install cabal
$ ghcup set cabal
```

## Appendix

### Clean install을 위한 USB 만들기

- macOS 다운로드
  - Ventura를 App Store에서 다운로드  
  - 다운로드가 완료되면 Sonoma 설치 관련(Install macOS Sonoma) 안내 페이지를 확인할 수 있는데, 해당 페이지를 실행하지 말고 종료(Quit Install macOS).

- USB 준비
  - 16기가 이상의 USB를 사용하세요. USB를 초기화하기 위해서 `App > Other > Disk Utility`를 실행해서, `Disk Utility의 External` 항목에 사용할 USB를 선택하시고 Erase를 선택해서 USB를 초기화
  - USB의 Name은 `macOS-Installer`로 하였고, Format은 `Mac OS Extended (Journaled)`
  - Terminal(혹은 iTerm2 등)을 실행하고 `sudo /Applications/Install\ macOS\ Sonoma.app/Contents/Resources/createinstallmedia --volume /Volumes/macOS-Installer/`를 실행      
  - sudo는 관리자 권한이 필요하단 뜻으로 해당 명령어를 실행하면 시스템의 비밀번호를 입력해야 함
  - `--volume`은 USB의 경로(일반적으로 /Volumes/ 아래에 USB의 레이블명(Name)으로 존재)를 적어줌

- USB를 사용해서 설치하기
  - Big Sur에서 USB Booting 관련 설정을 하셨다면 아래 USB 부팅 설정은 건너띄고 진행
  - 만약 이번에 처음 USB로 설치를 진행하신다면 USB 부팅 설정을 꼭 확인, 설치시 사용하는 키는 아래 이미지에서 확인

### macOS 부팅 및 설치

- USB 부팅 설정
  - 컴퓨터를 부팅할 때 복구모드 설정 키(Command + R)을 누르고 있으면 복구 모드로 진행
  - 이때, 사용하는 비밀번호는 현재 설치된 운영체제에서 사용하는 비밀번호
  - iCloud 관련 비번이 아니니 주의
  - 복구모드에서 상단의 메뉴바를 선택하고 `Utilities > Startup Security Utility`를 선택 후
  - 기존에 사용하시던 macOS의 비밀번호를 입력하면, 옵션이 출력
  - 하단에 위치한 `Allow booting from external or removable media`를 선택하시고, 창을 닫은 후 사과마크를 눌러서 `restart`를 선택

- USB 부팅
  - 컴퓨터가 새로 시작될 때, Option 키 누르고 있으면, Boot Disk를 선택하는 화면에서 Install macOS Sonoma를 선택
  - 만약 업데이트가 필요하다는 알림창이 안내된다면 업데이트를 진행(`A software update is required to use this startup key`)
  - Disk Utility를 사용해서 기존에 사용하던 디스크를 Erase를 하시고, Install macOS Sonoma를 사용해서 설치
  - 설치 후 몇번의 재부팅이 되고 난 이후에, 그래픽 화면에서 중요 설정 사항을 입력하는 화면이 진행, 지역 및 iCloud 등은 안내에 맞춰서 진행하시면 됨
  - 저는 개발 환경을 구성하기 기존의 데이터를 마이그레이션(`Migration Assistant > Not Now`) 하지 않았음, 기존에 데이터를 마이그레이션 하셔야 된다면 적절한 옵션을 선택

## Updated

- 2025.09.30
  - 26.0.1 (25A362)로 문서 업데이트  

- 2024.10.01   
  - Sequoia 반영   

- 2023.09.27   
  - Sonoma로 문서 업데이트   

- 2022.10.25   
  - Ventura로 문서 업데이트
  - 이미지 수정 및 M1/M2 사용자를 위한 간단한 가이드 추가   

- 2021.10.25   
  - Monterey로 문서 업데이트
  - 이미지가 없어서 불편하다는 의견을 반영해서, 도움이 될만한 이미지 추가   

- 2021.01.12   
  - brew를 사용해서 pyenv(>=1.2.22) 설치
  - brew를 사용해서 nvm(>=0.37.2) 설치   

- 2021.01.02   
  - pyenv 설치 변경
  - 오타 수정   

- 2020.11.14   
  - Big Sur 변경
  - pyenv 설치 에러 관련해서 설치방법
