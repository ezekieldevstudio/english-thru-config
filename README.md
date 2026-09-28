# English Thru Support

한국어 공개 정책·지원 페이지입니다. HTML/CSS만 사용하며 설치나 빌드 과정이 없습니다.

- `index.html`: 지원 홈
- `privacy.html`: 개인정보처리방침
- `delete-account.html`: 계정 삭제 요청 안내
- `terms.html`: 이용약관
- `faq.json`, `notice.json`: 초기 FAQ·공지 (기존 파일명과 배열 형식 유지)
- `styles.css`: 공통 반응형 스타일
- `.nojekyll`: 정적 파일 그대로 제공

## 공개 전 확인

- 지원 이메일은 운영자가 제공한 `ezekieldevstudio@gmail.com`이며, 시행일은 2026-09-21입니다. 삭제 요청 접수 시 예상 처리 일정을 회신하고, 본인 확인 후 지체 없이 처리합니다. 고정 일수는 임의로 약속하지 않습니다.
- Supabase Dashboard에서 실제 `profiles` 필드, 트리거, 사용자 연결 테이블과 백업·로그 보관 정책을 확인합니다. 앱 코드에서는 profiles 직접 조회/저장 및 course_progress 서버 동기화를 사용하지 않습니다. 실제 서버 설정에 따른 추가 처리 항목과 해외 이전 안내가 필요한 경우 정책에 반영합니다.
- 이메일 수신 및 본인 확인 후 삭제 처리를 수행할 운영자가 필요합니다. 단순히 이 사이트를 게시해도 자동 삭제 기능이 생기지 않습니다.

## GitHub Pages

Repository Settings → Pages → Build and deployment:

- Source: **Deploy from a branch**
- Branch: **main**
- Folder: **/ (root)**
- Save

예상 URL (실제 배포 성공 여부는 별도 확인):

- https://ezekieldevstudio.github.io/english-thru-config/
- https://ezekieldevstudio.github.io/english-thru-config/privacy.html
- https://ezekieldevstudio.github.io/english-thru-config/delete-account.html

## 계정 삭제 운영 절차

1. 등록된 로그인 이메일을 통해 요청자 본인 및 삭제 의사를 확인합니다. 제3자의 요청만으로 계정을 삭제하지 않습니다.
2. 해당 사용자 ID에 연결된 실제 서버 사용자 데이터를 확인합니다. `profiles` 자동 삭제(cascade)를 가정하지 않습니다. 존재하는 관련 데이터를 삭제하고 Supabase Dashboard의 Authentication → Users에서 해당 Auth 사용자를 삭제합니다.
3. 삭제 결과를 확인한 뒤 요청자에게 안내합니다. 서버 삭제는 기기의 AsyncStorage를 지우지 않으므로 페이지의 기기 데이터 삭제 방법도 안내합니다.
4. 처리 목적이 끝난 문의·삭제 요청 이메일을 삭제합니다. 실제 보존 의무가 있다면 항목, 근거 및 기간을 사용자에게 설명합니다.

기존 발급 액세스 토큰은 만료까지 유효할 수 있으므로 즉각적인 모든 기기 로그아웃을 약속하지 않습니다. 관리자 자격 증명이나 사용자 정보는 이 공개 저장소에 보관하지 않습니다.

## 참고

- [Google Play 계정 삭제 요구사항](https://support.google.com/googleplay/android-developer/answer/13327111?hl=ko)
- [Supabase 사용자 관리](https://supabase.com/docs/guides/auth/managing-user-data)
- [GitHub Pages 게시 소스 설정](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
