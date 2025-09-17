# 개발자를 위한 macOS(>= Sequoia) 설정

> 새로운 마음으로 시작하고 싶은 개발자들을 위한 작은 가이드 입니다. 새로운 시작을 위해 가장 중요한 것은 백업입니다. 백업부터 투철하게 하세요. AWS 인증키나 1password 백업파일, 기존에 사용하시던 설정(`.zshrc`, `init.el`, `vscode` 등...)은 어딘가(`Dropbox` or `github`)에 반드시 보관해 주세요. Dropbox 동기화가 최신으로 되어 있는지도 확인하세요. `포멧(Erase)`은 돌아오지 않아요. 백업 및 클라우드에 모든 파일이 동기화 되셨나요? 이제 시작해보죠! - 2025.09.17

운영체제를 새롭게 설치하거나 부득이한 사정으로 인해서 운영체제의 업데이트가 아닌 모든 과정을 다시 설정해야 경우가 있습니다. 대부분의 개발자들이 기존에 사용하던 환경을 뒤로하고, 모든 환경을 새롭게 구성하는 것은 쉽지 않은 결정입니다. 그래서 대부분의 개발자들은 시스템의 문제를 해결할 수 없거나, 발생할 수 있는 오류의 가짓수를 줄이기 위한 노력의 일환으로 클린 설치(모든 것을 삭제하고 새롭게 설치하는 것)를 진행합니다. 따라서, 별다른 이유가 없다면 클린 설치나 초기화를 하지 않기를 권해드립니다.

## 클린 설치를 위한 변경사항 안내

더 이상 USB를 사용한 설치 디스크를 만들어서 진행하지 않아도 됩니다. 설정에서 제공되는 macOS 업그레이드(upgrade)를 선택하신 후에, 초기화(`System Settings > General > Transfer or Reset > Erase All Content and Settings`)를 선택하시면 됩니다. 이후 과정은 macOS의 안내에 따라 진행하시면 됩니다.

### 클린 설치시 주의사항

> USB를 사용하여 설치 디스크를 만들어서 진행하고 싶다면, USB 설치 디스크를 선호하시는 분들은 가장 뒷부분의 Appendix를 참고해주세요.  

`Ventura` 버전부터 초기화 기능이 강력하기 때문에 USB 설치 디스크를 만들어서 클린 설치를 해야 할 이유가 거의 없지만, USB 클린 설치를 원하시는 분들은 별도의 진행절차를 확인해주세요. 하지만 가능하면 USB 설치는 권해드리지 않습니다. 왜냐하면, USB 설치시 발생할 수 있는 특이사항(하드웨어 인증)의 경우 대처가 힘들 수 있습니다. 가능하시면 업데이트 이후 초기화를 선택하시길 권해드립니다. USB로 새로운 운영체제를 설치하는 건 `Intel` 하드웨어 기반의 macOS 사용자 뿐만 아니라 모든 macOS 사용자에게 권해드리지 않습니다.

## 운영체제 설정

> 제가 개인적으로 사용하는 시스템 설정입니다. 간략하게 해당 설정을 적용/미적용 하는 이유를 적어두었으니 참고하시면 좋을 듯 합니다.

### 시스템 설정(System Settings)

- General   
  - `About > Name`은 iCloud에 표시될 기기이름 입니다.
  - `Date & Time > 24-hour time` 등과 같이 자주 사용하시는 옵션을 선택하세요.
  - Language & Region > Preferred Languages > 'English - Primary', 'Korean' 로 설정합니다. 개발 과정에서 오류 및 에러가 한글로 출력되지 않도록 하기 위해서 영어를 Primary로 설정하였습니다. 
  - `Sharing > Local hostname`은 Terminal에 표시됩니다. 될 수 있으면 짧고 적당한(?) 것으로 변경하세요.
   
- Appearance
  - `Apperance > Dark`를 선택하였습니다. 밝은색을 원하시면 Light를 선택하세요.
  
- Menubar
  - Spotlight, Wi-Fi, Bluetooth, Battery(Battery Options... > Show Percentage), Focus, Screen Mirroring, Display, Sound(Always Show), Now Playing

- Siri
  - `Listen for "Siri야" > On`, `Keyboard shortcut > Off`, `Language > Korean`
  
