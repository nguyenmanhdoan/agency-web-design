# Agency Web Design — Agent Skill (Multi-Industry Craft & Bricks/ACSS Handoff)

Skill thiết kế website chuẩn hóa theo đặc tả **Agent Skills** (Progressive Disclosure) dành cho **Google Antigravity**, Claude Code, Codex và Cursor. Được thiết kế riêng cho các **Web Agency đa lĩnh vực** xây dựng template và FE Demo chất lượng cao trước khi triển khai 1-to-1 sang WordPress (`bricks-acss-stack`).

## Triết lý 3 lớp (Chắt lọc tinh hoa + Tương thích 100% ACSS/Bricks)

* **Tầng 1 — Hệ khung đa lĩnh vực (chắt lọc từ UI/UX Pro Max):** 6 Visual Archetypes của Agency + Ma trận 12 lĩnh vực (B2B sản xuất, Kiến trúc/Nội thất, Y tế/Nha khoa, Bất động sản, Luật/Tài chính, SaaS, Giáo dục, F&B, Làm đẹp/Spa, Thương mại điện tử, Creative Studio, Logistics) kèm tâm lý màu sắc, nhịp section, bằng chứng chuyển đổi và lỗi cấm phạm theo từng ngành.
* **Tầng 2 — Gu thẩm mỹ & Chống AI-Slop (chắt lọc từ Taste Skill & Impeccable):** Danh mục 12 kiểu bố cục section chống lặp, bộ luật khử mùi AI (cấm card 3 cột lặp liên tiếp, cấm gradient tím-xanh, cấm bo góc/đổ bóng vô tội vạ), bộ cặp font hỗ trợ đầy đủ dấu tiếng Việt, thang chấm điểm Art Director 5 tiêu chí và bộ lệnh tinh chỉnh (`critique`, `audit`, `polish`, `bolder`, `quieter`, `distill`, `clarify`, `de-slop`).
* **Tầng 3 — Bàn giao 1-to-1 sang Bricks + ACSS (Zero Tailwind / Zero React):** Khóa chặt đầu ra về HTML5 + CSS thuần + hệ biến gương Automatic.css (`tokens.css`) + DTCG `design-system.json` (Novamira Design) + 1-level BEM + comment đánh dấu Component/JetEngine Loop để chuyển thẳng vào Stage 2 của `bricks-acss-stack`.

## Cấu trúc thư mục

```text
agency-web-design/
├── SKILL.md                                # Quy trình 4 bước, Pre-Build Gate & Hard Guardrails
├── references/
│   ├── industry-archetypes.md              # 6 Agency Visual Archetypes & Ma trận 12 lĩnh vực
│   ├── typography-and-color-vn.md          # Cặp font chuẩn dấu tiếng Việt, thang ACSS fluid & hệ màu 60-30-10
│   ├── anti-slop-and-composition.md        # Luật chống AI-slop, danh mục 12 bố cục section & Visual Richness Floor
│   ├── critique-and-polish.md              # Rubric chấm điểm Art Director 5 tiêu chí, Steering Verbs & Playwright QA
│   └── bricks-acss-handoff.md              # Quy chuẩn HTML5/CSS thuần, biến ACSS, BEM 1 cấp & DTCG design-system.json
├── scripts/
│   └── install-to-workspace.ps1            # Script cài nhanh skill vào .agents/skills/ của từng dự án
├── README.md
├── CHANGELOG.md
├── LICENSE
└── .gitignore
```

## Cài đặt

### 1. Google Antigravity

**Cài toàn cục (dùng cho mọi dự án trên máy):**

```powershell
# Windows (PowerShell)
git clone https://github.com/nguyenmanhdoan/agency-web-design.git "$env:USERPROFILE\.gemini\config\skills\agency-web-design"
```

```bash
# macOS / Linux
git clone https://github.com/nguyenmanhdoan/agency-web-design.git "$HOME/.gemini/config/skills/agency-web-design"
```

### 2. OpenAI Codex (Codex App / Codex CLI)

**Cài toàn cục (dùng cho mọi dự án trên máy):**

```powershell
# Windows (PowerShell)
git clone https://github.com/nguyenmanhdoan/agency-web-design.git "$env:USERPROFILE\.codex\skills\agency-web-design"
```

```bash
# macOS / Linux
git clone https://github.com/nguyenmanhdoan/agency-web-design.git "$HOME/.codex/skills/agency-web-design"
```

### 3. Cài cục bộ theo từng dự án (dùng chung Antigravity, Codex, Cursor)

```powershell
git clone https://github.com/nguyenmanhdoan/agency-web-design.git ".agents/skills/agency-web-design"
```

Hoặc chạy script cài vào workspace:

```powershell
.\scripts\install-to-workspace.ps1 -TargetWorkspace "C:\path\to\your\workspace"
```

### 4. Cài nhanh qua CLI (`npx skills`)

```bash
npx skills add nguyenmanhdoan/agency-web-design
```

### Cập nhật phiên bản mới

Chạy `git pull` trong thư mục skill đã cài:

```powershell
git -C "$env:USERPROFILE\.gemini\config\skills\agency-web-design" pull
git -C "$env:USERPROFILE\.codex\skills\agency-web-design" pull
```

### 5. Phối hợp với `bricks-acss-stack`

1. Dùng `agency-web-design` ở **Pha thiết kế & tạo mẫu (Stage 1 & Gate 1B)** để chốt `DESIGN.md`, `design-system.json`, `tokens.css` và các bản FE Demo HTML/CSS thuần qua kiểm duyệt trực quan trên `playwright-cli`.
2. Sau khi duyệt mẫu, bàn giao toàn bộ bundle sang **Stage 2 → Stage 4** của [bricks-acss-stack](https://github.com/nguyenmanhdoan/bricks-acss-stack) để đồng bộ lên WordPress + Bricks Builder + ACSS + JetEngine + SureRank qua MCP Novamira Pro.
