# Mythores — App Store 제출 작업지시서

이 문서 하나로 **앱 레코드 만들기부터 심사 제출까지** 한 번에 끝나도록 썼습니다.

> **2026-11-07 현재 ASC 상태:** 앱 레코드는 **이미 만들어져 있습니다(앱 ID `6831528188`).** §1은 새로 만들지 말고 **확인만** 하세요.
> 가격(무료)·배포 국가·카테고리·영어(English U.S.) 문구·심사 연락처·저작권도 이미 들어가 있습니다. 해당 절에서는 **값이 아래와 같은지 확인만** 하고 다르면 고치지 말고 앱 담당자에게 알려 주세요.
**§0부터 §12까지 위에서 아래로 순서대로** 하시면 됩니다. 되돌아갈 일은 없습니다.
입력할 값은 전부 이 문서와 이 저장소 안에 있습니다. 새로 지어내야 하는 값은 없습니다.

| 항목 | 값 |
|---|---|
| 앱 이름 | **Mythores: Rare Pet Collector** (영어) · 「Mythores: 희귀 펫 컬렉터」(한국어) |
| Bundle ID | **`com.anotherlevelstudio.mythores`** |
| 위젯 Bundle ID | `com.anotherlevelstudio.mythores.widget` (앱 안에 들어 있음, 따로 등록할 것 없음) |
| 버전 / 빌드 | **1.0.0 (1)** |
| 팀 | **AJUVV9A2NC** (hyeyoung lee) |
| 최소 iOS | 14.0 · **iPhone + iPad 모두 지원** |
| 종류 | 게임 · 무료 · 인앱 결제 없음 · 광고 없음 · 서버 없음 |
| 작성일 | 2026-11-06 (앱 파일·스크린샷 2026-11-07 교체) |

### 진행 상황표 — 끝낸 칸에 ✅를 표시하며 진행하세요

| 절 | 내용 | 걸리는 시간 | 상태 |
|---|---|---|---|
| §0 | 준비물 확인 | 5분 | ⬜ |
| §1 | 앱 레코드 — **이미 있음, 확인만** (앱 ID 6831528188) | 1분 | ⬜ |
| §2 | 빌드(IPA) 업로드 | 10분 + 처리 대기 30분 | ⬜ |
| §3 | 앱 정보 · 카테고리 · 콘텐츠 권한 | 5분 | ⬜ |
| §4 | 연령 등급 | 5분 | ⬜ |
| §5 | 가격 및 배포 국가 | 5분 | ⬜ |
| §6 | 앱 개인정보 | 3분 | ⬜ |
| §7 | 9개 언어 메타데이터 | 40분 | ⬜ |
| §8 | 스크린샷 (별도 문서) | 40분 | ⬜ |
| §9 | 빌드 선택 | 2분 | ⬜ |
| §10 | 심사 정보 | 5분 | ⬜ |
| §11 | 제출 | 3분 | ⬜ |

> **팁:** §2에서 IPA를 올린 뒤 Apple이 처리하는 데 최대 30분이 걸립니다.
> 기다리지 말고 바로 §3 → §8을 채우세요. §9에 도착할 즈음이면 처리가 끝나 있습니다.

---

## 0. 준비물 체크리스트

| # | 준비물 | 어디에 있나 |
|---|---|---|
| 1 | 서명된 IPA 파일 `mythores.ipa` (약 26 MB) | https://github.com/milovane777/mythores-store/releases/tag/v1.0.0-build1 → **Assets** 에서 `mythores.ipa` 클릭 |
| 2 | 스크린샷 (9개 언어 × iPhone·iPad) | 이 저장소 `screenshots/` — 받는 법은 [`스크린샷_업로드_지시서.md`](스크린샷_업로드_지시서.md) |
| 3 | 9개 언어 메타데이터 | 이 저장소 `metadata/<언어>/` — 복사·붙여넣기용 텍스트 파일 |
| 4 | 개인정보 처리방침 URL | `https://milovane777.github.io/mythores-privacy/` |
| 5 | 고객 지원 URL | `https://milovane777.github.io/mythores-privacy/support.html` |
| 6 | Mac + **Transporter** 앱 | Mac App Store에서 「Transporter」 무료 설치 (Apple 공식 앱) |
| 7 | App Store Connect 권한 | 작업자의 Apple ID가 팀 **AJUVV9A2NC**에 **App Manager** 이상 역할로 초대되어 있어야 합니다 |

