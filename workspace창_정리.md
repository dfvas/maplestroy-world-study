# 🗂️ Workspace 창 정리

> 메이플 월드 크리에이터 — Workspace(리소스 공간) 구성 요소 학습 정리

---

## 1. BaseEnvironment

메이커가 제공하는 기본 모델과 스크립트가 저장된 공간.  
폴더 순서 변경 및 하위 목록 이동 **불가**.

### 하위 폴더 구조

| 폴더 | 설명 |
|------|------|
| `NativeScripts` | Component, Service, Logic, Event, Misc 하위 폴더 포함 |
| `Component` | 수정·삭제 불가능한 기본 컴포넌트 저장 (확장 사용 가능) |
| `Service` | 기본 서비스 스크립트 저장 (수정·삭제 불가) |
| `Logic` | 기본 로직 스크립트 저장 (수정·삭제 불가) |
| `Event` | 기본 이벤트 스크립트 저장 (수정·삭제 불가) |
| `Misc` | 기타 스크립트 저장 폴더 |
| `NativeModel` | 제공 기본 모델 저장. Scene으로 배치 가능. 확장 모델은 MyDesk에 저장 |

### 주요 컨텍스트 메뉴

| 메뉴 | 설명 |
|------|------|
| `Duplicate` | NativeModel 복제 |
| `Open` | 선택한 항목 열기 |
| `Add Component` | NativeModel에 컴포넌트 추가 |
| `Add New Component` | NativeModel에 새로운 컴포넌트 추가 |
| `Place to Hierarchy` | 선택한 모델을 Scene에 배치 |
| `Extend` | 선택한 모델의 확장 모델 생성 |
| `Copy Entry ID` | 선택한 모델의 ID 복사 |

---

## 2. MyDesk

개발자가 추가한 음악, 스크립트, 이미지 파일, 확장 컴포넌트 등을 관리하는 공간.  
`WorldConfig`에서 월드 설정 변경 가능.

- `UIPopup` : 팝업 메시지 로직 (필요에 따라 수정·삭제 가능)
- `UIToast` : 토스트 메시지 로직 (필요에 따라 수정·삭제 가능)

### 리소스 추가 방법

Workspace 상단의 `[+]` 버튼 클릭

### 주요 컨텍스트 메뉴

| 메뉴 | 설명 |
|------|------|
| `Create Model` | 비어있는 새 모델 생성. 직접 컴포넌트를 추가해서 사용 |
| `Import Scripts` | 스크립트 파일 가져오기 |
| `Import Image` | 이미지 파일 가져오기 |
| `Import Sound` | 사운드 파일 가져오기 |
| `Import Package` | 패키지 가져오기 |

---

## 3. DefaultPlayer

작업 편의를 위해 제공되는 기본 플레이어.  
NativeModel의 Player 정보를 참조하며, **플레이어 아바타 생성 위치 설정**에 사용.

### 주요 컨텍스트 메뉴

| 메뉴 | 설명 |
|------|------|
| `Duplicate` | DefaultPlayer 복제 모델 생성 |
| `Open` | Player의 상태 및 변경점 확인 |
| `Add Component` | DefaultPlayer에 컴포넌트 추가 |
| `Add New Component` | 컴포넌트 생성 후 DefaultPlayer에 추가 |
| `Extend` | DefaultPlayer에 확장 모델 생성 |
| `Copy Entry ID` | DefaultPlayer의 modelID 복사 |

---

## 4. WorldConfig

월드 전체 설정을 변경하는 공간.

| 설정 항목 | 설명 |
|-----------|------|
| `LegacyAnimation` | 캐릭터에 이전 메이플스토리 월드 움직임·애니메이션 적용 |
| `PlayerEntityAuthorityCheck` | 플레이어 엔티티 컴포넌트의 server 함수를 로컬 클라이언트 이외에서 호출 불가로 변경 |
| `ServiceAuthorityCheck` | native에서 동작하는 service 함수들을 serveronly 함수로 동작하도록 변경 |
| `SourceLanguage` | 자동 번역 기준 언어 설정 (예: 한국어, 영어) |
| `RestrictedPlayerEntitySync` | 일부 컴포넌트의 동기화를 제한해 클라이언트 → 서버로 값 전달 차단 |
| `LocalWorkspace` | 월드 데이터를 로컬 PC에 파일 형태로 저장 |
| `WorldOrientation` | 월드 비율 변경 (`Landscape`: 가로, `Portrait`: 세로, `Responsive`: 반응형) |
| `UseLitDefaultMaterial` | 모든 엔티티를 기본적으로 광원 영향을 받는 Lit 모드로 설정 |
