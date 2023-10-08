# Maqueta Landing Page

Vite + Tailwind

## Para deploy en gh pages

- npm i gh-pages -D

- En vite.config.js:
    import { defineConfig } from "vite";
    import react from "@vitejs/plugin-react";

    // https://vitejs.dev/config/
    export default defineConfig({
      plugins: [react()],
      base: "/el-nombre-de-tu-repositorio/",
    });

- En package.json:
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview",
    "deploy": "gh-pages -d dist"
  }

- Luego y cada vez que se actualice el proyecto:
    npm run build
    npm run deploy

- Acordarse de cambiar el nombre del rute y agregar el nombre del repo que sino no detecta las rutas.