- Desktop & Dock
  - `Show suggested and recent apps in Dock > Off`
  - `Stage Manager > Off`, `Stage Manager > Show recent apps in Stage Manager > On`
  - `Widgets > Ipone Widgets > Off`
  - `Mission Control > Automatically rearrange Spaces based on mst recent use > Off`
   
- Spotlight
  - `Results from System > Phone Apps > Off` 
   
  
   
   
   Desktop & Dock
   
   
   * Show suggested and recent applications in Dock을 사용하지 않음으로 설정하였습니다. 최근 사용한 애플리케이션을 Dock에 표시하는 옵션으로 Dock이 복잡해지는 것을 좋아하지 않아서 사용하지 않습니다.
   * Mission Control > Automatically rearrange Spaces based on most recent use의 선택을 해제합니다. Space를 변경할 때, 최근에 사용된 Space를 중심으로 배치되는데 개발할 때 좌우 Space를 고정해서 사용하는 것을 선호하기 때문에 사용하지 않습니다.
   
 * 
   
   
   Keyboard
   
   
   * Keyboard Shortcuts... > Modifier Keys.. > Caps Lock; Emacs를 사용하신다면 Control로 변경하는게 훨씬 편합니다.
   * Text Input > Edit를 선택해서 Show Input menu in menu bar를 제외하고 모든 옵션의 선택을 해제합니다. 그리고 Text Replacements...에 등록된 모든 것들을 제거합니다.
   * Text > Replace 항목 모두 삭제하고 왼쪽에 있는 모든 선택 항목을 해제; 개발관련 업무를 진행중이시면 Use smart quotes and dashes를 해제하시면 사소한 실수를 줄일 수 있으며, 자동 변경과 관련된 모든 옵션은 사용하지 않습니다.
   






Finder 설정


 * 파인더(Finder)를 실행하고, Finder > Preferences를 실행합니다.
   
   * General > New Finder windows show
     
     * 자신의 홈 폴더를 선택합니다.
     
   * Sidebar 에서 필요하거나 불필요한 폴더를 선택해서 Finder 왼쪽의 즐겨찾기 목록을 수정하세요.
   * Advanced > Show all filename extensions를 선택하세요. 확장자를 확인해야 될 일이 많으시면 해당 옵션을 선택합니다.
   * 파인더의 정렬을 사용할 때, 폴더를 우선 정렬하고 싶으시면 Keep folders on top > In windows when sorting by name을 선택하세요.
   * 파인더의 검색 창의 범위를 조절하고 싶으시면 When performing a search 관련 옵션을 조절하세요. 전 Search the Current Folder를 선택해서, 폴더 내부에서 검색하는 것을 선호합니다.
   



App Store 프로그램 설치


 * 가장 먼저 Xcode를 설치해주세요. 이후에 App Sotre에서 Page, Numbers, Keynote, KakaoTalk, Movist, Magnet, Telegram 등은 App Store를 사용해서 설치하시면 됩니다.



brew를 사용한 프로그램 설치



brew 설치


 * 터미널에서 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"를 실행하여, brew를 설치합니다.
 * 터미널에서 아래 명령어를 실행하여 brew를 실행 경로(Path)에 추가해줍니다.


$ echo >> /Users/sd/.zprofile
$ echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/sd/.zprofile
$ eval "$(/opt/homebrew/bin/brew shellenv)"



 * 자세한 사항은 brew 공식 홈페이지를 참고하세요.



brew를 사용한 프로그램 설치


 * brew 설치 후 자주 사용하는 프로그램을 설치하도록 합니다. 아래 예시는 제가 자주 사용하는 프로그램입니다. 필요한 프로그램이 있으면 search를 사용해서 검색하셔서 설치하시면 됩니다.


$ brew search ocaml
==> Formulae
ocaml ocaml-findlib ocaml-num ocaml-zarith ocamlbuild ocm

==> Casks
local



 * docker 처럼 Formulae와 Casks에 동일한 이름의 패키지가 존재하고, Casks를 기반으로 설치해야 할 경우 brew install docker --cask로 설치하시면 됩니다.


$ brew install --cask dropbox iterm2 google-chrome visual-studio-code keepingyouawake jetbrains-toolbox gitkraken microsoft-edge docker brave-browser




폰트 설치


 * 자주 사용하는 폰트를 설치하기 위해서 brew의 별도의 tap을 설정한 후에 폰트를 설치합니다.


$ brew install font-d2coding font-ibm-plex-sans-kr font-ibm-plex-mono font-meslo-lg-nerd-font font-d2coding-nerd-font




