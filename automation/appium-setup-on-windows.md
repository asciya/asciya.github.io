# Appium SetUp (On Windows)

## Java JDK 설치

Oracle 사이트에서 JDK Windows 버전을 다운로드 합니다.

(http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

jdk 설치 완료 되었다면 java 버전을 확인할 수 있습니다.

Java 설치 완료 후, 환경 변수 JAVA\_HOME을 추가 지정해줍니다.

시스템 속성 > 환경 변수 > 시스템 변수 - 새로 만들기 클릭하여 JAVA\_HOME을 추가해줍니다.

시스템 변수 - Path 에도 java 경로 ( %JAVA\_HOME%\bin ) 를 추가해줍니다.

## Android Studio 설치

Android Studio 사이트에서 Android Studio를 다운로드 합니다.

(https://developer.android.com/studio)

설치 완료 후 시작 화면 아래의 Configure를 클릭하여 SDK Manager를 실행시킵니다.

해당 화면에서 Android SDK Location 값을 확인하고 복사해둡니다

SDK Tools 탭에서 Appium에서 사용할 SDK와 Tool을 선택하고 설치합니다

* Android Emulator
* Android SDK Platform-Tools
* Android SDK Tools
* Google Play Licensing Library
* Google USB Driver

SDK Platforms 탭에서 Android 버전에 맞는 API를 선택하고 설치합니다

필요한 Tool과 SDK 체크 후 OK 버튼을 클릭하여 설치합니다

설치 완료 후, 환경 변수 ANDROID\_HOME을 추가 지정해줍니다.

시스템 속성 > 환경 변수 > 시스템 변수 - 새로 만들기 클릭하여 ANDROID\_HOME을 추가해줍니다.

변수 값은 복사해둔 Android SDK Location 값을 사용합니다.

시스템 변수 - Path 에도 Android 경로를 추가해줍니다.

* %ANDROID\_HOME%\emulator
* %ANDROID\_HOME%\tools
* %ANDROID\_HOME%\platform-tools

## Appium 설치

Appium 사이트에서 Appium을 다운로드 후, 파일을 실행하여 설치를 완료합니다.

(https://appium.io)

## Node.js 설치

Node.js 사이트에서 Node.js를 다운로드 합니다.

(https://nodejs.org/en/download/)

node 설치 완료 되었다면 node 버전을 확인할 수 있습니다.

Appium 실행을 위해 Appium 내 main.js 파일 위치로 이동하여 명령 프롬프트를 실행 > node를 이용하여 main.js를 실행합니다

```
node main.js -a 127.0.0.1 -p 4723
```

여러개의 명령 프롬프트를 실행하여 여러개의 Appium을 띄울 수 있습니다.

## appium-doctor 설치

appium-doctor는 appium을 사용하려면 여러 설정이 필요하며 해당 설정이 정상적으로 이루어져있는지 확인해주는 툴입니다.

하단 명령어 입력을 통해 npm으로 appium-doctor를 설치합니다.

```
npm install -g appium-doctor
```

appium-doctor 설치 후 명령어 입력을 통해 의존성을 확인합니다.

확인 항목들은 다음과 같습니다.

* Necessary
  * Node.js 설치
  * ANDROID\_HOME 시스템 변수 설정
  * JAVA\_HOME 시스템 변수 설정
  * adb, android, emulator 확인 jdk bin 폴더 확인
* Optional
  * opencv4nodejs 설치
  * ffmpeg 설치
  * mjpeg-consumer 설치
  * bundletool.jar 설치
  * gst-launch-1.0 and gst-inspect-1.0 설치

### ffmpeg 설치

> FFmpeg 사이트에서 FFmpeg Windows builds 버전을 다운로드 합니다.
>
> (https://ffmpeg.org/download.html)
>
> FFmpeg 설치 완료 후, 시스템 변수 - Path 에도 FFmpeg 설치 경로를 추가해줍니다.

### mjpeg-consumer 설치

> 하단 명령어 입력을 통해 npm으로 mjpeg-consumer를 설치합니다.
>
> ```
> npm install -g mjpeg-consumer
> ```

### bundletool 설치

> Google Bundletool Github 저장소에서 bundletool release jar 파일을 다운로드 합니다.
>
> (https://github.com/google/bundletool/releases)
>
> 다운로드 받은 jar 파일 이름을 bundletool.jar 로 변경 후, 시스템 변수 - Path 에도 bundletool 설치 경로를 추가해줍니다.
>
> 시스템 변수 - PATHEXT 에 JAR 확장자를 추가해줍니다.

### gst-launch-1.0 및 gst-inspect-1.0 설치

> GStreamer 사이트에서 Gstreamer Windows builds 버전을 다운로드 합니다.
>
> (https://gstreamer.freedesktop,org/download)
>
> GStreamer 설치 완료 후, 시스템 변수 - Path 에도 GStreamer 설치 경로를 추가해줍니다.

### opencvc4nodejs 설치

> Git 사이트에서 Git Windows 버전을 다운로드 및 설치합니다.
>
> (https://git-scm.com/downloads)
>
> cmake 사이트에서 cmake release 버전을 다운로드 및 설치합니다.
>
> (https://cmake.org/download)
>
> cmake 설치 완료 되었다면 cmake 버전을 확인할 수 있습니다.
>
> Mac 운영체제에서 Homebrew와 같은 역할을 하는 Chocolatey를 설치합니다.
>
> (https://chocolatey.org/install)
>
> Windows Powershell을 관리자로 실행하고 하단의 명령어를 입력합니다.
>
> ```
> Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
> ```
>
> choco 설치 완료 되었다면 choco 버전을 확인할 수 있습니다.
>
> choco를 이용하여 OpenCV를 설치합니다.
>
> ```
> choco install OpenCV -y -version 4.1.0
> ```
>
> OpenCV 설치 완료 후, 시스템 변수 - Path 에 %OPENCV\_BIN\_DIR% 를 추가해줍니다.
>
> 시스템 환경 변수를 추가 3개를 생성합니다.
>
> * OPENCV\_INCLUDE\_DIR 라는 환경변수를 새로 생성하고 값은 OPENCV를 깔때 경로를 따로 지정하지않았다면 C:\tools\opencv\build\include 로 설정합니다.
> * OPENCV\_LIB\_DIR 라는 환경변수를 새로 생성하고 값은 C:\tools\opencv\build\x64\vc15\lib (기본경로)로 설정합니다.
> * OPENCV\_BIN\_DIR 라는 환경변수를 새로 생성하고 값은 C:\tools\opencv\build\bin (기본경로)로 설정합니다.
>
> npm을 이용하여 opencv4nodejs를 설치합니다
>
> ```
> npm install -g opencv4nodejs --ignore-scripts
> ```
