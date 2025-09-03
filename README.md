# 🚀 Client Template – Vite + Vue 3 + DaisyUI

Template ini membantu memulai pengembangan **Frontend** modern dengan:

* ⚡ [Vite](https://vite.dev/) – build & dev server super cepat
* 🖖 [Vue 3](https://vuejs.org/) – framework progresif untuk UI
* 🧭 [Vue Router](https://router.vuejs.org/) – routing bawaan Vue
* 📦 [Pinia](https://pinia.vuejs.org/) – state management resmi Vue
* 🎨 [Tailwind CSS](https://tailwindcss.com/) – utility-first CSS framework
* 🌼 [DaisyUI](https://daisyui.com/) – komponen siap pakai + **theming support**
* ✅ [Vitest](https://vitest.dev/) & [Playwright](https://playwright.dev/) – testing unit & end-to-end
* 🧹 [ESLint](https://eslint.org/) + [Oxlint](https://oxlint.com/) + [Prettier](https://prettier.io/) – linting & formatting

![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite\&logoColor=white)
![Vue](https://img.shields.io/badge/Vue.js-42B883?logo=vue.js\&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-38B2AC?logo=tailwind-css\&logoColor=white)
![DaisyUI](https://img.shields.io/badge/DaisyUI-5A0EF8?logo=tailwind-css\&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?logo=vitest\&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?logo=playwright\&logoColor=white)

---

## 📦 Instalasi

Clone repo lalu install dependencies:

```sh
git clone https://github.com/username/client-template-vite-vue.git
cd client-template-vite-vue
npm install
```

**Node.js version** yang didukung:

* `^20.19.0` atau `>=22.12.0`

---

## 🛠️ Development

Jalankan local dev server dengan HMR:

```sh
npm run dev
```

Buka di [http://localhost:5173](http://localhost:5173).

---

## 🏗️ Build

Untuk compile dan minify production build:

```sh
npm run build
```

Preview hasil build:

```sh
npm run preview
```

---

## ✅ Testing

### Unit Tests (Vitest)

```sh
npm run test:unit
```

### End-to-End Tests (Playwright)

```sh
# Install browser (sekali saja)
npx playwright install

# Build dulu sebelum testing di CI
npm run build

# Jalankan semua e2e test
npm run test:e2e

# Test hanya di Chromium
npm run test:e2e -- --project=chromium

# Test file tertentu
npm run test:e2e -- tests/example.spec.js

# Debug mode
npm run test:e2e -- --debug
```

---

## 🧹 Lint & Format

Lint kode dengan ESLint & Oxlint:

```sh
npm run lint
```

Format otomatis dengan Prettier:

```sh
npm run format
```

---

## 📂 Struktur Proyek

```
client-template-vite-vue/
├── public/              # File statis
├── src/
│   ├── assets/          # Asset (gambar, ikon, dll.)
│   ├── components/      # Komponen Vue
│   ├── stores/          # Store Pinia
│   ├── views/           # Halaman utama
│   ├── router/          # Vue Router setup
│   ├── App.vue          # Root component
│   └── main.js          # Entry point (JavaScript, bukan TS)
├── tests/               # Unit & e2e tests
├── vite.config.js       # Konfigurasi Vite + Tailwind + DaisyUI
└── package.json
```

---

## 🌟 Fitur

* ⚡ Build super cepat dengan Vite
* 🌼 Integrasi penuh DaisyUI dengan **theming support** → ubah tema dengan mudah (misalnya light/dark/retro/bumblebee)
* 📦 Modular dengan Vue 3 Composition API
* 🧭 Routing bawaan Vue Router
* 🔒 State management dengan Pinia
* ✅ Testing siap pakai (unit & e2e)
* 🧹 Linting + formatting otomatis

---

## 🎨 Theming DaisyUI

Template ini sudah terintegrasi dengan **DaisyUI themes**.
Kamu bisa mengubah tema langsung dari `vite.config.js` atau runtime via `data-theme` attribute.

Referensi tema lengkap: [https://daisyui.com/themes/](https://daisyui.com/themes/)

---

## 📜 Lisensi

[MIT](./LICENSE) © 2025 Kura Ninja