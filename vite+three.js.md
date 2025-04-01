### 🚀 Vite + Three.js 프로젝트 실습 요약

#### ✅ 1. Node.js 설치 확인
```bash
node -v
npm -v
```
- 설치 안 되어 있으면 [https://nodejs.org](https://nodejs.org) 에서 **LTS 버전 설치**

---

#### ✅ 2. 새 프로젝트 폴더 만들고 진입
```bash
mkdir my-three-app
cd my-three-app
```

---

#### ✅ 3. Node.js 프로젝트 초기화
```bash
npm init -y
```

---

#### ✅ 4. Vite 설치
```bash
npm install vite
```

---

#### ✅ 5. 기본 웹사이트 구성
**`index.html`** 생성:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>My Three.js Project</title>
</head>
<body>
  <canvas class="webgl"></canvas>
  <script type="module" src="./script.js"></script>
</body>
</html>
```

---

#### ✅ 6. Vite 실행 스크립트 추가 (`package.json`)
```json
"scripts": {
  "dev": "vite",
  "build": "vite build"
}
```

---

#### ✅ 7. 개발 서버 실행
```bash
npm run dev
```
- 브라우저에 `http://localhost:5173` 접속

---

#### ✅ 8. Three.js 설치
```bash
npm install three
```

---

#### ✅ 9. 기본 Three.js 코드 작성 (`script.js`)
```js
import * as THREE from 'three'

// Scene
const scene = new THREE.Scene()

// Cube
const geometry = new THREE.BoxGeometry(1, 1, 1)
const material = new THREE.MeshBasicMaterial({ color: 0xff0000 })
const mesh = new THREE.Mesh(geometry, material)
scene.add(mesh)

// Camera
const sizes = { width: 800, height: 600 }
const camera = new THREE.PerspectiveCamera(75, sizes.width / sizes.height)
camera.position.z = 3
scene.add(camera)

// Renderer
const canvas = document.querySelector('.webgl')
const renderer = new THREE.WebGLRenderer({ canvas })
renderer.setSize(sizes.width, sizes.height)
renderer.render(scene, camera)
```

---

### 🟢 최종 결과
브라우저에서 **빨간색 정육면체가 보이는 Three.js 첫 장면**이 표시됩니다.

---

필요하면 다음 단계인 `애니메이션`, `카메라 조작`, `GLTF 모델 불러오기` 등도 요약해드릴게요.  
원하시면 **starter 파일 활용법**이나 `vite.config.js` 구조도 알려드릴 수 있어요!