iterm2 설정


 * iterm2의 컬러 테마는 이 곳에서 다운로드하여 설치합니다.
   
   * Preferences > Profiles > Colors > Color Presets > Import... 를 선택해서 다운로드 받은 컬러 테마의 압축 폴더 중에서 schemes에 있는 설정 파일을 선택하시면 됩니다.
   
 * iterm2 > Preferences에서 몇가지 환경설정을 합니다.
   
   * Appearance > Theme : Dark 혹은 원하시는 Theme를 선택합니다.
   * Appearance > Windows > Hide scrollbars을 사용함으로 선택합니다.
   * Appearance > Windows > Show line under title bar when the tab bar is not visible : 사용하지 않습니다.
   * Appearance > Panes > Side margins와 Top & bottom margins을 15 정도로 설정합니다.
   * Profiles > Text > Font: D2Coding을 선택하세요. ZSH의 테마를 설정하시면 Powerline 폰트가 필요할 경우가 있는데, D2Coding을 선택하시면 큰 문제 없이 사용할 수 있습니다.
   * Profiles > Session > Status bar enabled: CPU나 RAM 등의 정보를 터미널에 표시하는 것으로 필요한 것을 추가해서 사용하세요.
     
     
   



Zsh 설정


 * oh-my-zsh을 설치(sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)") 합니다.
 * zsh 플러그인을 설치합니다.
   
   * brew install zsh-completions를 설치합니다.
   * git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
   * git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
   * 설치된 플러그인을 ZSH에서 활성화 하기 위해서 ~/.zshrc 파일의 plugins 항목에 git, zsh-syntax-highlighting, zsh-autosuggestions를 설치합니다. 항목을 작성하실 때 plugins=(git zsh-syntax-highlighting zsh-autosuggestions)와 같이 ,가 아닌 공백으로 구분하시면 됩니다.
   
 * theme는 이 곳을 참고하세요.
   
   * Spaceship ZSH등과 같은 테마도 있으니 검색해서 자신만의 테마를 선택해보세요.
     
     
   



한/영 변환키를 Shift+Space로 변경하는 방법


 * 
   
   
   Xcode를 설치하신 이후에 한/영 변환키를 ⇧+Space로 설정하시는 분들은 해당 항목을 진행하시면 됩니다.
   

 * 
   
   
   (2023.09.27) Sonoma 경우 Fn+Shift+Space가 적용되지 않는 듯 합니다. 그래서 아래 Xcode를 설치하시고 파일을 직접 수정하시면 됩니다. 그리고 Fn키가 없는 키보드를 사용중인 iMac 사용자의 경우 아래 방법으로 Shift+Space 한영전환이 가능합니다.
   
   
   * plist를 수정하기 위해서 가장 좋은 방법은 Xcode를 설치하는 것 입니다(여타의 다른 소프트웨어를 사용하셔도 됩니다만 개인적으로 Xcode를 권장합니다).
   * Finder에서 Go > Go to Folder(Command + Shift + G)를 선택하여 ~/Library/Preferences/com.apple.symbolichotkeys.plist를 선택합니다.
   * 해당 파일의 내용 중에서 <key>61</key>을 찾아서 <item 2>786,432</item2>의 <number>131072</number>로 변경하고 파일을 저장합니다.
   * 저장 후에 맥을 재시동하세요.
   
 * 
   
   
   @adhrinae님이 트윗으로 좋은 방법 알려주셔서을 알려주셨는데, 현재(Sonoma)에서는 적용되지 않습니다.
   



필요한 개발 환경 설정



(애증의) Ruby


 * Ruby의 경우 사용하시는 버전이 각자 다르기 때문에 버전 관리자를 먼저 설치하도록 하겠습니다.


$ brew install rbenv



 * .zshrc에 eval "$(rbenv init - zsh)"를 입력해주세요.


// Ruby
$ rbenv install 3.3.5
$ rbenv rehash
$ rbenv global 3.3.5
$ ruby -v
ruby 3.3.5 (2024-09-03 revision ef084cc8f4) [arm64-darwin24]




Haskell


 * 즐거운 프로그래밍 언어인 Haskell도 brew를 사용해서 손쉽게 설치 가능합니다. :D


$ brew install ghcup
$ ghcup install stack 2.9.1
$ ghcup set stack 2.9.1
$ stack ghci






모두 즐거운 개발 되세요!





Appendix



Clean install을 위한 USB 만들기



