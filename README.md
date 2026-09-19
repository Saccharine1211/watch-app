# Watch App

Flutter로 만든 시계 기능 프로토타입입니다. 현재는 타이머와 스톱워치 화면의 기본 내비게이션만 구현되어 있으며, 완성된 시계 앱은 아닙니다.

> 상태: 초기 UI 프로토타입

## 현재 구현된 내용

- `MaterialApp` 실행 및 파란색 Material 테마
- 하단 내비게이션: 타이머, 스톱워치, 기록
- 타이머 탭과 스톱워치 탭의 플레이스홀더 화면
- 기록 화면용 `ThirdPage.dart` 파일

## 아직 구현되지 않은 기능

- 카운트다운 타이머
- 스톱워치 동작 및 컨트롤
- 알람 예약
- 세계 시간
- 기록 저장 및 조회
- 영속성, 알림, 사용자 설정

## 알려진 문제

하단 내비게이션에는 세 항목이 있지만 `lib/main.dart`의 페이지 목록에는 두 페이지만 등록되어 있습니다. 따라서 `기록`을 선택하면 세 번째 인덱스를 조회하는 과정에서 오류가 발생할 수 있습니다.

기본 Flutter 카운터 예제 테스트도 남아 있어 현재 UI와 일치하지 않습니다.

## 요구 사항

- Flutter SDK
- `pubspec.yaml`의 Dart 제약과 호환되는 Dart SDK (`>=2.18.4 <3.0.0`)
- Android Studio 또는 Flutter 지원 IDE
- iOS 실행 시 macOS와 Xcode

정확한 Flutter SDK 버전은 저장소에 고정되어 있지 않습니다.

## 지원 플랫폼

저장소에 Android, iOS, Web 프로젝트가 포함되어 있습니다. Windows, macOS, Linux 데스크톱 프로젝트는 포함되어 있지 않습니다.

## 시작하기

```bash
git clone https://github.com/Saccharine1211/watch-app.git
cd watch-app
flutter pub get
flutter run
```

특정 대상으로 실행하려면 다음처럼 사용할 수 있습니다.

```bash
flutter run -d chrome
flutter run -d android
flutter run -d ios
```

## 테스트

```bash
flutter test
```

현재 `test/widget_test.dart`는 기본 Flutter 카운터 앱 테스트이므로 실제 애플리케이션을 검증하지 않습니다.

## 구조

```text
lib/
├── main.dart
└── screen/
    ├── FirstPage.dart
    ├── SecondPage.dart
    └── ThirdPage.dart
android/
ios/
web/
test/
pubspec.yaml
```

## 의존성

- `flutter`
- `intl`
- `cupertino_icons`
- 개발 의존성: `flutter_test`, `flutter_lints`

## 라이선스

저장소에 라이선스가 명시되어 있지 않습니다.
