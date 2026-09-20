# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

A learning project for three.js. Vanilla JavaScript (ES modules, no TypeScript, no UI framework) bundled with Vite. There is no test runner or linter configured.

## Commands

- `npm run dev` — Vite dev server (http://localhost:5173)
- `npm run build` — production build into `dist/`
- `npm run preview` — serve the production build locally

## Architecture

`index.html` loads `src/main.js` as a module; all scene code lives there: scene, camera, renderer, `OrbitControls`, lights, and a `renderer.setAnimationLoop` render loop. The canvas is appended to `document.body` and sized to the window (resize handler updates camera aspect and renderer size).

Addons are imported from `three/examples/jsm/...` (e.g. `OrbitControls`), not from a separate package.
