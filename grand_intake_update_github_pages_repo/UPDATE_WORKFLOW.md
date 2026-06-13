# 업데이트 운영 방법

## 새 버전 배포 순서

예: v18.9 배포 시

### 1. Android Studio에서 release APK 빌드

반드시 기존 앱과 같은 keystore로 서명해야 합니다.

### 2. 파일명 변경

```text
app-release.apk
→ grand-intake-v18.9.apk
```

### 3. GitHub에 APK 업로드

```text
apk/grand-intake-v18.9.apk
```

### 4. version.json 수정

```json
{
  "versionName": "18.9",
  "versionCode": 189,
  "apkFileName": "grand-intake-v18.9.apk",
  "apkUrl": "https://YOUR_GITHUB_ID.github.io/grand-intake-update/apk/grand-intake-v18.9.apk",
  "releaseNote": "수정내용 입력",
  "required": false
}
```

### 5. 태블릿에서 업데이트

앱에 업데이트 기능이 들어간 후에는:

```text
앱 실행
→ OneDrive 설정 또는 관리자
→ 최신 버전 확인
→ 다운로드
→ 설치하기
```

## 버전 규칙

```text
v18.8 → versionCode 188
v18.9 → versionCode 189
v19.0 → versionCode 190
```

## 주의

- APK는 공개 주소로 접근 가능할 수 있습니다.
- 환자 데이터는 절대 업로드하지 마세요.
- release APK는 기존과 같은 keystore로 서명해야 덮어설치됩니다.
