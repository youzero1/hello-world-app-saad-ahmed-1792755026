---
status: pending
title: Hello World App
---

# Hello World App

Build a minimal single-page app that displays a centered "Hello, World!" message on the home page. The project currently contains no source code, so the plan includes the full project scaffold.

1. Create `package.json` with the project name, ESM module type, npm scripts (`dev`, `build`, `preview`), and dependencies: React, React DOM, TanStack Router, Vite, the Vite React plugin, the TanStack Router Vite plugin, TypeScript, Tailwind CSS v4, and the Tailwind Vite plugin.
   - Expected outcome: `npm install` completes and the dev/build scripts are available.

2. Create `vite.config.ts` registering the TanStack Router plugin, the React plugin, and the Tailwind CSS v4 plugin, plus the `@/` path alias pointing at `src/`.
   - Expected outcome: Vite starts with routing, React, and Tailwind all wired up.

3. Create `tsconfig.json` with strict TypeScript settings, bundler-style module resolution, JSX support, and the `@/*` path alias matching the Vite config.
   - Expected outcome: TypeScript compiles the project with no errors and the alias resolves in editor and build.

4. Create `index.html` at the project root with a `<div id="root">` mount point, a page title of "Hello World", and a script entry loading `/src/main.tsx`.
   - Expected outcome: the dev server serves a page shell ready to mount the app.

5. Create `src/styles/global.css` whose first line is exactly `@import "tailwindcss";` and which otherwise holds only minimal base styling (e.g. default font smoothing).
   - Expected outcome: Tailwind utilities work throughout the app.

6. Create `src/main.tsx` that imports `src/styles/global.css` once, creates the TanStack Router instance from the generated route tree, and renders the router provider into `#root`.
   - Expected outcome: the app boots and hands rendering to the router.

7. Create `src/routes/__root.tsx` as the app shell: a full-height layout rendering the active route's outlet.
   - Expected outcome: every route renders inside a consistent shell. (Note: `src/routeTree.gen.ts` is generated automatically by the router plugin and must never be hand-written.)

8. Create `src/routes/index.tsx` as the home route: a full-screen, centered layout showing a large "Hello, World!" heading with a short supporting line, styled with Tailwind utilities (dark or light neutral background, clear typography, responsive sizing).
   - Expected outcome: visiting `/` shows a polished, centered "Hello, World!" screen.

9. Create `src/vite-env.d.ts` with the Vite client type reference so asset and env typings resolve.
   - Expected outcome: TypeScript understands Vite-specific types.

10. Verify the whole app: install dependencies, start the dev server, confirm the home page renders the "Hello, World!" screen, and run a production build to confirm it compiles cleanly.
    - Expected outcome: `npm run build` succeeds and the app works identically in dev and production.