**시작 전에 꼭 할 것**

1. 4번과 5번 URL을 브라우저에 붙여 넣어 **둘 다 열리는지** 확인합니다.
   열리지 않으면 거기서 멈추고 앱 담당자에게 알려 주세요. 열리지 않는 URL은 **확실한 반려 사유**입니다.
2. https://appstoreconnect.apple.com 에 로그인해서 왼쪽 위 팀 이름이 **hyeyoung lee**인지 확인합니다.
   여러 팀에 속해 있다면 오른쪽 위 이름을 눌러 팀을 바꿉니다.
   **나의 앱** 메뉴가 안 보이거나 **＋** 버튼이 없으면 권한이 부족한 것입니다 → 7번을 앱 담당자에게 요청하세요.

---

## 1. App Store Connect에 앱 레코드 만들기

> ⚠️ **이미 만들어져 있습니다 — 새로 만들지 마세요.** 또 만들면 이름·SKU 중복으로 막히거나 같은 앱이 두 개 생깁니다.
> **나의 앱**에서 앱 ID `6831528188`인 Mythores를 열고, 번들 ID가 `com.anotherlevelstudio.mythores`, 기본 언어가 English (U.S.)인지만 확인한 뒤 **§2로** 가세요.
> 아래 표는 기록용입니다(만들 때 쓴 값).

