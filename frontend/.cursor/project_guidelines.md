# 📘 Project Development Guidelines

This document outlines the coding and architectural practices for maintaining a scalable, clean, and efficient React + TypeScript codebase.

---

## 🧱 Architecture
- Modular structure under `src/` with domains like `features/`, `components/`, `services/`, etc.
- Feature-based slicing: each domain should own its own UI, logic, types, and state.

## 💡 Design System
- Use **TailwindCSS** for all styling.
- Use **shadcn/ui** for prebuilt components.
- Avoid all other CSS strategies.

## 🧪 Testing
- Use **Vitest** or **Jest** with **Testing Library**.
- Use **MSW** for mocking APIs.
- Every component and service must include tests.

## ⚙️ State Management
- Use **React Context** or **Zustand** for local/global state.
- Avoid Redux unless needed for cross-feature communication.

## 📦 API & Backend
- Use **Supabase** with full TypeScript support.
- Store logic in `services/`.
- Document and comment every API interaction.

## ✨ Standards
- Enforce **SOLID**, **DRY**, **KISS**, **YAGNI**.
- Avoid unnecessary abstractions.
- Comment all complex logic.
- Apply `eslint` + `prettier` consistently.
- Use `husky` + `lint-staged` for pre-commit checks.

## 🧰 Tooling
- **GitHub Actions** for CI
- **Vercel/Supabase Edge Functions** for deployment
- Analyze and optimize bundle sizes proactively

## 🔒 Security
- Never expose keys or secrets in frontend.
- Validate all user inputs.
- Use HTTPS endpoints only.

## 📄 Documentation
- Use `.cursor/` folder to include:
  - `rules.json` – Enforced coding standards
  - `prompts.json` – Predefined AI tasks
  - `README.md` – Setup and architecture notes

---

By adhering to these standards, this project ensures quality, maintainability, and performance at scale. All contributions must follow these principles.

