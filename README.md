# 🧩 Skill Generator v3.2 Expert — Complete AI Skill Building Toolkit

<a href="https://unikorn.vn/p/skillgenerator?ref=embed" target="_blank"><img src="https://unikorn.vn/api/widgets/badge/skillgenerator/rank?theme=light&type=weekly" alt="Skill Generator - Weekly" style="width: 250px; height: 64px;" width="250" height="64" /></a>

> **Turn your ideas + workflows into fully automated AI Skills**
> Built for Google Antigravity. Score: 🏆 100/100 S-tier.

---

## 📋 Table of Contents

- [Introduction](#introduction)
- [Installation](#-installation)
- [Usage](#-usage)
- [Scripts & Tools](#-scripts--tools-7-utilities)
- [Slash Commands](#-slash-commands)
- [Project Structure](#-project-structure)
- [Platform Compatibility](#-platform-compatibility)
- [Documentation](#-documentation)
- [Changelog](#-changelog-en)
- [License](#-license-en)

---

## Introduction

**Skill Generator** is a specialized AI Skill for **Google Antigravity** (and 7 other platforms).
It helps you **create new AI Skills** — even if you **DON'T know** what a skill is, what YAML is, or how to write SKILL.md.

**You only need:**

- ✅ An idea about what you want to automate
- ✅ A workflow / process / logic in your head

**AI handles the rest:**

- 🎤 Smart interview to understand your workflow
- 🔍 Auto-detect the right patterns
- 🏗️ Generate a **complete skill package** (not just 1 file!)
- 🧪 Live test before deployment

### Key Features (v3.2)

| Feature | Description |
| --- | --- |
| 🧠 **5-Phase Pipeline** | Interview → Extract → Detect → Generate → Test |
| ⚡ **Fast Track** | Skip phases when user provides detailed workflow upfront |
| 📦 **Full Package Output** | Generates complete skill directory: SKILL.md + README + resources + examples + scripts + workflows |
| 🔧 **7 Python Scripts** | Audit, Export, Stats, Compare, Scaffold, Validate, Simulate |
| ⚡ **7 Slash Commands** | `/skill-audit`, `/skill-export`, `/skill-stats`, and more |
| 🌐 **8 Platforms** | Antigravity, Claude Code, Cursor, Windsurf, Cline, Copilot, OpenClaw, Aider |
| 🏆 **100/100 S-tier** | Self-audited against 7 Perfect Skill Principles |

### Who is this for?

| Audience | Example |
| --- | --- |
| **Non-coders** | Sales rep who wants AI to auto-draft price quotes |
| **Developers** | Want AI to format commit messages, review code |
| **Team Leads** | Standardize team workflows with AI |
| **Freelancers** | Automate repetitive daily tasks |

---

## 🔧 Installation

### Prerequisites

- A supported AI Agent platform (see compatibility table below)
- Python 3.8+ (optional, for scripts)
- Git (recommended)

### 🌟 Antigravity (Recommended)

**Global Installation** — Available in ALL projects:

```bash
# macOS / Linux
git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git \
  ~/.gemini/antigravity/skills/skill-generator
```

```powershell
# Windows (PowerShell)
git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git `
  "$env:USERPROFILE\.gemini\antigravity\skills\skill-generator"
```

**Workspace Installation** — Only in current project:

```bash
cd your-project/
git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git \
  .agent/skills/skill-generator
```

**After install:** Open a new chat and type `/skill-generate` to verify.

### 🤖 OpenClaw AI Gateway

OpenClaw uses a different approach — you paste the skill content into the Agent System Prompt.

**Step 1:** Clone the repository

```bash
git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git
cd skill-generator
```

**Step 2:** Open the OpenClaw Admin Panel → **Agents** → Select your agent

**Step 3:** Copy the contents of `SKILL.md` into the **System Prompt** field

**Step 4:** Add the `phases/` folder contents as additional context:

- Upload `phases/phase1_interview.md` through `phases/phase5_test.md`
- Or concatenate them into the System Prompt below the main SKILL.md

**Step 5:** Save and test with: *"Tạo cho tao 1 skill tự soạn email báo giá"*

> ⚠️ **Note:** OpenClaw has token limits. If System Prompt is too long, use only `SKILL.md` (slim version, ~270 lines) — the AI will still work, just without deep phase references.

### Other Platforms

| Platform | Command |
| --- | --- |
| **Claude Code** | `git clone ...skill-generator.git .claude/commands/skill-generator` |
| **Cursor** | `git clone ...skill-generator.git .cursor/rules/skill-generator` |
| **Windsurf** | `git clone ...skill-generator.git .windsurf/rules/skill-generator` |
| **Cline** | `git clone ...skill-generator.git .clinerules/skill-generator` |
| **Copilot** | `git clone ...skill-generator.git .github/skill-generator` |

### Update to latest version

```bash
cd path/to/skill-generator
git pull
```

---

## 🚀 Usage

Just tell the AI what you want to automate:

```
You: Create a skill that auto-drafts price quote emails
AI: (Reads SKILL.md → Starts interviewing you → Generates complete skill package)
```

### Scripts & Tools (7 Utilities)

```bash
# Validate SKILL.md structure
python scripts/validate_skill.py ./path/to/my-skill/

# Simulate a dry-run of the skill
python scripts/simulate_skill.py ./path/to/my-skill/

# 🆕 Audit against 7 Perfect Principles → S/A/B/C/D/F grade
python scripts/skill_audit.py ./path/to/my-skill/
python scripts/skill_audit.py ./path/to/my-skill/ --json
python scripts/skill_audit.py ./path/to/my-skill/ --strict

# 🆕 View stats + Cognitive Load Score
python scripts/skill_stats.py ./path/to/my-skill/

# 🆕 Export to Cursor/Claude/Windsurf/Cline/Copilot/OpenClaw
python scripts/skill_export.py ./path/to/my-skill/ --platform cursor
python scripts/skill_export.py ./path/to/my-skill/ --platform all

# 🆕 Compare 2 versions of a skill
python scripts/skill_compare.py ./old-skill/ ./new-skill/

# 🆕 Scaffold a new skill from scratch
python scripts/skill_scaffold.py my-new-skill --full
python scripts/skill_scaffold.py my-new-skill --interactive
```

### ⚡ Slash Commands (8 commands)

Type `/` in your AI chat to access these commands:

| Command | Description |
| --- | --- |
| `/skill-generate` | 🧠 **Create new skill from idea** (5-Phase interview pipeline) |
| `/skill-audit` | 🔍 Audit skill against 7 principles |
| `/skill-export` | 📦 Export to other platforms |
| `/skill-stats` | 📊 View stats + Cognitive Load |
| `/skill-compare` | 🔄 Compare 2 skill versions |
| `/skill-scaffold` | 🧩 Create new skill skeleton |
| `/skill-validate` | ✅ Check SKILL.md validity |
| `/skill-simulate` | 🧪 Simulate dry-run |

---

## 📁 Project Structure

```text
skill-generator/                             (35+ files)
├── SKILL.md                                ← 🧠 Slim orchestrator (~270 lines)
├── README.md                               ← 📖 This file
├── .gitignore                              ← 🔒 Git config
├── .pylintrc                               ← 🔧 Python lint config
│
├── phases/                                 ← 🎬 Detailed phase instructions (5 files)
│   ├── phase1_interview.md                 ← 🎤 Phase 1: Smart interview
│   ├── phase2_extract.md                   ← 🔬 Phase 2: Knowledge extraction
│   ├── phase3_detect.md                    ← 🔎 Phase 3: Pattern detection
│   ├── phase4_generate.md                  ← 🏗️ Phase 4: Skill generation
│   └── phase5_test.md                      ← 🧪 Phase 5: Test & refine
│
├── resources/                              ← 📚 Reference docs (13 files)
│   ├── scripts_guide.md                    ← Guide for all 7 scripts
│   ├── skill_template.md                   ← Standard SKILL.md template
│   ├── checklist.md                        ← 2-tier quality checklist
│   ├── advanced_patterns.md                ← 6 architecture patterns
│   ├── interview_questions.md              ← 30+ questions + Expert Probing
│   ├── pattern_detection.md                ← Decision tree + Complexity scoring
│   ├── blueprints.md                       ← 10 ready-made skill templates
│   ├── anti_patterns.md                    ← 15 common mistakes + fixes
│   ├── prompt_engineering.md               ← 15 instruction-writing techniques
│   ├── versioning_guide.md                 ← Skill upgrade guide
│   ├── industry_questions.md               ← 8 industry-specific question sets
│   ├── composition_cookbook.md              ← 5 multi-skill composition patterns
│   └── script_integration.md              ← Script integration (7 security layers)
│
├── examples/                               ← 🎯 Example skills (3 files)
│   ├── example_git_commit.md               ← Example 1: Git commit formatter
│   ├── example_api_docs.md                 ← Example 2: API docs generator
│   └── example_db_migration.md             ← Example 3: DB migration helper
│
├── scripts/                                ← 🔧 Python tools (7 files)
│   ├── validate_skill.py                   ← Validate SKILL.md structure
│   ├── simulate_skill.py                   ← Simulate dry-run
│   ├── skill_audit.py                      ← Audit 7 principles, grade S-tier
│   ├── skill_export.py                     ← Export to 6 platforms
│   ├── skill_stats.py                      ← Stats + Cognitive Load
│   ├── skill_compare.py                    ← Compare 2 versions
│   └── skill_scaffold.py                   ← Scaffold new skill
│
├── .agents/workflows/                      ← ⚡ Slash commands (8 files)
│   ├── skill-generate.md                   ← 🆕 /skill-generate (create from idea)
│   ├── skill-audit.md                      ← /skill-audit
│   ├── skill-export.md                     ← /skill-export
│   ├── skill-stats.md                      ← /skill-stats
│   ├── skill-compare.md                    ← /skill-compare
│   ├── skill-scaffold.md                   ← /skill-scaffold
│   ├── skill-validate.md                   ← /skill-validate
│   └── skill-simulate.md                   ← /skill-simulate
│
└── .github/workflows/                      ← 🔄 CI/CD (1 file)
    └── ci.yml                              ← 6 automated checks on push
```

---

## 🌐 Platform Compatibility

| Platform | Skills/Custom Instructions | Compatibility | Notes |
| --- | --- | --- | --- |
| **Google Antigravity** | ✅ Skills (SKILL.md) | 🟢 100% Native | Designed for this platform |
| **Claude Code** | ✅ Custom Commands (CLAUDE.md) | 🟢 95% | Rename SKILL.md → CLAUDE.md |
| **Cursor** | ✅ Rules (.cursor/rules/) | 🟡 85% | Use as Rule, no auto-trigger |
| **Windsurf / Codeium** | ✅ Rules (.windsurfrules) | 🟡 85% | Similar to Cursor |
| **Cline** | ✅ Custom Instructions (.clinerules) | 🟡 80% | Paste into System Prompt |
| **OpenClaw** | ✅ System Prompt (Agent Config) | 🟡 80% | Via Telegram bot, config in agent |
| **GitHub Copilot** | ✅ Instructions (.github/) | 🟡 75% | Instructions only, no scripts |
| **Aider** | ⚠️ Conventions (.aider.conf.yml) | 🟠 60% | Limited, conventions only |

---

## 📚 Documentation

### For Beginners

| File | Description | When to read |
| --- | --- | --- |
| `SKILL.md` | Core brain — AI reads this | No need (AI handles it) |
| `resources/scripts_guide.md` | 🆕 Guide for all 7 scripts | Want to use analysis tools |
| `resources/skill_template.md` | Standard SKILL.md template | Want to understand skill structure |
| `resources/blueprints.md` | 10 ready-made templates | Need quick ideas |

### For Intermediate Users

| File | Description | When to read |
| --- | --- | --- |
| `resources/prompt_engineering.md` | 15 instruction techniques | Want more precise skills |
| `resources/anti_patterns.md` | 15 common mistakes | Debug broken skills |
| `resources/advanced_patterns.md` | 6 architecture patterns | Complex skills |

### For Experts

| File | Description | When to read |
| --- | --- | --- |
| `resources/composition_cookbook.md` | 5 multi-skill patterns | Build skill systems |
| `resources/industry_questions.md` | 8 industry question sets | Domain-specific skills |
| `resources/script_integration.md` | Script integration + 7 security layers | Skills that run system commands |

---

## 📜 Changelog (EN)

### v3.2 Expert Edition (2026-03-04)

- Added **7 Perfect Skill Principles** + System Architecture philosophy
- Added **Full Package Output** — generates complete skill directory (not just 1 file)
- Added **5 expert scripts**: skill_audit, skill_export, skill_stats, skill_compare, skill_scaffold
- Added **7 slash commands** for quick script access
- Added **scripts_guide.md** — detailed usage guide for all scripts
- Added **OpenClaw AI Gateway** support
- Added **⚡ Fast Track** — shortcut for simple skills
- Achieved **100/100 S-tier** on self-audit

### v3.0 Ultimate (2026-03-03)

- Added blueprints, anti_patterns, prompt_engineering resources
- Added simulate_skill.py

### v2.0 Pro (2026-03-03)

- Rewrote SKILL.md — Interview-driven (5 Phases)

### v1.0 (2026-03-03)

- Initial release

---

## ❓ FAQ

**Q: Do I need to know how to code?**
A: No. Skill Generator is designed for non-coders. Just describe your workflow in plain language.

**Q: Global or Workspace install?**
A: **Global** (`~/.gemini/antigravity/skills/`) for all projects. **Workspace** (`.agent/skills/`) for one project only.

**Q: What does the generated skill include?**
A: A complete package: SKILL.md + README.md + resources/ + examples/ + scripts/ + workflows/ + .gitignore

**Q: Can I edit the skill after generation?**
A: Yes. Open the SKILL.md file and edit directly, or ask the AI to modify it.

**Q: What languages are supported?**
A: Vietnamese and English. The AI interviews you in your language.

---

## 🤝 Contributing

1. Fork the repository
2. Create your branch: `git checkout -b feature/my-feature`
3. Commit: `git commit -m "feat: add my feature"`
4. Push: `git push origin feature/my-feature`
5. Create a Pull Request

---

## 📄 License (EN)

MIT — Free to use, modify, and share.

---

> 🇻🇳 **Developed by Thân Công Hải** — Skill Generator v3.2 Expert Edition
> *"Turn ideas into AI Skills, turn ordinary people into AI architects."*

---
---

# 🇻🇳 PHIÊN BẢN TIẾNG VIỆT (Vietnamese Version)

---

# 🧩 Skill Generator v3.2 Expert — Bộ Công Cụ Tạo AI Skill Hoàn Chỉnh

<a href="https://unikorn.vn/p/skillgenerator?ref=embed" target="_blank"><img src="https://unikorn.vn/api/widgets/badge/skillgenerator/rank?theme=light&type=weekly" alt="Skill Generator - Hàng tuần" style="width: 250px; height: 64px;" width="250" height="64" /></a>
> **Biến ý tưởng + quy trình công việc trong đầu bạn → AI Skill tự động hóa**
> Dành cho Google Antigravity. Đánh giá: 🏆 100/100 S-tier.

---

## 📋 Mục lục

- [Giới thiệu](#giới-thiệu)
- [Cài đặt](#-cài-đặt)
- [Cách sử dụng](#-cách-sử-dụng)
- [Cấu trúc dự án](#-cấu-trúc-dự-án)
- [Tài liệu tham khảo](#-tài-liệu-tham-khảo)
- [Changelog](#-changelog)
- [License](#-license)

---

## Giới thiệu

**Skill Generator** là một AI Skill chuyên biệt cho nền tảng **Google Antigravity**.
Nó giúp bạn **tạo AI Skill mới** — ngay cả khi bạn **KHÔNG biết** skill là gì,
YAML là gì, hay cấu trúc SKILL.md viết thế nào.

**Bạn chỉ cần có:**

- ✅ Ý tưởng về công việc muốn tự động hóa
- ✅ Flow / quy trình / logic trong đầu

**AI sẽ lo phần còn lại:**

- 🎤 Phỏng vấn thông minh để hiểu quy trình
- 🔍 Phát hiện pattern phù hợp
- 🏗️ Sinh toàn bộ skill hoàn chỉnh
- 🧪 Test thử trước khi deploy

### Ai nên dùng?

| Đối tượng | Ví dụ |
| --- | --- |
| **Người không biết code** | Nhân viên kinh doanh muốn AI tự soạn báo giá |
| **Developer** | Muốn AI tự format commit message, review code |
| **Team Lead / Manager** | Muốn chuẩn hóa quy trình team bằng AI |
| **Freelancer** | Tự động hóa các task lặp lại hàng ngày |

---

## 🔧 Cài đặt

### Yêu cầu

- Một nền tảng AI Agent (xem bảng tương thích bên dưới)
- Python 3.8+ (cho scripts kiểm tra — tùy chọn)
- Git (khuyến khích, để cài và cập nhật dễ dàng)

### Bảng tương thích nền tảng

| Nền tảng | Skills/Custom Instructions | Tương thích | Ghi chú |
| --- | --- | --- | --- |
| **Google Antigravity** | ✅ Skills (SKILL.md) | 🟢 100% Native | Được thiết kế chuyên cho nền tảng này |
| **Claude Code** | ✅ Custom Commands (CLAUDE.md) | 🟢 95% | Cần đổi SKILL.md → CLAUDE.md |
| **Cursor** | ✅ Rules (.cursor/rules/) | 🟡 85% | Dùng làm Rule, không có auto-trigger |
| **Windsurf / Codeium** | ✅ Rules (.windsurfrules) | 🟡 85% | Tương tự Cursor |
| **Cline** | ✅ Custom Instructions (.clinerules) | 🟡 80% | Paste nội dung vào System Prompt |
| **GitHub Copilot** | ✅ Instructions (.github/copilot-instructions.md) | 🟡 75% | Chỉ hỗ trợ instructions, không có scripts |
| **OpenClaw** | ✅ System Prompt (Agent Config) | 🟡 80% | Dùng qua Telegram bot, cấu hình trong agent config |
| **Aider** | ⚠️ Conventions (.aider.conf.yml) | 🟠 60% | Hạn chế, chỉ dùng conventions |

---

### 🟢 Google Antigravity (Native — Khuyến khích)

**Bước 1: Clone repository**

```bash
git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git
```

**Bước 2: Copy vào thư mục skills** (chọn 1 trong 2)

| Phạm vi | Đường dẫn | Khi nào dùng |
| --- | --- | --- |
| **Global** | `~/.gemini/antigravity/skills/` | Dùng cho TẤT CẢ dự án |
| **Workspace** | `.agent/skills/` | Chỉ cho 1 dự án cụ thể |

**macOS / Linux:**

```bash
# Global
cp -r skill-generator ~/.gemini/antigravity/skills/skill-generator

# Hoặc Workspace
cp -r skill-generator .agent/skills/skill-generator
```

**Windows (PowerShell):**

```powershell
# Global
Copy-Item -Recurse skill-generator "$env:USERPROFILE\.gemini\antigravity\skills\skill-generator"

# Hoặc Workspace
Copy-Item -Recurse skill-generator ".agent\skills\skill-generator"
```

**Bước 3: Khởi động lại Antigravity** (hoặc mở chat mới)

```
Bạn: tạo skill
AI: (Bắt đầu phỏng vấn → Cài thành công ✅)
```

---

### 🟣 Claude Code (Anthropic)

Claude Code hỗ trợ Custom Commands qua file `CLAUDE.md` — tương tự SKILL.md.

**Bước 1: Clone và copy**

```bash
git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git
```

**Bước 2: Cài đặt** (chọn 1 trong 2)

```bash
# Global — áp dụng cho mọi dự án
cp -r skill-generator ~/.claude/commands/skill-generator

# Workspace — chỉ dự án hiện tại
mkdir -p .claude/commands
cp -r skill-generator .claude/commands/skill-generator
```

**Bước 3: Tạo file bridge** (để Claude Code nhận diện)

```bash
# Tạo file CLAUDE.md ở root dự án (nếu chưa có)
cat >> CLAUDE.md << 'EOF'

## Skill Generator
Khi user yêu cầu "tạo skill", "biến quy trình thành skill", hoặc "tự động hóa công việc":
- Đọc file `.claude/commands/skill-generator/SKILL.md` để biết quy trình
- Tham khảo các file trong `.claude/commands/skill-generator/resources/`
- Tuân theo 5 Phase: Interview → Extract → Detect → Generate → Test
EOF
```

**Bước 4: Sử dụng**

```
Bạn: /skill-generator (hoặc) tạo skill cho em
Claude: (Đọc SKILL.md → Bắt đầu phỏng vấn)
```

---

### 🔵 Cursor

Cursor hỗ trợ Rules — dùng skill-generator làm Custom Rule.

**Bước 1: Clone và copy**

```bash
git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git
```

**Bước 2: Cài vào Cursor Rules**

```bash
# Tạo thư mục rules (nếu chưa có)
mkdir -p .cursor/rules

# Copy skill-generator vào
cp -r skill-generator .cursor/rules/skill-generator
```

**Windows:**

```powershell
New-Item -ItemType Directory -Force -Path ".cursor\rules"
Copy-Item -Recurse skill-generator ".cursor\rules\skill-generator"
```

**Bước 3: Tạo rule file**

Tạo file `.cursor/rules/skill-generator.mdc`:

```markdown
---
description: Tạo AI Skill mới từ ý tưởng hoặc quy trình công việc
globs: 
alwaysApply: false
---

Khi user yêu cầu "tạo skill", "biến quy trình thành skill", "tự động hóa":
- Đọc file `.cursor/rules/skill-generator/SKILL.md`
- Tuân theo quy trình 5 Phase trong đó
- Tham khảo resources/ cho templates và best practices
```

**Bước 4: Sử dụng**

```
Bạn: @skill-generator tạo skill soạn báo giá
Cursor: (Đọc rule → Áp dụng SKILL.md → Bắt đầu phỏng vấn)
```

---

### 🟠 Windsurf / Codeium

Windsurf dùng Cascade Rules — tương tự Cursor.

**Bước 1: Clone và copy**

```bash
git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git
```

**Bước 2: Cài vào Windsurf Rules**

```bash
# Tạo thư mục rules
mkdir -p .windsurf/rules

# Copy skill-generator
cp -r skill-generator .windsurf/rules/skill-generator
```

**Bước 3: Tạo rule file**

Tạo file `.windsurf/rules/skill-generator.md`:

```markdown
---
trigger: manual
description: Tạo AI Skill mới từ ý tưởng hoặc quy trình công việc
---

Khi user yêu cầu "tạo skill", "biến quy trình thành skill", "tự động hóa":
- Đọc file `.windsurf/rules/skill-generator/SKILL.md`
- Tuân theo quy trình 5 Phase trong đó
- Tham khảo resources/ cho templates và best practices
```

**Bước 4: Sử dụng**

```
Bạn: Tạo skill từ quy trình deploy
Windsurf: (Áp dụng rule → Bắt đầu phỏng vấn)
```

---

### 🟤 Cline (VS Code Extension)

Cline dùng Custom Instructions — paste nội dung SKILL.md vào System Prompt.

**Bước 1: Clone**

```bash
git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git
```

**Bước 2: Cài vào dự án**

```bash
# Copy vào thư mục dự án
cp -r skill-generator .clinerules/skill-generator
```

**Bước 3: Cấu hình Cline**

1. Mở VS Code → Cline sidebar
2. Vào **Settings** → **Custom Instructions**
3. Thêm đoạn sau:

```
Khi user yêu cầu "tạo skill" hoặc "tự động hóa":
- Đọc file .clinerules/skill-generator/SKILL.md
- Tuân theo 5 Phase: Interview → Extract → Detect → Generate → Test
- Tham khảo .clinerules/skill-generator/resources/ cho best practices
```

**Bước 4: Sử dụng**

```
Bạn: Tạo skill tự động review code
Cline: (Đọc SKILL.md → Bắt đầu phỏng vấn)
```

---

### ⚫ GitHub Copilot

GitHub Copilot hỗ trợ Custom Instructions ở cấp dự án.

**Bước 1: Clone và copy**

```bash
git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git
cp -r skill-generator .github/skill-generator
```

**Bước 2: Thêm vào Copilot Instructions**

Tạo hoặc mở file `.github/copilot-instructions.md`, thêm:

```markdown
## Skill Generator

Khi user yêu cầu "tạo skill", "biến quy trình thành skill", "tự động hóa":
- Đọc file `.github/skill-generator/SKILL.md` để biết quy trình đầy đủ
- Tuân theo 5 Phase: Interview → Extract → Detect → Generate → Test
- Tham khảo `.github/skill-generator/resources/` cho templates
```

**Bước 3: Sử dụng** (trong Copilot Chat)

```
Bạn: Tạo skill soạn email báo giá
Copilot: (Đọc instructions → Bắt đầu phỏng vấn)
```

> ⚠️ **Lưu ý:** Copilot không hỗ trợ chạy scripts trực tiếp.
> Phần scripts (`validate_skill.py`, `simulate_skill.py`) cần chạy thủ công.

---

### 🐾 OpenClaw (AI Gateway)

OpenClaw là AI Gateway hỗ trợ multi-LLM, thường truy cập qua Telegram bot.
Dùng System Prompt của agent để nhúng skill-generator.

**Bước 1: Clone repository**

```bash
git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git
```

**Bước 2: Copy nội dung SKILL.md vào Agent Config**

1. Mở file cấu hình agent của OpenClaw (thường là `config.yaml` hoặc qua Admin Panel)
2. Tìm phần **System Prompt** hoặc **Agent Instructions** của agent muốn thêm skill
3. Copy toàn bộ nội dung file `SKILL.md` vào phần System Prompt

**Bước 3: Upload tài liệu tham khảo (tùy chọn)**

Nếu OpenClaw hỗ trợ file upload / knowledge base:

- Upload các file trong `resources/` vào knowledge base của agent
- Đặc biệt: `skill_template.md`, `checklist.md`, `anti_patterns.md`

**Bước 4: Sử dụng** (qua Telegram hoặc Web UI)

```
Bạn: Tạo skill tự động trả lời khách hàng
OpenClaw Bot: (Đọc System Prompt → Bắt đầu phỏng vấn)
```

> ⚠️ **Lưu ý:** OpenClaw chạy qua API nên không hỗ trợ tạo file trực tiếp.
> AI sẽ sinh nội dung SKILL.md dạng text → bạn cần tự copy vào file.

---

### 📥 Cài bằng 1 lệnh (Quick Install)

| Nền tảng | 1 lệnh (macOS/Linux) |
| --- | --- |
| **Antigravity (Global)** | `git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git ~/.gemini/antigravity/skills/skill-generator` |
| **Antigravity (Workspace)** | `git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git .agent/skills/skill-generator` |
| **Claude Code** | `git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git .claude/commands/skill-generator` |
| **Cursor** | `git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git .cursor/rules/skill-generator` |
| **Windsurf** | `git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git .windsurf/rules/skill-generator` |
| **Cline** | `git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git .clinerules/skill-generator` |
| **Copilot** | `git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git .github/skill-generator` |
| **OpenClaw** | `git clone https://github.com/marketingjuliancongdanh79-pixel/skill-generator.git` → Copy SKILL.md vào Agent System Prompt |

### Cập nhật phiên bản mới

```bash
# Vào thư mục đã cài, chạy:
cd <đường-dẫn-skill-generator>
git pull
```

---

## 🚀 Cách sử dụng

### Cách 1: Dùng slash command

```
/skill
```

### Cách 2: Nói tự nhiên

AI sẽ tự nhận diện và kích hoạt skill khi bạn nói:

| Câu nói | AI hiểu |
| --- | --- |
| "Tạo skill từ quy trình deploy của em" | → Kích hoạt skill-generator |
| "Em muốn AI tự động viết báo cáo tuần" | → Kích hoạt skill-generator |
| "Biến workflow review code thành skill" | → Kích hoạt skill-generator |
| "Make a new skill for checking PRs" | → Kích hoạt skill-generator |
| "Tự động hóa công việc soạn báo giá" | → Kích hoạt skill-generator |

### Quy trình tạo skill

```text
Bạn nói ý tưởng
    ↓
⚡ Fast Track?
    ├── Nếu bạn nói RÕ flow → AI xác nhận → Sinh skill ngay
    └── Nếu chưa rõ → AI phỏng vấn thông minh (5-10 câu)
         ↓
    🔍 AI phát hiện pattern + tính complexity
         ↓
    🏗️ AI sinh toàn bộ skill (SKILL.md + resources + scripts)
         ↓
    🧪 AI chạy thử (Dry Run) với tình huống thực
         ↓
    ✅ Skill hoàn chỉnh, sẵn sàng deploy!
```

### Ví dụ sử dụng thực tế

**Bạn:** "Em muốn AI tự soạn email báo giá cho khách hàng. Khi nhận email khách hỏi giá, AI sẽ đọc yêu cầu, tra bảng giá, tính chiết khấu theo số lượng (10-49: giảm 5%, 50-99: giảm 10%, ≥100: giảm 15%), cộng VAT 8%, rồi soạn email trả lời."

**AI:** Sẽ tự nhận diện đây là Fast Track (bạn đã cung cấp flow rõ ràng) → xác nhận lại → sinh skill `price-quoter` hoàn chỉnh.

### Scripts hỗ trợ (7 công cụ)

```bash
# Kiểm tra SKILL.md có hợp lệ không
python scripts/validate_skill.py ./path/to/my-skill/

# Mô phỏng chạy thử skill
python scripts/simulate_skill.py ./path/to/my-skill/

# 🆕 Audit 7 nguyên tắc → chấm điểm S/A/B/C/D/F
python scripts/skill_audit.py ./path/to/my-skill/
python scripts/skill_audit.py ./path/to/my-skill/ --json

# 🆕 Thống kê + Cognitive Load Score
python scripts/skill_stats.py ./path/to/my-skill/

# 🆕 Export sang Cursor/Claude/Windsurf/Cline/Copilot/OpenClaw
python scripts/skill_export.py ./path/to/my-skill/ --platform cursor
python scripts/skill_export.py ./path/to/my-skill/ --platform all

# 🆕 So sánh 2 phiên bản skill
python scripts/skill_compare.py ./old-skill/ ./new-skill/

# 🆕 Tạo skeleton skill mới
python scripts/skill_scaffold.py my-new-skill --full
python scripts/skill_scaffold.py my-new-skill --interactive
```

### ⚡ Slash Commands

Gõ `/` trong chat AI để truy cập nhanh:

| Lệnh | Chức năng |
| --- | --- |
| `/skill-audit` | 🔍 Audit skill theo 7 nguyên tắc |
| `/skill-export` | 📦 Export ra các nền tảng khác |
| `/skill-stats` | 📊 Xem thống kê + Cognitive Load |
| `/skill-compare` | 🔄 So sánh 2 phiên bản skill |
| `/skill-scaffold` | 🧩 Tạo skeleton skill mới |
| `/skill-validate` | ✅ Kiểm tra SKILL.md hợp lệ |
| `/skill-simulate` | 🧪 Mô phỏng chạy thử |

---

## 📁 Cấu trúc dự án

```text
skill-generator/                             (27+ files)
├── SKILL.md                                ← 🧠 Bộ não chính (1200+ dòng, 5 Phase)
├── README.md                               ← 📖 File này
├── .gitignore                              ← 🔒 Git config
│
├── resources/                              ← 📚 Tài liệu tham khảo (13 files)
│   ├── scripts_guide.md                    ← 🆕 Hướng dẫn sử dụng 7 scripts
│   ├── skill_template.md                   ← Template chuẩn SKILL.md
│   ├── checklist.md                        ← Checklist 2-tier (Basic + Expert)
│   ├── advanced_patterns.md                ← 6 pattern kiến trúc nâng cao
│   ├── interview_questions.md              ← 30+ câu hỏi + Expert Probing
│   ├── pattern_detection.md                ← Decision tree + Complexity scoring
│   ├── blueprints.md                       ← 10 skill templates "ăn liền"
│   ├── anti_patterns.md                    ← 15 lỗi phổ biến + cách fix
│   ├── prompt_engineering.md               ← 15 kỹ thuật viết Instructions
│   ├── versioning_guide.md                 ← Hướng dẫn nâng cấp skill
│   ├── industry_questions.md               ← 8 bộ câu hỏi chuyên ngành
│   ├── composition_cookbook.md              ← 5 patterns kết hợp skill
│   └── script_integration.md              ← Tích hợp Scripts (7 lớp bảo mật)
│
├── examples/                               ← 🎯 Ví dụ mẫu (3 files)
│   ├── example_git_commit.md               ← Ví dụ 1: Git commit formatter
│   ├── example_api_docs.md                 ← Ví dụ 2: API docs generator
│   └── example_db_migration.md             ← Ví dụ 3: DB migration helper
│
├── scripts/                                ← 🔧 Công cụ Python (7 files)
│   ├── validate_skill.py                   ← Kiểm tra SKILL.md hợp lệ
│   ├── simulate_skill.py                   ← Mô phỏng chạy thử skill
│   ├── skill_audit.py                      ← 🆕 Audit 7 nguyên tắc, chấm S-tier
│   ├── skill_export.py                     ← 🆕 Export ra 6 nền tảng
│   ├── skill_stats.py                      ← 🆕 Thống kê + Cognitive Load
│   ├── skill_compare.py                    ← 🆕 So sánh 2 phiên bản
│   └── skill_scaffold.py                   ← 🆕 Tạo skeleton skill mới
│
└── .agents/workflows/                      ← ⚡ Slash commands (7 files)
    ├── skill-audit.md                      ← /skill-audit
    ├── skill-export.md                     ← /skill-export
    ├── skill-stats.md                      ← /skill-stats
    ├── skill-compare.md                    ← /skill-compare
    ├── skill-scaffold.md                   ← /skill-scaffold
    ├── skill-validate.md                   ← /skill-validate
    └── skill-simulate.md                   ← /skill-simulate
```

---

## � Tài liệu tham khảo

### Cho người mới bắt đầu

| File | Mô tả | Khi nào đọc |
| --- | --- | --- |
| `SKILL.md` | Bộ não chính — AI đọc file này | Không cần đọc (AI tự xử lý) |
| `resources/scripts_guide.md` | 🆕 Hướng dẫn sử dụng 7 scripts | Muốn dùng công cụ kiểm tra |
| `resources/skill_template.md` | Template mẫu SKILL.md | Muốn hiểu cấu trúc skill |
| `resources/blueprints.md` | 10 skill ăn liền | Cần ý tưởng nhanh |
| `resources/checklist.md` | Checklist chất lượng | Kiểm tra skill trước deploy |

### Cho người muốn hiểu sâu

| File | Mô tả | Khi nào đọc |
| --- | --- | --- |
| `resources/prompt_engineering.md` | 15 kỹ thuật viết Instructions | Muốn skill chính xác hơn |
| `resources/anti_patterns.md` | 15 lỗi phổ biến | Debug skill bị lỗi |
| `resources/advanced_patterns.md` | 6 pattern kiến trúc | Skill phức tạp |
| `resources/script_integration.md` | Tích hợp scripts + 7 lớp bảo mật | Skill cần chạy lệnh hệ thống |

### Cho chuyên gia

| File | Mô tả | Khi nào đọc |
| --- | --- | --- |
| `resources/composition_cookbook.md` | 5 patterns kết hợp multi-skill | Xây hệ thống skill |
| `resources/industry_questions.md` | 8 bộ câu hỏi chuyên ngành | Skill cho ngành đặc thù |
| `resources/versioning_guide.md` | Nâng cấp + backward compat | Maintain skill lâu dài |

---

## 📚 Changelog

### v3.2 Expert Edition (2026-03-04)

- Thêm **7 Nguyên Tắc Skill Hoàn Hảo** + triết lý System Architecture vào Mindset
- Thêm **⚡ Fast Track** — lối tắt cho skill đơn giản (skip Phase 1-3)
- Thêm **📦 Full Package Output** — tạo skill package hoàn chỉnh (không chỉ 1 file)
- Thêm **5 scripts chuyên gia mới:**
  - `skill_audit.py` — Audit 7 nguyên tắc, chấm điểm S/A/B/C/D/F
  - `skill_export.py` — Export ra 6 nền tảng (Cursor, Claude, Windsurf...)
  - `skill_stats.py` — Thống kê + Cognitive Load Score
  - `skill_compare.py` — So sánh 2 phiên bản skill
  - `skill_scaffold.py` — 1 lệnh tạo skeleton skill mới
- Thêm **7 slash commands** — truy cập nhanh bằng `/skill-*`
- Thêm **scripts_guide.md** — hướng dẫn sử dụng chi tiết 7 scripts
- Thêm hỗ trợ **OpenClaw AI Gateway**
- Nâng cấp **prompt_engineering.md** (+210 dòng): 5 kỹ thuật expert + Ma Trận
- Nâng cấp **checklist.md** (+100 dòng): Expert Quality Gates + Red Flags
- Đạt **100/100 S-tier** theo self-audit 7 nguyên tắc

### v3.0 Ultimate (2026-03-03)

- Thêm `blueprints.md`, `anti_patterns.md`, `prompt_engineering.md`
- Thêm `versioning_guide.md`, `industry_questions.md`, `composition_cookbook.md`
- Thêm `simulate_skill.py`

### v2.0 Pro (2026-03-03)

- Viết lại SKILL.md — Interview-driven (5 Phase)
- Thêm `interview_questions.md`, `pattern_detection.md`

### v1.0 (2026-03-03)

- Initial release

---

## ❓ FAQ

**Q: Cần biết code không?**
A: Không. Skill Generator được thiết kế cho người KHÔNG biết code. Bạn chỉ cần mô tả công việc bằng lời.

**Q: Global hay Workspace?**
A: **Global** (`~/.gemini/antigravity/skills/`) nếu muốn dùng cho tất cả dự án. **Workspace** (`.agent/skills/`) nếu chỉ dùng cho 1 dự án.

**Q: Skill tạo ra lưu ở đâu?**
A: AI sẽ hỏi bạn muốn Global hay Workspace, rồi tự tạo file vào đúng vị trí.

**Q: Có thể sửa skill sau khi tạo không?**
A: Có. Chỉ cần mở file SKILL.md của skill đó và sửa trực tiếp, hoặc nhờ AI sửa.

**Q: Hỗ trợ ngôn ngữ nào?**
A: Tiếng Việt và tiếng Anh. AI sẽ phỏng vấn bằng ngôn ngữ bạn nói.

---

## 🤝 Đóng góp

1. Fork repository
2. Tạo branch mới: `git checkout -b feature/ten-tinh-nang`
3. Commit: `git commit -m "feat: thêm tính năng X"`
4. Push: `git push origin feature/ten-tinh-nang`
5. Tạo Pull Request

---

## 📄 License

MIT — Thoải mái sử dụng, chỉnh sửa, chia sẻ.

---

> 🇻🇳 **Được phát triển bởi Thân Công Hải** — Skill Generator v3.2 Expert Edition
> *"Biến ý tưởng thành AI Skill, biến con người thường thành kiến trúc sư AI."*
