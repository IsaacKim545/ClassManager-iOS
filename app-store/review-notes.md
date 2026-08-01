# 앱 심사 정보 — 심사팀 전달 메모

App Store Connect > 앱 심사 정보 > **비고(Notes)** 란에 아래 영문 내용을
붙여넣으세요. 심사는 영어로 진행되므로 영문본이 기본이고, 국문본은 검토용입니다.

- **로그인 필요 여부:** 아니요 (데모 계정 불필요)
- 앱을 처음 실행하면 사용자가 직접 PIN을 설정하는 화면이 나타납니다. 심사자가
  임의의 PIN을 설정하면 바로 앱을 사용할 수 있습니다. **이 점을 반드시 메모에
  적어야 합니다.** 잠금 화면을 로그인 화면으로 오인해 "계정 정보 누락"으로
  반려되는 사례가 있습니다.

---

## 영문 (App Store Connect에 입력)

```
No account or sign-in is required to use this app. All features are available immediately.

FIRST LAUNCH — APP LOCK SETUP
On first launch the app asks you to create a local app-lock PIN. This is NOT a login
screen and it is not connected to any server. Please choose any 4-digit PIN (for
example 1234), confirm it, and store the recovery code shown on the next screen.
After that the app opens directly to the home dashboard. Face ID can be enabled later
in Settings, but it is optional.

HOW TO TRY THE APP
1. Set a PIN on first launch as described above.
2. Go to the Settings tab and create a class (school / grade / class name).
3. Go to the Students tab and add one or more students.
4. The Attendance, Counseling and Records tabs then become usable for those students.
   The Home tab shows today's attendance summary and pending counseling follow-ups.
5. Settings also contains Excel / JSON backup export and a full reset option.

DATA HANDLING
All class, student, attendance, counseling and record data is stored locally in an
on-device SQLite database. Nothing is uploaded to our servers — we operate no backend.
Backup files (Excel / JSON) are created only when the user explicitly taps export, and
the user chooses where to save them. Deleting the app removes all local data, and
Settings > Reset erases everything immediately. Because the app has no accounts, the
account-deletion requirement (Guideline 5.1.1(v)) does not apply; this is stated in
our privacy policy.

ADVERTISING AND TRACKING
The app displays Google AdMob banner ads. Before requesting the advertising identifier
we present the App Tracking Transparency prompt (expo-tracking-transparency). If the
reviewer declines tracking, every feature of the app still works without restriction.
Ads are the only reason any data leaves the device.

INTENDED USERS
The app is a work tool for homeroom teachers, not for children. Teachers enter their
own class records. The app is rated 4+ and contains no user-generated content sharing,
messaging, social features, or web browsing.

ENCRYPTION
The app uses only standard iOS encryption. ITSAppUsesNonExemptEncryption is set to
false in Info.plist.

CONTACT
Privacy policy: https://isaackim545.github.io/ClassManager-iOS/privacy.html
Support: https://isaackim545.github.io/ClassManager-iOS/support.html
```

---

## 국문 (검토용)

```
이 앱은 회원가입이나 로그인이 필요하지 않으며, 모든 기능을 바로 사용할 수 있습니다.

[첫 실행 — 앱 잠금 설정]
처음 실행하면 기기 안에서만 쓰이는 앱 잠금 PIN을 설정하는 화면이 나타납니다.
로그인 화면이 아니며 서버와 연결되지 않습니다. 임의의 네 자리 PIN(예: 1234)을
설정하고 다음 화면의 복구 코드를 보관하면 바로 홈 화면으로 이동합니다.
Face ID는 설정에서 선택적으로 켤 수 있습니다.

[사용 순서]
1. 첫 실행 시 PIN 설정
2. 설정 탭에서 학급(학교·학년·반) 생성
3. 학생 탭에서 학생 추가
4. 출석·상담·기록 탭 사용, 홈 탭에서 오늘 현황 확인
5. 설정 탭에서 Excel·JSON 백업 내보내기 및 전체 초기화

[데이터 처리]
모든 학급·학생·출석·상담·기록 자료는 기기 내 SQLite에 저장되며 서버로 전송되지
않습니다(백엔드 없음). 백업 파일은 사용자가 직접 내보낼 때만 생성됩니다. 앱 삭제
또는 설정의 전체 초기화로 모든 자료가 즉시 삭제됩니다. 계정 기능이 없으므로
계정 삭제 요구사항(가이드라인 5.1.1(v))은 해당하지 않습니다.

[광고와 추적]
Google AdMob 배너 광고를 표시하며, 광고 식별자 사용 전에 ATT 동의 안내를
표시합니다. 추적을 허용하지 않아도 모든 기능을 제한 없이 사용할 수 있습니다.

[대상 사용자]
담임 교사의 업무 도구이며 아동을 대상으로 하지 않습니다. 콘텐츠 공유, 메시지,
소셜 기능, 웹 브라우징 기능이 없습니다. 연령 등급 4+.

[암호화]
표준 iOS 암호화만 사용하며 ITSAppUsesNonExemptEncryption = false 입니다.
```

## 자주 반려되는 항목과 대응

| 가이드라인 | 위험 | 대응 |
| --- | --- | --- |
| 2.1 App Completeness | PIN 화면을 로그인으로 오인 | 위 메모의 첫 실행 안내로 설명 |
| 5.1.1 Data Collection | 학생 정보 수집 오해 | 기기 내 저장·서버 없음 명시 |
| 5.1.1(v) 계정 삭제 | 계정 삭제 경로 요구 | 계정 기능 없음 + 전체 초기화 안내 |
| 5.1.2 ATT | 추적 거부 시 기능 제한 | 거부해도 전 기능 사용 가능 명시 |
| 1.3 Kids Category | 아동 대상 앱 오해 | 교사용 업무 도구임을 명시, 키즈 카테고리 미선택 |
| 4.0 Design | iPad 레이아웃 깨짐 | iPad 스크린샷·실기기 확인 필수 |
