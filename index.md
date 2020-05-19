이문서는 react native docs의 environment setup을 참고 하고 있습니다.



우선 react native를 개발하기 위해서는 

JDK8 ,PYTHON2 , node js, android studio , android sdk가 필요합니다.

우선 choco를 인스톨 해줍니다.

cmd를 관리자 권한으로 열어 줍니다.

그리고 다음의 명령어를 입력 합니다.

```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command " [System.Net.ServicePointManager]::SecurityProtocol = 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```

이후 cmd에 이것을 입력하여 nodejs python2 jdk8를 설치 합니다.

```
choco install -y nodejs.install python2 jdk8
```

그리고 java 환경설정을 해줍니다.

![enter_env_01](enter_env_01.png)

![enter_env_02](enter_env_02.PNG)

![enter_env_03](enter_env_03.PNG)

![enter_env_04](enter_env_04.PNG)

![enter_env_05](enter_env_05.PNG)

![enter_env_06](enter_env_06.PNG)

![enter_env_07](enter_env_07.PNG)

![enter_env_08](enter_env_08.PNG)

이제 확인을 쭉쭉 눌러서 적용을 시켜 줍니다.



다음으로 안드로이드 스튜디오 설치법을 설명하겠습니다.

[https://developer.android.com/studio/install?hl=ko](https://developer.android.com/studio/install?hl=ko)



위 링크의 가이드를 참고 하여 설치를 하여 줍니다.

그리고 안드로이드 스튜디오를 열고 sdk 설정을 해줍니다.

![android_studio00](android_studio00.PNG)

![android_studio01](android_studio01.png)

![android_studio02](android_studio02.PNG)

![android_studio03](android_studio03.PNG)

![android_studio4](android_studio04.PNG)

둘중 1나 선택해서 적용해 줍니다.



이후에 안드로이드sdk 환경 변수 설정을 하여 줍니다.

안드로이드 sdk 환경변수 설정은 

![android_env01](android_env01.PNG)

여기에서 안드로이드 sdk위치는 c:\user\(사용자명)\AppData\Local\Android\Sdk입니다.

![android_env02](android_env02.PNG)

%ANDROID_HOME%\tools\bin과

%ANDROID_HOME%platform-tools를 path에 추가 합니다.

이제 사전에 필요한 준비는 다 끝났습니다.

이제 원하는 디렉토리에 들어가서 

```shell
npx react-native init 프로젝트명
```

명령어를 실행하여 프로젝트를 생성 합니다.

프로젝트를 생성하면 프로젝트명으로 디렉토리가 생성됨니다.

![create_prj](create_prj.PNG)

이제 안드로이드 디바이스를 연결 합니다. (usb 디버깅으로 연결)

또는 안드로이드 스튜디오에서 안드로이드 가상며신을 설정

이제 프로젝트 폴더에서 다음 명령어를 실행 합니다.

```shell
npx react-native run-android
```

![create_prj2](create_prj2.PNG)

이제 샘플이 실행 됩니다.

![sample_android](sample_android.jpg)

이제 부터 안드로이드 apk를 뽑는 법을 설명하겠습니다.

안드로이드 스튜디오를 실행합니다.

existing android studio project 를 클릭합니다.

![apk_out](apk_out.PNG)

프로젝트 안의 android폴더를 선택 합니다.

![apk_out1](apk_out1.PNG)

![apk_out2](apk_out2.PNG)

몇개의 프로세스가 전부 실행될때 까지 기다림니다.

![apk_out3](apk_out3.png)

프로젝트를 make합니다.

![apk_out4](apk_out4.png)

generate signed bundle / APK를 선택 합니다.

![apk_out5](apk_out5.PNG)

next를 선택 합니다.

![apk_out6](apk_out6.PNG)

key store를 선택하거나 새로 만듬니다.

기존에 key store가 있다면 하지 안아도 됨니다.

![apk_out7](apk_out7.PNG)

저는 테스트용으로 아무렇게나 생성 하겠습니다. 하지만 앱을 실제 배포하는 경우에는 신중히 적어야 합니다.

![apk_out8](apk_out8.PNG)

키스토어를 입력하고 next를 선택합니다.

![apk_out9](apk_out9.PNG)

다음으로 릴리즈를 선택하고 signature versions을 선택하고 finish를 선택합니다. 이제 그럼 안드로이드 스튜디오에서 빌드를 실행합니다.

![apk_out10](apk_out10.PNG)

빌드가 되고나면 프로젝트경로\android\app\release에 app-release가 생성이 됩니다.