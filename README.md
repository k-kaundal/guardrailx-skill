# GuardrailX Copilot Skill

GuardrailX is a reusable **GitHub Copilot skill** that helps detect:

* 🔐 Hardcoded secrets
* 🔑 Credentials & tokens
* 🧾 API keys
* 👤 Personal identifiable information (PII)
* ⚙️ Sensitive configuration values

The skill works through **Copilot’s reasoning**, so it requires **no SDK, CLI, or runtime installation**.

---

## 📦 Repository

https://github.com/k-kaundal/guardrailx-skill

---

## 🚀 Install in your project

### Option 1 — Manual install (recommended)

Copy the skill into your repository:

```
.github/skills/guardrailx/
```

Example:

```
your-project/
 └─ .github/
    └─ skills/
       └─ guardrailx/
          └─ SKILL.md
```

Commit and push — Copilot will automatically detect it.

---

### Option 2 — Install using skills CLI

If using the skills.sh ecosystem:

```
npx skills add k-kaundal/guardrailx-skill
```

---

## 💬 Usage in GitHub Copilot Chat

Ask Copilot:

```
Use the guardrailx-scan skill on this file
```

or:

```
Check this repository for secrets using guardrailx-scan
```

Copilot will:

1. Analyze the selected code or repository
2. Highlight risky lines
3. Explain why they are unsafe
4. Suggest secure alternatives and fixes

---

## 🎯 What this skill focuses on

* Preventing accidental secret leaks
* Improving secure coding practices
* Helping review AI-generated code safely
* Providing developer-friendly remediation advice

---

## 🧩 Requirements

* GitHub Copilot enabled in your IDE
* Repository access to `.github/skills/`

No SDK or external dependencies required.

---

## 📄 License

MIT (or choose your preferred license)

---

## ⭐ Contributing

Issues and pull requests are welcome to improve detection guidance, security rules, or documentation.