macOS 다운로드


 * 
   
   
   Ventura를 App Store에서 다운로드 합니다.
   

 * 
   
   
   다운로드가 완료되면 Sonoma 설치 관련(Install macOS Sonoma) 안내 페이지를 확인할 수 있는데, 해당 페이지를 실행하지 말고 닫아주세요(Quit Install macOS).
   






USB 준비


 * 
   
   
   16기가 이상의 USB를 사용하세요. USB를 초기화하기 위해서 App > Other > Disk Utility를 실행해서, Disk Utility의 External 항목에 사용할 USB를 선택하시고 Erase를 선택해서 USB를 초기화 합니다.
   
   
   * USB의 Name은 'macOS-Installer'로 하였고, Format은 'Mac OS Extended (Journaled)'
   
 * 
   
   
   Terminal(혹은 iTerm2 등)을 실행하고 sudo /Applications/Install\ macOS\ Sonoma.app/Contents/Resources/createinstallmedia --volume /Volumes/macOS-Installer/를 실행합니다. createinstallmedia에 관한 내용은 링크를 참고하세요.
   
   
   * sudo는 관리자 권한이 필요하단 뜻으로 해당 명령어를 실행하면 시스템의 비밀번호를 입력해야 합니다.
   * --volume은 USB의 경로(일반적으로 /Volumes/ 아래에 USB의 레이블명(Name)으로 존재합니다)를 적어줍니다.
   






USB를 사용해서 설치하기


Big Sur에서 USB Booting 관련 설정을 하셨다면 아래 USB 부팅 설정은 건너띄고 진행하셔도 됩니다. 만약 이번에 처음 USB로 설치를 진행하신다면 USB 부팅 설정을 확인하세요. 설치시 사용하는 키는 아래 이미지에서 확인하세요.






USB 부팅 설정


 * 컴퓨터를 부팅할 때 복구모드 설정 키(Command + R)을 누르고 있으면 복구 모드로 진행됩니다. 이때, 사용하는 비밀번호는 현재 설치된 운영체제에서 사용하는 비밀번호 입니다. iCloud 관련 비번이 아니니 주의하세요.





 * 복구모드에서 상단의 메뉴바를 선택하고 Utilities > Startup Security Utility를 선택 후, 기존에 사용하시던 macOS의 비밀번호를 입력하면, 옵션이 출력됩니다. 하단에 위치한 Allow booting from external or removable media를 선택하시고, 창을 닫은 후 사과마트를 눌러서 restart를 선택하세요.






USB 부팅


 * 컴퓨터가 새로 시작될 때, Option 키 누르고 있으면, Boot Disk를 선택하는 화면에서 Install macOS Sonoma를 선택하시면 됩니다. 만약 업데이트가 필요하다는 알림창이 안내된다면 업데이트를 진행하세요(A software update is required to use this startup key)





 * Disk Utility를 사용해서 기존에 사용하던 디스크를 Erase를 하시고, Install macOS Sonoma를 사용해서 설치하시면 됩니다.





 * 설치 후 몇번의 재부팅이 되고 난 이후에, 그래픽 화면에서 중요 설정 사항을 입력하는 화면이 진행됩니다. 지역 및 iCloud 등은 안내에 맞춰서 진행하시면 됩니다.
   
   * 저는 개발 환경을 구성하기 기존의 데이터를 마이그레이션(Migration Assistant > Not Now) 하지 않았습니다. 기존에 데이터를 마이그레이션 하셔야 된다면 적절한 옵션을 선택하세요.
   







Updated


 * 2024.10.01
   
   * Sequoia 반영
   
 * 2023.09.27
   
   * Sonoma로 문서 업데이트
   
 * 2022.10.25
   
   * Ventura로 문서 업데이트
   * 이미지 수정 및 M1/M2 사용자를 위한 간단한 가이드 추가
   
 * 2021.10.25
   
   * Monterey로 문서 업데이트
   * 이미지가 없어서 불편하다는 의견을 반영해서, 도움이 될만한 이미지 추가
   
 * 2021.01.12
   
   * brew를 사용해서 pyenv(>=1.2.22) 설치
   * brew를 사용해서 nvm(>=0.37.2) 설치
   
 * 2021.01.02
   
   * pyenv 설치 변경
   * 오타 수정
   
 * 2020.11.14
   
   * Big Sur 변경
   * pyenv 설치 에러 관련해서 설치방법
   
