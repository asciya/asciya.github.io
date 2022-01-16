# Appium SetUp (On MacOS)

## 터미널을 Bash로 변경

> ```
> $ chsh -s /bin/bash
> ```

원상복구 필요 시,

> ```
> $ chsh -s /bin/zsh
> ```

## Homebrew 설치

```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

비밀번호 입력 > 설치 완료 후, 터미널 재실행

## Java JDK 설치

cask 설치

> ```
> $ brew install cask
> ```

acceptopenjdk8을 설치

> ```
> $ brew install --cask adoptopenjdk/openjdk/adoptopenjdk8
> ```

JAVA\_HOME 설정

> ```
> $ nano .bash_profile
> ```
>
> > ```
> >  export JAVA_HOME=$(/usr/libexec/java_home)
> > ```
>
> ```
> $ source ~/.bash_profile
> $ echo $JAVA_HOME
> /Library/Java/JavaVirtualMachines/adoptopenjdk-8.jdk/Contents/Home
> ```

## Android Studio 설치

1. 안드로이드 개발자 사이트(https://developer.android.com/studio) 접속
2. Mac 버전 안드로이드 스튜디오 다운로드
3. 다운로드 약관 동의
4. 파일 다운로드 후 실행 & 설치
5. 프로그램 실행 > 안드로이드 스튜디오 설정

ANDROID\_HOME 설정

> ```
> $ nano .bash_profile
> ```
>
> > ```
> > export ANDROID_HOME=/Users/$USER/Library/Android/sdk/
> > export PATH=$PATH:$ANDROID_HOME
> > export PATH=$PATH:$ANDROID_HOME/tools
> > export PATH=$PATH:$ANDROID_HOME/platform-tools
> > ```
>
> ```
> $ source ~/.bash_profile
> $ echo $ANDROID_HOME
> /Users/$USER/Library/Android/sdk/
> ```

## Xcode 설치

1. http://developer.apple.com/download/more 접속 (Apple ID 로그인)
2. 다운받을 Xcode 버전 압축파일 다운로드
3. 압축 파일 실행 후 압축 해제된 Xcode 파일을 응용프로그램 폴더로 복사 & 실행
4. Xcode 실행 > Preferences > Locations > Command Line Tools 선택

## xcode-select 설치

```
$ xcode-select -p
/Applications/Xcode.app/Contents/Developer
```

없다면

```
$ xcode-select --install
```

설치 후, 라이선스 수락

```
$ sudo xcodebuild -license accept
```

## node.js 설치

```
$ brew install node
```

## Appium 설치

```
$ npm i -g appium
```

## Appium Client 설치

```
$ npm i wd
```

## Appium-Doctor 설치

```
$ npm i -g appium-doctor
```

### Carthage 설치

> ```
> $ brew install carthage 
> ```

### ffmpeg 설치

> ```
> $ brew install ffmpeg
> ```

### mjpeg-consumer 설치

> ```
> $ npm i -g mjpeg-consumer
> ```

### set-simulator-location 설치

> ```
> $ brew install lyft/formulae/set-simulator-location
> ```

### applesimutils 설치

> ```
> $ brew tap wix/brew && brew install applesimutils
> ```

### ios-deploy 설치

> ```
> $ npm install -g ios-deploy
> $ sudo gem install xcpretty
> ```

### gst-launch-1.0 and gst-inspect-1.0 설치

> ```
> $ brew install gstreamer gst-plugins-base gst-plugins-good gst-plugins-bad gst-plugins-ugly gst-libav
> ```

### opencv4nodejs 설치

> ```
> $ brew install cmake && npm install -g opencv4nodejs --ignore-scripts
> ```

### idb & idb\_companion 설치

> ```
> $ brew tap facebook/fb && brew install fbsimctl -- HEAD
> $ brew tap facebook/fb && brew install idb
> $ sudo pip3.10 install fb-idb
> ```

### bundletool.jar 설치

> 폴더 생성
>
> ```
> $ mkdir `~/Library/Android/sdk/bundle-tool`
> ```
>
> 생성한 폴더로 **bundletool.jar** 다운로드 (https://github.com/google/bundletool/releases)
>
> 권한 추가
>
> ```
> $ chmod +x bundletool.jar
> ```
