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

![enter_env_02](enter_env_02.png)

![enter_env_03](enter_env_03.png)

![enter_env_04](enter_env_04.png)

![enter_env_05](enter_env_05.png)

![enter_env_06](enter_env_06.png)

![enter_env_07](enter_env_07.png)

![enter_env_08](enter_env_08.png)

이제 확인을 쭉쭉 눌러서 적용을 시켜 줍니다.



다음으로 안드로이드 스튜디오 설치법을 설명하겠습니다.

**https://developer.android.com/studio/install?hl=ko**

위 링크의 가이드를 참고 하여 설치를 하여 줍니다.

그리고 안드로이드 스튜디오를 열고 sdk 설정을 해줍니다.