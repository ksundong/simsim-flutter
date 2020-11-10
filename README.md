# 잠이안와서 해보는 플러터

## MacOS에서 해보자

1. Flutter SDK 다운로드는 간단하게 `brew install flutter`

2. `flutter precache`로 개발 바이너리 사전 다운로드(Optional)

   잘 보면 정보수집을 한다. 개인의 자유~ 특이한건 Dart SDK도 포함하고 있어서 그것도 같이 보낸다고 한다.
   `flutter config`로 설정정보를 볼 수 있다.
   `flutter config --no-analytics`로 해제가능하다.

3. `flutter doctor` 플랫폼 의존성이 있는지 확인 `-v` 플래그로 상세 출력

   ```
   Doctor summary (to see all details, run flutter doctor -v):
   [✓] Flutter (Channel stable, 1.22.3, on macOS 11.0 20A5395g, locale en-KR)
   [✗] Android toolchain - develop for Android devices
       ✗ Unable to locate Android SDK.
         Install Android Studio from: https://developer.android.com/studio/index.html
         On first launch it will assist you in installing the Android SDK components.
         (or visit https://flutter.dev/docs/get-started/install/macos#android-setup for detailed instructions).
         If the Android SDK has been installed to a custom location, set ANDROID_SDK_ROOT to that location.
         You may also want to add it to your PATH environment variable.
   
   [!] Xcode - develop for iOS and macOS (Xcode 12.1)
       ✗ CocoaPods not installed.
           CocoaPods is used to retrieve the iOS and macOS platform side's plugin code that responds to your plugin usage on the Dart side.
           Without CocoaPods, plugins will not work on iOS or macOS.
           For more info, see https://flutter.dev/platform-plugins
         To install:
           sudo gem install cocoapods
   [!] Android Studio (not installed)
   [!] IntelliJ IDEA Ultimate Edition (version 2020.2.3)
       ✗ Flutter plugin not installed; this adds Flutter specific functionality.
       ✗ Dart plugin not installed; this adds Dart specific functionality.
   [!] VS Code (version 1.51.0)
       ✗ Flutter extension not installed; install from
         https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter
   
   [!] Connected device
       ! No devices available
   
   ! Doctor found issues in 6 categories.
   ```

   난 이렇게 나왔다.

   받아야 할 게 엄청 많다.

   ```
   Doctor summary (to see all details, run flutter doctor -v):
   [✓] Flutter (Channel stable, 1.22.3, on macOS 11.0 20A5395g, locale en-KR)
   [✓] Android toolchain - develop for Android devices (Android SDK version 30.0.2)
   [✓] Xcode - develop for iOS and macOS (Xcode 12.1)
   [!] Android Studio (version 4.1)
       ✗ Flutter plugin not installed; this adds Flutter specific functionality.
       ✗ Dart plugin not installed; this adds Dart specific functionality.
   [✓] IntelliJ IDEA Ultimate Edition (version 2020.2.3)
   [✓] VS Code (version 1.51.0)
   [!] Connected device
       ! No devices available
   ```

   안드로이드 스튜디오는 다 설치했는데 안됐다고 나온다. 여튼 다했다.

4. 테스트를 위해서 간단한 앱을 만들고 실행해보자
   1. `flutter create my_app` 을 실행해 새로운 Flutter 앱을 만든다.
   2. `open -a Simulator` 로 시뮬레이터를 실행시킨다.
      **Hardware > Device** 로 가서 64비트 기기(iPhone 5s 이상)인지 확인한다.
      화면 크기에 따라서 화면보다 커질 수 있으므로 **Window > Scale** 메뉴에서 조정한다.
   3. `flutter run` 을 한다. 이 때, 시뮬레이터가 실행중이 아니면, 기기를 찾을 수 없다고 나온다.
      컴파일하고 링크하는게 조금 걸린다.
      바로 디버그 모드로 들어가는게 특이하다.

> 번역이 되어있는건 좋은데 오타가 좀 많은 편이다.

5. 안드로이드는 굳이 안만들었다. 어차피 기계가 없어서 테스트도 못함.

# my_app

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
