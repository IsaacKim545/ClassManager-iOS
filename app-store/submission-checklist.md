# 제출 전 최종 체크리스트 — 담임노트 iOS

## 1. 공개 URL (가장 먼저)

- [ ] GitHub Pages 배포 완료 후 세 주소가 모두 열리는지 확인
  - [ ] `https://isaackim545.github.io/ClassManager-iOS/`
  - [ ] `https://isaackim545.github.io/ClassManager-iOS/privacy.html`
  - [ ] `https://isaackim545.github.io/ClassManager-iOS/support.html`
- [ ] 개인정보 처리방침과 지원 페이지의 **문의 이메일이 실제 수신 가능한
      주소**인지 확인 (심사팀이 실제로 확인합니다)
- [ ] 페이지에 미치환 자리표시자(대문자 CONTACT + EMAIL 형태)가 남아 있지 않은지 확인

## 2. 빌드

- [ ] `app.json` 버전 확인 — `version: 2.2.0`, `ios.buildNumber: 20`
- [ ] 빌드 번호가 이전 제출본보다 큰 값인지 확인 (같으면 업로드 거부)
- [ ] `npx expo-doctor` 통과
- [ ] `npm run typecheck` 통과
- [ ] `eas build --platform ios --profile production` 실행
- [ ] `eas submit --platform ios` 또는 Transporter로 업로드
- [ ] App Store Connect에 빌드가 "처리 완료" 상태로 표시되는지 확인

## 3. 실기기 확인

- [ ] iPhone에서 첫 실행 → PIN 설정 → 복구 코드 확인 흐름 정상 동작
- [ ] **iPad에서 레이아웃 깨짐 없음** (`supportsTablet: true` 이므로 필수 확인)
- [ ] 가로/세로 회전 시 화면 정상
- [ ] 학급 생성 → 학생 추가 → 출석 → 상담 → 기록 전체 흐름 동작
- [ ] Excel / JSON 내보내기 및 복구 동작
- [ ] ATT 안내에서 **"추적 요청 안 함"을 선택해도 모든 기능이 동작**하는지 확인
- [ ] Face ID 켜고 끄기 정상 동작
- [ ] 광고 배너가 콘텐츠나 버튼을 가리지 않는지 확인
- [ ] 빈 상태(학생 0명, 기록 0건) 화면이 비어 보이지 않고 안내가 표시되는지 확인

## 4. App Store Connect 입력

- [ ] 앱 이름 / 부제 / 설명 / 키워드 / 프로모션 텍스트
      → [`app-store-connect-metadata.md`](./app-store-connect-metadata.md)
- [ ] 개인정보 처리방침 URL, 지원 URL, 마케팅 URL 입력
- [ ] 카테고리: 교육 / 생산성
- [ ] 저작권: `2026 담임노트`
- [ ] 연령 등급 설문 — **"부적절할 수 있는 광고 포함: 예"** 로 답변
- [ ] App Privacy 라벨 입력
      → [`app-privacy-details.md`](./app-privacy-details.md)
- [ ] 앱 심사 정보 비고란에 영문 메모 붙여넣기
      → [`review-notes.md`](./review-notes.md)
- [ ] 로그인 필요 여부: **아니요**
- [ ] 연락처 이름·전화번호·이메일 입력

## 5. 스크린샷

- [ ] iPhone 6.9" (1320×2868 또는 1290×2796) — 4~6장
- [ ] iPad 13" (2064×2752 또는 2048×2732) — 4~6장
- [ ] 실제 앱 화면만 사용 (기기 프레임 합성·모의 화면 금지)
- [ ] 개인정보가 드러나는 실제 학생 이름 대신 예시 이름 사용
- [ ] 광고 영역이 캡처에 포함되지 않도록 정리

## 6. 규정 관련

- [ ] 수출 규정: `ITSAppUsesNonExemptEncryption: false` (`app.json`에 설정됨)
- [ ] 콘텐츠 권리: 제3자 콘텐츠 미포함
- [ ] 광고 식별자(IDFA) 사용 여부: **예** — "앱 내 광고 게재" 항목 체크
- [ ] 대한민국 외 판매 지역 설정 확인

## 7. 제출

- [ ] 자동 릴리스 / 수동 릴리스 선택
- [ ] 심사 제출 후 상태 알림 확인
- [ ] 반려 시 Resolution Center 답변에 이 문서의 근거를 그대로 인용

---

### 반려 대비 요약 문장

> 담임노트는 계정이 없는 교사용 로컬 업무 도구이며, 모든 학급 자료는 기기 내
> SQLite에만 저장되고 서버로 전송되지 않습니다. 첫 화면의 PIN 입력은 로그인이
> 아니라 사용자가 직접 만드는 기기 내 앱 잠금입니다. 광고 식별자는 ATT 동의
> 이후에만 사용하며, 추적을 거부해도 모든 기능을 사용할 수 있습니다.