[appstoreconnect.apple.com](https://appstoreconnect.apple.com) → **나의 앱(Apps)** → 왼쪽 위 **＋** → **신규 앱(New App)**.

| 칸 | 입력값 | 주의 |
|---|---|---|
| 플랫폼 | **iOS** 체크 | |
| 이름 | `Mythores: Rare Pet Collector` | 전 세계에서 유일해야 합니다. 거부되면 **§1-1**로 |
| 기본 언어 | **English (U.S.)** | ⚠️ **한 번 정하면 바꿀 수 없습니다.** 가장 흔한 실수입니다 |
| 번들 ID | `com.anotherlevelstudio.mythores` 선택 | 목록에 없으면 **§1-2**로. `…mythores.widget`을 고르면 **안 됩니다** |
| SKU | `mythores-ios-001` | 내부 관리용. 이 값으로 통일해 주세요 |
| 사용자 액세스 | **전체 액세스** | |

**생성** 클릭 → 앱 페이지가 열리면 성공입니다.
주소창의 `…/apps/` 뒤 숫자(앱 ID, 10자리)를 메모해서 끝나고 앱 담당자에게 알려 주세요.

> **왜 영어가 기본 언어인가:** 번역이 없는 나라(예: 이탈리아, 태국)의 사용자는 기본 언어를 봅니다.
> 앱 안에서도 모르는 언어는 영어로 표시되도록 되어 있어서, 스토어와 앱이 같은 언어로 보입니다.

### 1-1. 이름이 이미 쓰이고 있을 때

아래 순서로 시도하고 **처음 통과한 것**을 씁니다. 어떤 이름이 통과했는지 앱 담당자에게 알려 주세요.

1. `Mythores: Rare Pet Collector`
2. `Mythores: Pet Collector` (23자)
3. `Mythores - Rare Pet Collector` (29자)

이름을 바꿔 쓰게 되면 §7에서 **English (U.S.)의 `name.txt` 대신 통과한 이름**을 넣으세요.
다른 언어의 이름도 같은 이유로 거부되면 해당 언어 이름 뒤에 ` 2`를 붙이지 말고 앱 담당자에게 문의하세요.

### 1-2. 번들 ID가 목록에 없을 때

정상이라면 이미 있습니다(개발 중 자동 서명이 등록함). 없을 때만:

[developer.apple.com → Identifiers](https://developer.apple.com/account/resources/identifiers/list) → **＋** → **App IDs** → **App** → Continue

- Description: `Mythores`
- Bundle ID: **Explicit**, `com.anotherlevelstudio.mythores`
- Capabilities: **App Groups** 하나만 체크 → Configure → `group.com.anotherlevelstudio.mythores` 선택(없으면 같은 이름으로 새로 만듦)
- Continue → Register

App Store Connect 화면을 새로고침하면 목록에 나타납니다.

---

## 2. 빌드(IPA) 업로드 — Transporter 사용

> **2026-11-07 결정: 앱 파일은 앱 담당자(계정 주인)가 직접 올립니다.** 담당자는 이 절을 건너뛰세요. 아래는 앱 담당자용 기록입니다.

1. §0-1의 링크에서 **`mythores.ipa`를 내려받습니다.** (다운로드 폴더에 저장됨)
   - ⚠️ 파일을 **압축 풀거나 이름을 바꾸지 마세요.** 서명이 깨질 수 있습니다.
2. **Transporter** 실행 → App Store Connect와 같은 Apple ID로 로그인
3. `mythores.ipa`를 Transporter 창에 **끌어다 놓기**
4. 목록에 `Mythores 1.0.0 (1)`이 나타나면 오른쪽 **전송(Deliver)** 클릭
5. 초록색 체크와 「전송됨(Delivered)」이 뜨면 끝

업로드 뒤 App Store Connect의 앱 → **TestFlight** 탭에 빌드 **1.0.0 (1)**이 나타나기까지 **5~30분** 걸립니다.
처리가 끝나면 Apple이 이메일을 보냅니다. **기다리지 말고 바로 §3으로 가세요.**

> **암호화(수출 규정) 질문:** 앱에 `ITSAppUsesNonExemptEncryption = NO`가 이미 들어 있어서 **질문이 뜨지 않는 것이 정상**입니다.
> 혹시 TestFlight에 「수출 규정 정보 누락(Missing Compliance)」이 보이면 → 빌드 옆 **관리** →
> 「앱이 암호화를 사용합니까?」에 **아니요**(면제 대상인 표준 암호화만 사용)를 고르세요.
> (앱은 펫 서명 확인과 백업 파일 잠금에 공개 표준 알고리즘만 쓰며, 이는 면제 범위입니다.)

> **IPA를 다시 올려야 하는 경우:** 같은 빌드 번호 `(1)`은 **두 번 올릴 수 없습니다.**
> 다시 올려야 하면 앱 담당자에게 빌드 번호를 올린 새 IPA를 요청하세요.

업로드가 거부되면 **§13 문제 해결**을 보세요.

---

## 3. 앱 정보 (왼쪽 메뉴 일반 → 앱 정보 / App Information)

| 칸 | 입력값 |
|---|---|
| 이름 · 부제 | §7에서 언어별로 넣습니다. 여기서는 English (U.S.)만 보입니다 → `metadata/en-US/name.txt`, `subtitle.txt` |
| 기본 카테고리 | **게임(Games)** → 하위 카테고리 **시뮬레이션(Simulation)**, **캐주얼(Casual)** |
| 보조 카테고리 | **엔터테인먼트(Entertainment)** |
| 콘텐츠 권한(Content Rights) | 「제3자 콘텐츠를 포함하거나 표시합니까?」 → **아니요** |
| 연령 등급 | §4에서 따로 합니다 |

**저장(Save)** 클릭 (오른쪽 위).

> 콘텐츠 권한 근거: 그림·이름·문구가 전부 직접 만든 오리지널입니다. 펫 그림은 직접 그린 픽셀 아트이고
> 다른 회사의 캐릭터·게임을 쓰거나 닮게 만들지 않았습니다.

---

## 4. 연령 등급 (앱 정보 화면의 「연령 등급」 → 편집)

**목표 결과: 4+** (한국 「전체 이용가」에 해당)

질문은 화면 순서대로 나옵니다. 아래 표에 없는 질문은 전부 **없음(None) / 아니요(No)** 입니다.

| 질문(요지) | 답 | 이유 |
|---|---|---|
| 폭력·공포·성적 내용·욕설·약물·음주·흡연 관련 모든 항목 | **없음** | 펫을 돌보는 게임 |
| 의료·치료 정보 / 건강·웰니스 주제 | **없음 / 아니요** | |
| 도박(Gambling) — 실제 돈 | **아니요** | 결제 기능 자체가 없음 |
| 시뮬레이션 도박(Simulated Gambling) | **없음** | 카지노·슬롯 같은 기능 없음 (아래 메모 참고) |
| 콘테스트(Contests) | **아니요** | |
| 무제한 웹 접근(Unrestricted Web Access) | **아니요** | 앱 안에 브라우저 없음 |
| 사용자 생성 콘텐츠(User-Generated Content) | **아니요** | 공개 게시판·피드 없음 |
| 메시지·채팅(Messaging and Chat) | **아니요** | 채팅 기능 없음 |
| 광고(Advertising) | **아니요** | 광고 없음 |
| 자녀 보호 기능 / 연령 확인(Parental Controls / Age Assurance) | **아니요** | |
| 인앱 구매 | **아니요** | |

**완료(Done)** → 결과가 **4+**인지 확인 → 저장.

> **알 뽑기에 대해 (심사에서 물어볼 수 있음):** 알을 깨면 무작위 펫이 나옵니다.
> 하지만 알은 **게임 안에서 얻는 코인으로만** 살 수 있고, **현금으로 코인을 살 방법이 없습니다**(인앱 결제 없음).
> 모든 확률은 앱 안 「부화」 탭의 확률 버튼에서 숫자로 공개됩니다. 그래서 「시뮬레이션 도박」이 아닙니다.
> 만약 질문 목록에 「무작위 아이템/루트 박스(Loot Boxes)」 같은 항목이 따로 있다면 **예**로 정직하게 답하세요 — 등급은 그대로 낮게 나옵니다.

> **「거래」 기능에 대해:** 이 앱에는 거래·판매 기능이 **없습니다.** 펫을 다른 사람에게 보내는 「선물하기」만 있고,
> 두 기기가 QR이나 텍스트 코드를 주고받아 펫 한 마리가 옮겨 갈 뿐 **돈·코인·아이템을 맞바꾸지 않으며 메시지를 주고받는 기능도 없습니다.**
> 그래서 「사용자 생성 콘텐츠」「메시지·채팅」은 **아니요**입니다.

> 4+는 위 답대로 했을 때의 **예상**입니다. 결과가 다르면 고치지 말고 결과 화면을 앱 담당자에게 보내 주세요.

> 결과가 4+가 아니라 9+ 이상으로 나오면 어느 질문을 「예」로 했는지 다시 보세요.
> 위 표대로라면 4+가 나와야 합니다.

---

## 5. 가격 및 배포 (왼쪽 메뉴 가격 및 사용 가능 여부 / Pricing and Availability)

| 칸 | 입력값 |
|---|---|
| 가격 | **무료(Free / USD 0.00)** |
| 사용 가능 국가 | **147개국** — 모든 국가에서 **EU 27개국과 중국 본토를 뺀 것** (이미 설정됨, 확인만) |
| 사전 주문 | 사용 안 함 |
| iPad·Mac·Vision Pro 사용 가능 여부 | **iPhone 및 iPad 앱: Apple Silicon Mac에서 사용 가능 → 체크 해제** (Mac에서 시험하지 않았습니다). Vision Pro도 **체크 해제** |

**저장(Save)** 클릭.

> **왜 중국 본토를 빼나:** 중국 본토 App Store에 게임을 올리려면 중국 정부의 게임 승인 번호(ISBN 판호)가 필요합니다.
> 이 앱은 그 번호가 없으므로, 빼지 않으면 심사가 멈추거나 반려됩니다.
> 간체 중국어(zh-Hans) 페이지는 싱가포르·말레이시아 등에서 그대로 쓰입니다. 번체(zh-Hant)는 대만·홍콩·마카오용입니다.

> **EU(유럽연합)는 이번에 배포하지 않습니다**(앱 담당자 결정). 그래서 「거래자 상태(DSA)」 신고는 이번 제출에 필요 없습니다.
> 그래도 DSA 경고가 뜨면 **임의로 답하지 말고** 앱 담당자에게 알려 주세요. 나머지 작업은 계속해도 됩니다.

---

## 6. 앱 개인정보 (왼쪽 메뉴 앱 개인정보 / App Privacy) — ★ 가장 중요

1. **개인정보 처리방침 URL** 옆 **편집** → `https://milovane777.github.io/mythores-privacy/` → 저장
2. **데이터 수집** 영역의 **시작하기(Get Started)** 클릭
3. 「이 앱에서 데이터를 수집합니까?」 → **아니요, 이 앱에서 데이터를 수집하지 않습니다(No)** → 저장
4. 오른쪽 위 **게시(Publish)** 클릭 → 「데이터가 수집되지 않음」 카드가 보이면 끝

이것이 정확한 답입니다. 근거:

- 서버가 없고, 앱은 어떤 네트워크 요청도 보내지 않습니다
- 분석·광고·크래시 리포트 SDK가 하나도 없습니다
- 계정·로그인이 없습니다
- 앱에 `PrivacyInfo.xcprivacy`(개인정보 매니페스트)가 들어 있고 「수집 없음 · 추적 없음」을 선언합니다

「아니요」를 고르면 상세 항목 입력 화면이 **나오지 않는 것이 정상**입니다.

---

## 7. 9개 언어 메타데이터

왼쪽 메뉴 **iOS 앱 → 1.0 제출 준비 중(1.0 Prepare for Submission)** 을 누르면 버전 페이지가 열립니다.

### 7-1. 언어 추가하는 법

버전 페이지 오른쪽 위 **「English (U.S.) ▾」** 모양의 언어 선택기 → **언어 추가** → 아래 표의 이름을 고릅니다.
언어를 하나 추가할 때마다 그 언어용 입력 칸이 새로 생깁니다. 언어 선택기로 언어를 바꿔 가며 채웁니다.

### 7-2. 넣을 언어와 순서 (위에서부터 채우세요. 위쪽이 더 큰 시장입니다)

| 순 | App Store Connect에서 고를 이름 | 이 저장소 폴더 | 스크린샷 폴더 |
|---|---|---|---|
| 1 | **English (U.S.)** ★기본 언어 | `metadata/en-US/` | `screenshots/en-US/` |
| 2 | **Korean** | `metadata/ko/` | `screenshots/ko/` |
| 3 | **Japanese** | `metadata/ja/` | `screenshots/ja/` |
| 4 | **Chinese (Simplified)** | `metadata/zh-Hans/` | `screenshots/zh-Hans/` |
| 5 | **Chinese (Traditional)** | `metadata/zh-Hant/` | `screenshots/zh-Hant/` |
| 6 | **Spanish (Spain)** | `metadata/es-ES/` | `screenshots/es-ES/` |
| 7 | **Portuguese (Brazil)** | `metadata/pt-BR/` | `screenshots/pt-BR/` |
| 8 | **German** | `metadata/de-DE/` | `screenshots/de-DE/` |
| 9 | **French** | `metadata/fr-FR/` | `screenshots/fr-FR/` |

> - Chinese는 **Simplified와 Traditional 두 개 다** 넣습니다. 앱 안에 두 가지 번역이 다 있습니다.
> - Spanish는 **Spanish (Spain)** 하나만. Portuguese는 반드시 **Brazil**, French는 **French**(France), German은 **German**.
> - 시간이 부족해 중간에 끊어야 하면, **최소한 1번(English)은 완전히 채워야** 제출할 수 있습니다.
>   나머지 언어는 비어 있어도 제출은 됩니다(그 나라에는 영어 페이지가 보임).

### 7-3. 각 언어에서 채울 칸

폴더 안 **파일 이름이 곧 칸 이름**입니다. 파일을 GitHub에서 열고 → 오른쪽 위 **복사 아이콘(Copy raw file)** → 해당 칸에 붙여넣기.

| 파일 | App Store Connect 칸 | 글자 수 제한 | 어디에 있나 |
|---|---|---|---|
| `name.txt` | 이름 (Name) | 30 | **앱 정보** 페이지 (§3과 같은 화면, 언어 선택기로 언어 전환) |
| `subtitle.txt` | 부제 (Subtitle) | 30 | **앱 정보** 페이지 |
| `promotional_text.txt` | 프로모션 텍스트 | 170 | 버전 페이지 |
| `description.txt` | 설명 (Description) | 4000 | 버전 페이지 |
| `keywords.txt` | 키워드 (Keywords) | 100 | 버전 페이지 |

⚠️ **이름과 부제는 버전 페이지가 아니라 「앱 정보」 페이지에 있습니다.** 언어마다 앱 정보 페이지로 가서 언어를 바꾼 뒤 이름·부제를 넣고 저장하세요.

- **모든 파일이 글자 수 제한 안에 들어가는지 미리 검사했습니다.**
- 붙여 넣을 때 **맨 끝 빈 줄**이 같이 들어가도 괜찮습니다.
- 「이 버전의 새로운 기능(What's New)」 칸은 **첫 버전에는 나타나지 않습니다.** 정상입니다.

### 7-4. 모든 언어에 똑같이 넣는 칸 (버전 페이지)

| 칸 | 값 |
|---|---|
| 지원 URL (Support URL) | `https://milovane777.github.io/mythores-privacy/support.html` |
| 마케팅 URL | **비워 두세요** |

### 7-5. 언어와 무관하게 한 번만 넣는 칸 (버전 페이지 아래쪽)

| 칸 | 값 |
|---|---|
| 저작권 (Copyright) | `2026 another_level_studio` (이미 입력됨, 확인만) |
| 버전 (Version) | `1.0.0` (이미 들어 있으면 그대로) |
| 라우팅 앱 범위 파일 | 없음 |
| Game Center | **끄기** (쓰지 않습니다) |

각 언어를 다 채운 뒤 오른쪽 위 **저장(Save)** 을 꼭 누르세요. 저장하지 않고 언어를 바꾸면 입력이 사라질 수 있습니다.

---

## 8. 스크린샷

**스크린샷은 미리 찍어서 이 저장소에 올려 두었습니다. 직접 찍지 마세요.**
받는 법, 칸별 배치, 거부 시 대처까지 적은 전용 문서가 있습니다:

### → [`스크린샷_업로드_지시서.md`](스크린샷_업로드_지시서.md)

요약: 언어마다 **iPhone 6.9형 10장 + iPad 13형 10장**. 9개 언어 모두 그 언어로 찍은 화면이 따로 있습니다.

---

## 9. 빌드 선택

§2에서 올린 빌드가 처리되면(이메일 도착 또는 TestFlight 탭에서 「처리 중」이 사라짐),
버전 페이지(English (U.S.)) 가운데쯤 **「빌드(Build)」** 항목에 **빌드 추가** 버튼이 생깁니다.

1. **빌드 추가** → **1.0.0 (1)** 선택 → **완료**
2. 수출 규정 질문이 뜨면 → **아니요**(§2의 메모 참고)
3. 저장

목록에 빌드가 없으면 아직 처리 중입니다. 몇 분 뒤 새로고침하세요(30분 넘게 없으면 §13).

---

## 10. 심사 정보 (버전 페이지 맨 아래 App Review Information)

| 칸 | 입력값 |
|---|---|
| 로그인 필요(Sign-in required) | **체크 해제** — 계정 기능이 없습니다 |
| 연락처 — 이름(First Name) | `hyeyoung` |
| 연락처 — 성(Last Name) | `lee` |
| 연락처 — 전화번호 | `+821047434164` |
| 연락처 — 이메일 | `milovane7777@gmail.com` |
| 첨부 파일 | 없음 |

### 메모(Notes) 칸 — 아래 상자 안 내용을 **그대로** 복사해 붙여넣으세요

```
Mythores is an offline pet-collecting and pet-care game. There is no account,
no sign-in, no server, no ads and no in-app purchases. Every feature is
available on first launch.

How to see the main features in two minutes:
1. First launch: tap the egg three times to hatch your first pet, then name it.
2. Home tab: tap the care buttons (Feed, Play, Wash, Brush, Tidy up, Sleep).
   Care takes the pet's own time by design (e.g. Sleep takes 45 minutes), and
   each action has a 90-minute cooldown, so buttons show a wait time.
3. Hatch tab: buy another egg with in-game coins (the app starts you with
   enough). The odds icon in the top bar lists every probability.
4. Codex tab: collection grid, seasonal sets, binder and goals.
5. Settings > How to play explains every system in one page.

Notes for review:
- Eggs give a random pet, but they can only be bought with coins earned by
  playing. There is no way to buy coins or anything else with money. All odds
  are disclosed in the app.
- Camera: used only to scan a friend's gift QR code (Gift tab). A gift can also
  be sent as a text code through the system share sheet. Gifting therefore
  needs a second device to complete; it is not required for anything else.
- Photo library (add only): used only when the user saves a card image from
  the share sheet.
- Notifications are local reminders scheduled on the device. Nothing is pushed
  from a server.
- Home Screen widget: shows the pet that needs care. The app writes a small
  file to its own App Group container; the widget reads it. No network.
- Hatch video: a 5-second clip rendered on the device and handed to the share
  sheet. Nothing is uploaded.
- Backup: a password-encrypted file exported through the share sheet and
  restored through the file picker.
- Shared card links point to a static page on GitHub Pages; the pet data is in
  the URL fragment (after #), which browsers never send to the server. The app
  itself makes no network requests. This is why App Privacy says no data is
  collected.
- A pet that receives no care at all for a whole month leaves and becomes a
  memorial card. The last week is clearly warned on the card, in the list and
  by notification, and any single care action resets the clock.

All art, names and text are original to this app.
Contact: milovane7777@gmail.com
```

저장(Save).

### 버전 출시 방식 (같은 페이지 아래)

**「이 버전을 자동으로 출시(Automatically release this version)」** 를 고르세요(앱 담당자 결정).
승인되는 즉시 스토어에 공개됩니다.

---

## 11. 제출

1. 버전 페이지 오른쪽 위 **「심사에 추가(Add for Review)」** 클릭
   - 빨간 경고가 뜨면 어떤 칸이 비었는지 알려 줍니다. 그 칸을 채우고 다시 누르세요(대부분 스크린샷이나 저장 안 한 언어).
2. 다음 화면에서 **「심사에 제출(Submit for Review)」** 클릭
3. 질문이 뜨면:
   - 수출 규정 / 암호화 → **아니요** (§2 메모 참고)
   - 광고 식별자(IDFA) 사용 → **아니요** (광고·추적 SDK 없음)
   - 콘텐츠 권한 → **아니요**(제3자 콘텐츠 없음)

상태가 **「심사 대기 중(Waiting for Review)」** 으로 바뀌면 작업 끝입니다. 보통 **24~48시간** 안에 결과가 나옵니다.

**끝나면 앱 담당자에게 알려 줄 것:** 제출 시각, 스크린샷을 올린 언어, 특이사항. (앱 ID `6831528188`는 이미 알고 있습니다.)

---

## 12. 제출 전 마지막 확인 (1분)

- [ ] 9개 언어 모두 이름·부제·프로모션 텍스트·설명·키워드가 들어가 있고 **저장**했다
- [ ] 9개 언어 모두 iPhone 6.9형 10장, iPad 13형 10장이 있다 (최소한 English는 반드시)
- [ ] 지원 URL이 모든 언어에 들어가 있다
- [ ] 앱 개인정보가 「데이터가 수집되지 않음」으로 **게시**되어 있다
- [ ] 연령 등급 결과가 **4+**
- [ ] 배포 국가가 **147개국**이고 **EU 27개국과 중국 본토가 빠져** 있다
- [ ] 빌드 **1.0.0 (1)** 이 선택되어 있다
- [ ] 심사 메모가 붙어 있고 「로그인 필요」가 해제되어 있다
- [ ] 출시 방식이 **자동**
- [ ] 저작권이 `2026 another_level_studio`

---

## 13. 문제 해결

| 증상 | 원인과 조치 |
|---|---|
| Transporter: 「Invalid Signature」 / 「서명이 유효하지 않음」 | IPA를 다시 내려받으세요. 압축을 풀었다가 다시 묶거나 이름을 바꾸면 서명이 깨집니다 |
| Transporter: 「No suitable application records were found」 | §1의 앱 레코드를 아직 안 만들었거나 다른 번들 ID로 만들었습니다 |
| Transporter: 「The bundle version must be higher than the previously uploaded version」 | 이미 한 번 올라갔습니다. TestFlight 탭을 확인하세요. 다시 올릴 필요 없음 |
| Transporter 로그인이 안 됨 | App Store Connect와 같은 Apple ID인지, 2단계 인증 코드를 받을 기기가 있는지 확인 |
| 빌드가 TestFlight에 30분 넘게 안 보임 | Apple에서 온 「ITMS-…」 이메일을 확인하고 그 내용을 앱 담당자에게 그대로 전달하세요 |
| 「Missing Compliance(수출 규정 누락)」 배너 | 빌드 옆 **관리** → 암호화 질문에 **아니요** |
| 키워드가 「너무 깁니다」 | 일본어·한국어·번체 중국어에서만 생길 수 있습니다. 파일의 **맨 마지막 쉼표 뒤 단어부터** 하나씩 지워 통과시키세요 |
| 이름이 「이미 사용 중」 | §1-1 |
| 스크린샷 「크기가 맞지 않음」 | 다른 폴더의 파일을 올렸습니다. iPhone 칸에는 `iphone-6.9/`, iPad 칸에는 `ipad-13/` |
| 스크린샷 「알파 채널/투명도」 오류 | 저장소의 파일은 모두 불투명으로 변환해 두었습니다. 다른 곳에서 받은 파일인지 확인하세요 |
| 처리방침 URL이 안 열린다고 반려 | GitHub Pages 장애일 수 있습니다. 앱 담당자에게 알려 주세요 |
| 「기본 언어를 잘못 골랐다」 | **되돌릴 수 없습니다.** 앱 담당자에게 알리세요(앱 레코드를 지우고 §1부터 다시) |

### 심사에서 물어볼 가능성이 있는 것과 답

**「알 뽑기가 루트 박스(확률형 아이템) 아닌가?」**
→ 무작위 보상은 맞지만 **현금으로 살 수 없습니다.** 코인은 게임 안에서만 얻고 앱에 결제 기능이 없습니다.
모든 확률이 앱 안에 공개되어 있습니다(부화 탭 → 확률 아이콘).

**「선물 기능을 시험할 수 없다」**
→ 선물은 두 기기가 서로 코드를 주고받아야 끝납니다. 기기가 한 대라면 선물 탭에서 받기 코드 화면과 QR 화면까지만 볼 수 있으며,
선물 없이도 게임의 모든 다른 기능을 쓸 수 있다고 답하세요.

**「데이터를 수집하지 않는다는 게 사실인가?」**
→ 사실입니다. §10 메모의 마지막 부분(카드 링크는 # 뒤에 데이터가 있어 서버로 가지 않음)을 그대로 안내하세요.

**반려(Rejected) 메일이 오면:** 내용을 임의로 고치지 말고 **원문 그대로** 앱 담당자에게 전달해 주세요.

---

## 14. 이 문서의 범위 밖 (작업자 몫 아님)

- 승인 후 공개 — **자동 출시**라 따로 누를 것이 없습니다
- 앱 안 웹 카드 페이지에 App Store 주소를 넣는 일 — 앱 담당자가 합니다
- Google Play(Android) 등록 — 별도 작업이며 이번에는 하지 않습니다
- 이 저장소는 **제출이 끝나면 삭제**합니다
