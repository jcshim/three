### ✅ Vite란?

**Vite**는 빠르고 간편한 **프론트엔드 개발 도구**입니다.  
주로 **Vue, React, Svelte** 등 모던 프레임워크에서 사용되며, **개발 서버는 빠르게 실행**, **프로덕션 빌드는 최적화**된 번들로 만들어줍니다.

---

### 💡 Vite의 주요 특징
- **빠른 개발 서버**: 모듈을 on-demand로 로딩해서 초기 실행이 빠름
- **빠른 번들링**: `esbuild`를 이용해 고속 번들링
- **HMR 지원**: 코드 수정 시 빠르게 반영 (Hot Module Replacement)
- **간편한 설정**: 직관적인 설정 방식(`vite.config.js`)
- **프레임워크 무관**: Vue, React, Preact 등 다양한 생태계 지원

---

### 🚀 CLI 명령어 요약

#### 📦 1. `vite` 또는 `vite dev`
개발 서버 실행  
```bash
vite [root]
```
- `--port <port>`: 포트 지정
- `--open`: 실행 시 브라우저 자동 열기
- `--host`: 네트워크 접근 허용

---

#### 🔧 2. `vite build`
프로덕션 빌드 생성  
```bash
vite build [root]
```
- `--outDir <dir>`: 결과물 디렉토리 지정 (기본값: `dist`)
- `--minify`: 압축 도구 설정 (기본: esbuild)
- `--sourcemap`: 소스맵 출력
- `--ssr`: 서버 사이드 렌더링 빌드

---

#### 🔍 3. `vite preview`
로컬에서 빌드 결과 미리보기  
```bash
vite preview [root]
```
- 실제 배포와 유사하게 확인 가능 (단, **프로덕션 서버로는 부적합**)
- `--port`, `--open` 등 옵션 동일

---

#### 🧹 4. `vite optimize` *(사용 안 해도 됨)*
의존성 사전 번들링 (자동으로 처리되므로 직접 호출 불필요)

---

### 🔑 요약 정리

| 명령어         | 기능 요약                      |
|----------------|-------------------------------|
| `vite`         | 개발 서버 실행                 |
| `vite build`   | 프로덕션용 번들링             |
| `vite preview` | 빌드 결과 미리보기             |
| `vite optimize`| 의존성 사전 번들링 *(자동)*     |

---

필요하시면 `vite.config.js` 구조나 React/Vue 연동 예시도 설명드릴 수 있어요!
