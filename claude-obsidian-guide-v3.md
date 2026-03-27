Obsidian × Claude Code Guide

ZH

EN

完整使用指南 v3.0 — 雙語版

Complete Guide v3.0 — Bilingual

Obsidian × Claude Code

把你腦子裡的開發脈絡，變成 AI 可以永久讀取的知識庫

Turn your dev context into a knowledge base AI can always read

適合初階開發者 · 含完整指令解釋 · 每個步驟都說清楚為什麼

Beginner-friendly · Every command explained · Step-by-step reasoning

初階友善Beginner Friendly

指令逐行解釋Commands Explained

8 大情境8 Real Scenarios

完整範本Full Templates

免費工具Free Tools

00 — 先看這個00 — Start Here

這份指南在說什麼？What Is This Guide About?

在學任何工具之前，先搞懂你要解決的問題，以及這套組合是怎麼解決它的。

Before learning any tool, understand the problem you're solving and how this combination solves it.

你的大腦Your Brain

想法 & 決定Ideas & Decisions

隨時在更新，但沒地方存Always updating, nowhere to store

→

Obsidian Vault

本機知識庫Local Knowledge Base

.md 檔案，Claude 可以讀.md files Claude can read

→

Claude Code

讀取脈絡Reads Context

每次啟動都知道背景Knows your background every session

→

結果Result

不用重複解釋No Re-explaining

直接接著上次繼續Pick up exactly where you left off

核心思維Core Idea

Claude Code 很強，但它有一個根本限制：每次開新 session 都是空白的，完全不記得上次的對話。你的思考脈絡、做過的決定、踩過的坑，全部消失。Obsidian Vault 就是用來解決這個問題——它是 Claude 的「外部硬碟」，讓知識可以跨 session 保存。

Claude Code is powerful, but it has one fundamental limitation: every new session starts completely blank — no memory of previous conversations. Your context, decisions, and hard-won lessons all vanish. Obsidian Vault solves this — it's Claude's "external hard drive," letting knowledge persist across sessions.

01 — 問題背景01 — The Problem

沒有 Vault 之前，你在浪費什麼？What Are You Wasting Without a Vault?

這些問題你可能每天都在遇到，但已經習慣了，不覺得是問題。

These problems probably happen to you daily. You've just gotten used to them.

❌ 現在的狀況

❌ Without Vault

每次開新 session 要重新解釋「我在做什麼」Re-explain your project every new session

做了一個技術決定，三個月後忘記原因，又重新想一遍Make a tech decision, forget why 3 months later

多個專案同時進行，上下文容易混亂Multiple projects running — context gets mixed up

靈感一來沒地方記，想記又懶得整理Ideas arrive with nowhere to put them

踩過的坑沒有記錄，之後再踩一次Hit the same bug twice because nothing was recorded

GitHub 有 code，但沒有「為什麼這樣寫」GitHub has the code, but not the "why"

✅ 有 Vault 之後

✅ With Vault

叫 Claude 讀 Vault，直接知道所有背景Tell Claude to read Vault — instant full context

所有決定都有紀錄：決定了什麼、為什麼、當時的條件Every decision recorded: what, why, and under what conditions

每個專案獨立資料夾，切換時脈絡清晰Each project has its own folder — clean context switching

靈感丟進 inbox，叫 Claude 幫你整理Dump ideas in inbox, let Claude organize them

bugs-log.md 記住所有踩過的坑bugs-log.md remembers every solved problem

Code + 脈絡 = 完整的專案記憶Code + context = complete project memory

為什麼這個問題比你想的更嚴重？Why This Problem Is Worse Than You Think

假設你做一個 SaaS 產品，從開始到 MVP 要三個月。這三個月你和 Claude Code 至少有 100 次對話。每次對話平均花 10 分鐘重新交代背景，就是 16 個小時浪費在解釋你自己已經知道的事情上。

Say you're building a SaaS product, 3 months to MVP. That's at least 100 conversations with Claude Code. If each one wastes 10 minutes re-explaining context, that's 16 hours spent explaining things you already know.

更嚴重的是決策品質的損失：沒有決策紀錄，你會在同一個問題上反覆猶豫，因為你不記得自己當初為什麼做這個選擇。有了 Vault，你可以叫 Claude「去看我之前對這個問題的分析，幫我評估現在的狀況有沒有改變」，直接站在過去的思考基礎上繼續。

Even worse is the loss of decision quality. Without decision logs, you'll second-guess the same choices repeatedly because you can't remember your original reasoning. With a Vault, you can ask Claude to "review my previous analysis on this and tell me if the conditions have changed" — building on past thinking instead of restarting.

GitHub 不夠嗎？Isn't GitHub Enough?

GitHub 很好，但它存的是結果，不是過程。GitHub is great, but it stores results, not process.

工具Tool

存什麼Stores

看得到「為什麼」嗎？See the "why"?

Claude 可以直接讀嗎？Claude can read directly?

GitHub程式碼、commit historyCode, commit history要翻 commit message，通常寫得很簡略Buried in commit messages, usually brief可以，但找特定脈絡很慢Yes, but finding context is slow

Obsidian Vault決策過程、思考脈絡、踩坑紀錄Decisions, context, bug logs✅ 這就是它的核心功能✅ That's the whole point✅ 直接讀資料夾✅ Reads the folder directly

Notion各種筆記All kinds of notes可以，但格式複雜Yes, but complex format❌ 需要 API，設定麻煩❌ Needs API, complicated setup

腦子Your Brain一切Everything記憶會消失Memory fades❌

02 — Obsidian 基礎02 — Obsidian Basics

Obsidian 到底是什麼？What Exactly Is Obsidian?

很多人聽到「知識管理工具」就覺得複雜，其實 Obsidian 的本質很簡單。

The term "knowledge management tool" sounds complex. The reality is much simpler.

最簡單的理解方式The Simplest Way to Understand It

你現在電腦上有很多 .md 檔案，比如專案的 README.md、Claude Code 用的 CLAUDE.md。你平時用 VS Code 或任何文字編輯器打開這些檔案。

You already have .md files on your computer — your project's README.md, Claude Code's CLAUDE.md. You open these in VS Code or any text editor.

Obsidian 就是一個專門用來讀寫 .md 檔案的介面，但它額外提供了幾個功能：筆記之間可以互相連結、有視覺化的連結圖、有強大的全文搜尋。就這樣。

Obsidian is simply a dedicated interface for reading and writing .md files, with a few extras: bidirectional links between notes, a visual graph of connections, and powerful full-text search. That's it.

你的資料不在 Obsidian 的伺服器，不在雲端，就在你電腦的某個資料夾裡。你關掉 Obsidian，用 VS Code 打開同一個資料夾，所有內容都還在，格式完全一樣。

Your data isn't on Obsidian's servers or in the cloud — it's in a folder on your computer. Close Obsidian, open the same folder in VS Code, and everything is still there, in exactly the same format.

ℹ️

Vault 是什麼？What is a Vault?

「Vault」是 Obsidian 對「工作資料夾」的稱呼。你告訴 Obsidian「這個資料夾是我的 Vault」，它就會把那個資料夾裡所有的 .md 檔案當成你的筆記來管理。一個 Vault = 一個資料夾。

"Vault" is Obsidian's name for your working folder. You tell Obsidian "this folder is my Vault" and it treats all the .md files inside as your notes. One Vault = one folder.

四個你會真正用到的功能Four Features You'll Actually Use

🔗

雙向連結Bidirectional Links

在任何筆記裡輸入 [[其他筆記名稱]]，Obsidian 就會自動建立連結。被連結的筆記也會知道「有人連結我」，這叫 backlink。Type [[note name]] anywhere and Obsidian creates a link automatically. The linked note also knows it's been linked — these are called backlinks.

🕸️

Graph View

按下 Cmd+G，所有筆記和它們之間的連結會以視覺化的圖形呈現。一眼看到哪些概念有關聯、哪些筆記是孤立的。Press Cmd+G to see all your notes and their connections in a visual graph. Instantly see which concepts are related and which notes are isolated.

🔍

全文搜尋Full-Text Search

Cmd+Shift+F，瞬間搜尋所有筆記的內容。比 grep 更快，也能搜標題、tags、內容。Cmd+Shift+F searches all note content instantly. Faster than grep and searches titles, tags, and body text.

⚡

快速切換Quick Switcher

Cmd+O，打幾個字母就能跳到任何一篇筆記。整個工作流可以完全用鍵盤完成。Cmd+O — type a few letters to jump to any note. Your entire workflow can be keyboard-driven.

費用說明Pricing

項目Item

費用Price

你需要嗎？Do you need it?

Obsidian 本體Obsidian App完全免費100% Free✅ 這就夠了✅ This is all you need

Obsidian Sync$4 USD/mo不需要，iCloud 或 GitHub 可免費同步No — iCloud or GitHub syncs for free

Obsidian Publish$8 USD/mo不需要（發布成網站用的）No — only needed to publish notes as a website

Commercial License$50 USD公司電腦才需要（個人用途免費）Only if used on a company computer — personal use is free

03 — 安裝設定03 — Setup

從零開始的完整設定流程Complete Setup From Zero

每個步驟都說明你在做什麼、為什麼這樣做。預計完成時間：30 分鐘。Every step explains what you're doing and why. Estimated time: 30 minutes.

1

下載 ObsidianDownload Obsidian

前往 obsidian.md 下載對應你作業系統的版本。完全免費，不需要建立帳號。Go to obsidian.md and download the version for your OS. Completely free, no account required.

ℹ️

第一次開啟會問你要「新建 Vault」還是「打開現有資料夾」。先選新建 Vault，繼續下一步。First launch asks to "Create new vault" or "Open folder as vault." Choose Create new vault for now and continue to the next step.

2

建立 Vault 資料夾結構Create the Vault Folder Structure

打開終端機，執行以下指令。每行都有說明。Open your terminal and run the following commands. Each line is explained.

bash

建立 Vault 基礎結構 — 逐行解釋Create Vault structure — line by line

# mkdir = make directory (create a folder)

# -p = create parent folders too; no error if already exists

# ~ = your home directory (/Users/yourname/ on Mac)

mkdir -p ~/vault

# cd = change directory (navigate into the folder)

cd ~/vault

# Create multiple subfolders at once

# No spaces allowed inside the curly braces

mkdir -p projects inbox decisions resources daily-notes

# ls -la = list all files with details (verify it worked)

ls -la

3

在 Obsidian 開啟這個資料夾Open the Folder in Obsidian

回到 Obsidian，選擇 Open folder as vault，導航到 ~/vault，點 Open。Back in Obsidian, choose Open folder as vault, navigate to ~/vault, and click Open.

⚠️

不要把 code repo 當 VaultDon't use a code repo as your Vault

如果你把 code repo 當 Vault，node_modules、package.json、.gitignore 這些檔案都會出現在 Obsidian 裡，搜尋和連結功能會非常雜亂。建議 Vault 和 code repo 完全分開。If you open a code repo as a Vault, node_modules, package.json, .gitignore, etc. all show up in Obsidian — search and linking become a mess. Keep Vault and code repos completely separate.

4

建立第一個專案狀態檔Create Your First Project Status File

bash

建立專案資料夾和狀態檔Create project folder and status file

# Replace "my-project" with your actual project name

mkdir -p ~/vault/projects/my-project

# cat > file

# Lets you write multi-line content directly in the terminal

# Everything between EOF markers is written to the file

cat > ~/vault/projects/my-project/status.md 'EOF'

# My Project — Status Tracker

Last updated: (update this every session)

## ✅ Completed

-

## 🔄 In Progress

-

## ⏳ Next Steps (in priority order)

1.

2.

3.

## ❓ Open Questions

-

## ⚠️ Notes & Gotchas

-

EOF

5

確認 Claude Code 可以讀取Verify Claude Code Can Read Your Vault

bash

啟動並測試Launch and test

# CRITICAL: navigate into vault BEFORE launching Claude Code

# Claude Code's working directory = the folder you launch from

cd ~/vault

claude

# Then in Claude Code, type:

# "List all .md files in this directory and describe the structure"

✅

成功的樣子Success looks like

Claude Code 應該回答類似：「我看到你的 vault 有以下結構：projects/my-project/status.md...」代表它可以正常讀取。Claude Code should respond with something like: "I can see your vault has the following structure: projects/my-project/status.md..." — that means it's working correctly.

04 — 資料夾設計04 — Folder Design

Vault 的完整結構設計Complete Vault Structure

好的結構讓你記錄更快、Claude 找脈絡更準。這裡說明每個資料夾的作用。Good structure means faster recording for you and more accurate context retrieval for Claude.

tree

完整目錄結構Complete directory structure

~/vault/

│

├── CLAUDE.md                    # ← Most important — Claude reads this every launch

│

├── projects/                    # One subfolder per active project

│   ├── project-a/

│   │   ├── status.md            # Where things are + what's next

│   │   ├── decisions.md         # All decisions with reasoning

│   │   ├── architecture.md      # System design, tech choices

│   │   └── bugs-log.md          # Bugs encountered + how they were fixed

│   └── project-b/

│       └── ...

│

├── inbox/                       # Dump ideas here without organizing

│   └── quick-capture.md         # All quick notes land here first

│

├── decisions/                   # Cross-project decisions (tech stack, architecture)

│

├── resources/                   # Learnings, research, reference notes

│   └── templates/               # Standard templates for notes

│

└── daily-notes/                 # Daily work logs (optional but useful)

└── 2026-03-26.md

📁

projects/

放什麼：每個進行中的專案各自一個子資料夾。為什麼：讓 Claude 可以精準指定「只看這個專案的脈絡」，不混入其他專案的資訊。What: One subfolder per active project.Why: Lets Claude target "only this project's context" precisely, without mixing in other projects.

📥

inbox/

放什麼：任何還沒整理的想法、靈感。為什麼：先丟進來，不用考慮格式。降低記錄的摩擦力，之後叫 Claude 整理。What: Any unorganized ideas, thoughts, notes.Why: Capture first, organize later. Lowering the barrier to record anything means you actually record things. Ask Claude to sort it later.

📚

resources/

放什麼：整理好的技術筆記、學習研究。為什麼：一個月後這裡會變成你自己的技術手冊，全部都是你真正驗證過的解法。What: Organized tech notes, research, learnings.Why: After a month, this becomes your personal reference manual — every entry a solution you've actually verified.

05 — 核心設定05 — Core Config

CLAUDE.md：你和 AI 之間的永久契約CLAUDE.md: Your Permanent Contract with AI

放在 vault 根目錄，Claude Code 每次啟動都會自動讀取。相當於你永久告訴 Claude「你是誰、在做什麼、有什麼規則」。

Placed in the vault root, Claude Code reads this automatically every launch. It's a permanent declaration of who you are, what you're building, and what rules apply.

💡

為什麼要有這個：沒有 CLAUDE.md，每次 session 你都要重新介紹自己和你的專案。有了它，這些資訊自動載入，你直接進入工作狀態。Why it matters: Without CLAUDE.md, every session starts with you re-introducing yourself and your project. With it, all that context auto-loads and you go straight to work.

markdown

~/vault/CLAUDE.md 完整範本~/vault/CLAUDE.md full template

# CLAUDE.md — Your Name's Dev Vault

---

## About Me

- Role: [your role, e.g. solo developer, frontend engineer]

- Main stack: [e.g. Next.js, TypeScript, Supabase, Tailwind CSS]

- Experience level: [e.g. learning, 2 years experience]

- Preferred response language: English

---

## Active Projects

### Project A: [Project Name]

- One-liner: [e.g. membership management system for hair salons]

- Stack: [e.g. Next.js + Supabase + Shadcn UI + Stripe]

- Current phase: [e.g. MVP development, targeting April launch]

- Status file: projects/project-a/status.md

### Project B: [Project Name]

- One-liner: [description]

- Status file: projects/project-b/status.md

---

## Rules (apply every session)

### Before starting work

1. Ask me which project we're working on

2. Read the corresponding projects/[name]/status.md

3. Tell me the current state, then wait for my instructions

### During work

- After important decisions, ask if I want them logged to decisions.md

- After fixing a bug, ask if I want it logged to bugs-log.md

- When unsure, ask — don't guess and make changes

### Before ending a session

- Update the project's status.md

- Remind me of anything still unresolved

### Always

- **Never delete any files** unless I explicitly say "please delete [filename]"

- **Explain commands** before I run them — don't just give me blind instructions

---

## Vault Structure

- projects/  → per-project context and status

- inbox/     → unorganized quick captures

- decisions/ → cross-project major decisions

- resources/ → tech notes and reference material

06 — 實際情境06 — Real Scenarios

8 個你每天都會遇到的情境8 Scenarios You'll Face Every Day

每個情境說明問題是什麼、為什麼會發生、以及完整的操作指令。Each scenario explains the problem, why it happens, and the exact commands to handle it.

1

每天開始工作 — 接續上次的狀態Starting Work — Resuming From Where You Left Off

問題：Problem: 你昨天做到一半，今天開新 session，完全忘了上次在幹嘛。You left off yesterday mid-task. Today's new session has no memory of it.

流程workflow每天開始工作的標準程序Standard start-of-day routine

# Step 1: Navigate to vault

cd ~/vault

# Step 2: Launch Claude Code

claude

# Step 3: In Claude Code, type:

"Read projects/my-project/status.md,

tell me the current state and what's next,

then wait for me to tell you where to start."

2

做了技術決定 — 記錄下來，未來可以查Made a Technical Decision — Log It For Future Reference

問題：Problem: 你和 Claude 討論了一個小時，選定了某個方案。session 結束，理由消失。You discussed a decision for an hour and landed on a solution. Session ends — the reasoning vanishes.

指令prompt決策結束後立刻執行Run immediately after making a decision

"Please log the decision we just made to

projects/my-project/decisions.md.

Include: today's date, the decision, options we considered,

reasons for our choice, and under what conditions

we should revisit this decision."

💡

進階用法：Pro tip: 三個月後想重新評估，叫 Claude：「讀取 decisions.md 裡的 [決定名稱]，告訴我當時的評估條件，幫我看看現在有沒有改變。」Months later, ask Claude: "Read the [decision name] entry in decisions.md, tell me the original conditions, and evaluate whether anything has changed."

3

靈感突然來 — 快速記錄，不破壞工作流Sudden Idea — Capture Fast Without Breaking Flow

問題：Problem: 你在做 A 功能時突然想到 B 的做法，打開 Obsidian 整理太麻煩，最後就忘了。You're working on feature A when an idea for feature B strikes. Opening Obsidian to organize feels like too much effort, so you forget it.

bash最快的記錄方式Fastest capture method

# echo outputs text, >> appends to file end (doesn't overwrite)

# If the file doesn't exist, >> creates it automatically

echo "Consider adding Google OAuth to reduce login friction" >> ~/vault/inbox/quick-capture.md

# With a date stamp:

echo "$(date +%Y-%m-%d) Consider adding Google OAuth" >> ~/vault/inbox/quick-capture.md

指令prompt整理 inboxSort inbox later

"Read inbox/quick-capture.md and sort the contents:

- Anything related to my-project → add to projects/my-project/

- Tech research ideas → add to resources/

- Cross-project decisions → add to decisions/

Tell me what you moved where, then clear quick-capture.md."

4

踩到 Bug — 記錄解法，避免下次再踩Hit a Bug — Log the Fix So You Never Hit It Again

問題：Problem: 你花了兩小時解決一個 bug，解掉了，繼續往前。兩個月後，同樣的 bug 又出現了。You spent two hours fixing a bug. Two months later, the same bug appears somewhere else.

指令prompt解完 bug 立刻執行Run immediately after fixing

"Log the bug we just fixed to projects/my-project/bugs-log.md.

Format:

- Date

- Symptoms (what error message/behavior was seen)

- Root cause (why it happened)

- Fix (complete steps or code)

- Prevention (how to avoid this in future)"

5

多專案切換 — 不把不同專案的脈絡混淆Switching Projects — Clean Context Switch

問題：Problem: 你同時在做三個專案，Claude 有時候會把 A 的技術細節帶進 B 的討論裡。You're running three projects simultaneously. Claude sometimes carries details from project A into project B discussions.

指令prompt切換專案的標準流程Standard project switch procedure

"We're switching to project-b now.

Please:

1. Clear all project-a details from your working memory

2. Read all .md files in projects/project-b/

3. Tell me this project's current status and tech stack

4. Wait for my instructions"

6

每天結束工作 — 更新進度，為明天做準備Ending Work — Update Progress for Tomorrow

問題：Problem: 今天做了很多事，但沒有記錄。明天又要重新想「昨天做到哪了」。You did a lot today but recorded nothing. Tomorrow you'll waste time figuring out where you left off.

指令prompt每天結束前的固定指令（只需 30 秒）End-of-day routine (takes 30 seconds)

"Session's done. Please update projects/my-project/status.md:

1. Move completed items to the 'Completed' list

2. Update 'In Progress' items

3. Update 'Next Steps' to reflect tomorrow's priorities

4. Note anything unresolved from today

5. Update the 'Last updated' date

Show me the result so I can confirm."

7

查找過去的資訊 — 不靠記憶，靠搜尋Finding Past Information — Search, Not Memory

問題：Problem: 「我記得我之前研究過這個，但忘了結論是什麼」"I know I researched this before, but I can't remember the conclusion."

bash在 Vault 搜尋關鍵字Search Vault by keyword

# grep: search text. -r: recursive. -l: list filenames only. -i: case-insensitive

grep -r -l -i "API" ~/vault --include="*.md"

# Show matching lines with filename and line number:

grep -r -n -i "API" ~/vault --include="*.md"

# Or in Obsidian GUI: Cmd+Shift+F

8

知識沉澱 — 把學到的技術記下來Knowledge Capture — Record What You Learned

問題：Problem: 你研究了一個技術，搞懂了，繼續往前。下次遇到類似問題，又要重新研究一遍。You researched a technology, figured it out, and moved on. Next time you hit a similar problem, you research it all over again.

指令prompt存成知識筆記Save as a knowledge note

"Summarize what we just learned about [technology] into a

reference note saved at resources/[topic]-notes.md.

Format:

- When you'd encounter this problem

- Why it happens (the underlying mechanism)

- The solution (copy-paste ready code)

- Related references

Make it useful enough that reading it next time solves the problem."

07 — 指令總覽07 — Command Reference

所有指令，逐一解釋Every Command, Explained

這裡把所有指令集中在一起，每個都說明在幹嘛。可以當作備忘清單。All commands in one place, each one explained. Use this as your cheatsheet.

終端機指令（bash）Terminal Commands (bash)

cd ~/vault

切換工作目錄到 VaultSwitch working directory to Vault

cd = change directory。~ 是你的家目錄。這個指令讓你「進入」vault 資料夾。一定要先執行這個，再啟動 Claude Code，否則 Claude 看不到你的筆記。

cd = change directory. ~ is your home directory. This "enters" the vault folder. Always run this before launching Claude Code — otherwise Claude can't see your notes.

claude

啟動 Claude CodeLaunch Claude Code

在 cd ~/vault 之後執行。Claude Code 會以當前資料夾作為工作目錄，就能讀取所有 .md 筆記。

Run after cd ~/vault. Claude Code uses the current folder as its working directory, giving it access to all your .md notes.

mkdir -p ~/vault/projects/new-project

建立新專案資料夾Create a new project folder

mkdir = make directory。-p = 如果中間資料夾不存在也一起建立，且已存在不報錯。把 new-project 換成你的專案名稱。

mkdir = make directory. -p = create parent folders if they don't exist, and don't error if already exists. Replace new-project with your actual project name.

echo "text" >> ~/vault/inbox/quick-capture.md

快速附加文字到 inboxQuickly append text to inbox

echo 輸出文字。>> 附加到檔案末尾（不覆蓋）。如果用 > 就會覆蓋，注意差別。如果檔案不存在，>> 會自動建立。

echo outputs text. >> appends to the end of a file (doesn't overwrite). Using > would overwrite — note the difference. If the file doesn't exist, >> creates it.

grep -r -l "keyword" ~/vault --include="*.md"

搜尋所有筆記裡包含某個關鍵字的檔案Search all notes for a keyword

grep = 搜尋文字。-r = 包含子資料夾。-l = 只列出檔案名稱。--include="*.md" = 只搜 .md 檔案。

grep = search text. -r = include subfolders. -l = list filenames only. --include="*.md" = only search .md files.

find ~/vault -name "*.md" | head -30

列出 Vault 裡前 30 個 .md 檔案List first 30 .md files in Vault

find 找出所有符合條件的檔案。| head -30 = 只顯示前 30 個。用來快速查看 vault 的內容。

find locates all matching files. | head -30 = show only the first 30. Use this to quickly audit what's in your vault.

給 Claude 的指令範本Claude Prompt Templates

情境Scenario

指令範本Prompt Template

開始工作Start work"Read projects/my-project/status.md, tell me the current state, wait for my instructions"

切換專案Switch project"Switch to project-b, clear project-a from memory, read all project-b notes, tell me its status"

記錄決定Log decision"Log our decision to decisions.md: date, decision, options considered, reasoning, re-evaluation conditions"

記錄 bugLog bug"Log this bug to bugs-log.md: symptoms, root cause, fix, prevention"

整理 inboxSort inbox"Read inbox/quick-capture.md, sort contents to the right places, tell me what you moved"

結束工作End session"Update status.md: completed items, in-progress, tomorrow's priorities, unresolved issues"

查詢歷史Search history"Search the entire vault for notes related to [keyword], tell me what you find and where"

存技術筆記Save tech note"Summarize what we learned about [topic] into resources/[topic]-notes.md for future reference"

08 — 進階技巧08 — Advanced Tips

讓工作流更強大的進階設定Power-User Setup

這些不是必須的，但設定好之後能大幅提升效率。None of these are required, but each one meaningfully speeds up your workflow.

技巧一：Shell Alias，一個字啟動Tip 1: Shell Alias — Launch With One Word

每次輸入 cd ~/vault && claude 有點麻煩。設定一個 alias，之後只要打兩個字。Typing cd ~/vault && claude every time is tedious. Set an alias to do it in two keystrokes.

bash設定 alias（只需要做一次）Set up aliases (one-time setup)

# Open your shell config file

# zsh (macOS default):

nano ~/.zshrc

# bash:

nano ~/.bashrc

# Add these lines at the bottom:

alias vault="cd ~/vault && claude"

alias note='f(){ echo "$(date +%Y-%m-%d) $*" >> ~/vault/inbox/quick-capture.md; }; f'

# Save (Ctrl+X, Y, Enter) then reload:

source ~/.zshrc

bash使用Using your aliases

# Launch vault + Claude Code in one word:

vault

# Capture a quick note from anywhere:

note "Consider adding Google OAuth to reduce login friction"

# Saves: "2026-03-26 Consider adding Google OAuth..."

技巧二：iCloud 免費跨裝置同步Tip 2: Free Cross-Device Sync With iCloud

不需要付費的 Obsidian Sync，用 iCloud 就能讓手機也能讀寫 Vault。No need for paid Obsidian Sync. iCloud lets your phone read and write to the same Vault.

bash移動 Vault 到 iCloud（macOS）Move Vault to iCloud (macOS)

# iCloud's Obsidian folder path:

ICLOUD="~/Library/Mobile Documents/iCloud~md~obsidian/Documents"

# Create if it doesn't exist:

mkdir -p "$ICLOUD"

# Move vault there:

mv ~/vault "$ICLOUD/vault"

# Create a symlink so ~/vault still works:

# ln -s original_path link_name

ln -s "$ICLOUD/vault" ~/vault

ℹ️

Symlink 就是捷徑——你還是可以用 ~/vault 這個路徑，但資料實際存在 iCloud，會自動同步到手機。在手機上安裝 Obsidian app，選擇 iCloud 裡的 vault，就能隨時記錄。A symlink is a shortcut — you still use ~/vault as the path, but the data lives in iCloud and syncs to your phone automatically. Install Obsidian on iOS, select the vault from iCloud, and you can capture notes anywhere.

技巧三：建立筆記範本Tip 3: Note Templates

每次記錄決定、bug，都要想格式很煩。先建好範本，叫 Claude 照著填。Deciding on a format every time you log a decision or bug is friction. Pre-build templates and tell Claude to use them.

bash建立決策紀錄範本Create decision log template

mkdir -p ~/vault/resources/templates

cat > ~/vault/resources/templates/decision.md 'EOF'

## YYYY-MM-DD [Decision Title]

**Final decision:**

**Background:** (why this decision was needed)

**Options considered:**

| Option | Pros | Cons |

|--------|------|------|

| Option A | | |

| Option B | | |

**Reasoning for choice:**

**Re-evaluation conditions:** (when should we revisit this?)

EOF

最重要的原則The Most Important Principle

不要追求完美的結構。先開始記，之後再優化。一個不完美但有在用的 Vault，遠比一個完美但沒在用的 Vault 有價值。從最小可行的結構開始：CLAUDE.md + projects/ + inbox/，這樣就夠了。其他的等你真的需要再加。

Don't chase the perfect structure. Start recording, optimize later. An imperfect Vault you actually use is infinitely more valuable than a perfect one you never touch. Minimum viable structure: CLAUDE.md + projects/ + inbox/. That's enough. Add everything else only when you genuinely need it.

09 — 錯誤警告09 — Mistakes & Misconceptions

新手最常踩的雷The Most Common Mistakes Beginners Make

這些錯誤幾乎每個人都會犯。有些只是讓工作流變差，有些會讓你的資料消失或 Claude 完全失效。提前知道，就不用親身踩坑。

Almost everyone makes these mistakes. Some just hurt your workflow. Others can destroy your data or make Claude useless. Know them in advance.

💀

絕對不能犯Never Do This

這些錯誤可能造成資料永久遺失或讓整個工作流崩潰These can cause permanent data loss or completely break your workflow

FATAL 01

從 code repo 目錄啟動 Claude Code，不是從 vaultLaunching Claude Code from the code repo, not the vault

❌ 錯誤做法❌ Wrong

bash

# 從 code repo 啟動 — Claude 看不到你的 vault 筆記

cd ~/my-project-code

claude

✅ 正確做法✅ Correct

bash

# 永遠從 vault 啟動，然後在 CLAUDE.md 裡標明 code 的路徑

cd ~/vault

claude

為什麼這麼嚴重：Claude Code 的工作目錄決定它能「看到」什麼檔案。從 code repo 啟動，它完全看不到你 vault 裡的任何筆記。你寫了幾個月的脈絡、決策紀錄、bugs log 全部對它不存在。整個 vault 系統完全失效。Why this is critical: Claude Code's working directory determines what files it can see. Launch from the code repo, and it's blind to everything in your vault — months of context, decision logs, bug records. The entire vault system is dead.

FATAL 02

叫 Claude 直接刪檔案，沒有確認機制Letting Claude delete files without a confirmation step

為什麼這麼嚴重：Claude Code 有能力直接刪除你的 vault 檔案，而且這個操作是無法復原的（除非你有 Git 備份）。如果你的 CLAUDE.md 沒有寫「不刪任何檔案」的規則，某些情境下 Claude 可能自行判斷「這個檔案沒用了」然後刪掉它。你三個月的決策紀錄就這樣消失。Why this is critical: Claude Code can delete your vault files directly, and that action is irreversible (unless you have a Git backup). Without a "never delete files" rule in CLAUDE.md, Claude might decide a file looks unused and remove it. Three months of decision logs: gone.

🛡️

防護措施：在 CLAUDE.md 的規則裡加上「不刪任何檔案，除非我明確說「請刪掉 [檔案名稱]」」。然後定期把 vault 用 Git 備份：cd ~/vault && git init && git add . && git commit -m "backup"Protection: Add to CLAUDE.md rules: "Never delete any file unless I explicitly say 'please delete [filename]'." Also back up your vault with Git regularly: cd ~/vault && git init && git add . && git commit -m "backup"

FATAL 03

把 .env 或機密資訊放進 vault，然後把 vault 推上 GitHubPutting .env or secrets in the vault, then pushing to GitHub

為什麼這麼嚴重：很多人會把「踩坑紀錄」裡的環境變數、API key 或密碼直接複製貼上進筆記，然後把 vault 推上 GitHub 做備份。這會把你的機密資訊公開給全世界。Why this is critical: Many people copy environment variables, API keys, or passwords into their bug logs, then push the vault to GitHub for backup. This exposes your secrets to the world.

🛡️

防護措施：在 vault 根目錄建立 .gitignore，列出不推上 GitHub 的檔案。筆記裡永遠用佔位符代替真實值：API_KEY=&lt;your-key-here&gt;，不要貼真正的 key。Protection: Create a .gitignore in the vault root to exclude sensitive files. In notes, always use placeholders instead of real values: API_KEY=&lt;your-key-here&gt; — never paste actual keys.

⚠️

新手常犯的錯Common Beginner Mistakes

不會讓資料消失，但會讓整個系統越來越沒用Won't lose data, but will make the whole system less and less useful over time

COMMON 01

status.md 寫了，但從來不更新Creating status.md but never updating it

最常見的問題。你第一次設定 vault 時認真填了 status.md，然後一週後它就過時了，但你繼續叫 Claude 讀它。Claude 拿到的是錯誤的現狀，給你的建議也會跑偏。The most common problem. You carefully fill out status.md on day one, then a week later it's outdated — but you keep telling Claude to read it. Claude gets a false picture of reality and its suggestions drift off course.

解法Fix

把「更新 status.md」設為每次 session 結束前的固定習慣，只要 30 秒。或者在 CLAUDE.md 的規則裡寫「每次工作結束前自動更新 status.md」，讓 Claude 提醒你。Make "update status.md" a non-negotiable end-of-session habit — it takes 30 seconds. Or add to CLAUDE.md rules: "before ending any session, update the project's status.md" so Claude reminds you.

COMMON 02

把整個 code repo 當 vault 用Using your entire code repo as the vault

很多人覺得「我的 code repo 裡已經有 README.md，直接把那個資料夾當 vault 不就好了？」結果是：Obsidian 裡充滿了 node_modules、.gitignore、package.json、build 產物，搜尋功能幾乎廢掉，graph view 變成一團亂，Claude 讀取時也容易被不相關的檔案干擾。Many people think "my repo already has a README.md, why not just use that folder as the vault?" The result: Obsidian fills with node_modules, .gitignore, package.json, build artifacts. Search becomes useless, graph view becomes noise, and Claude gets confused by irrelevant files.

解法Fix

Vault 和 code repo 永遠分開。在 vault 裡的 CLAUDE.md 或 projects 筆記裡標明 code 的路徑，需要的時候叫 Claude 去讀那個路徑。Always keep vault and code repo separate. In CLAUDE.md or your project notes, record where the code lives. Tell Claude to read that path when needed.

COMMON 03

CLAUDE.md 寫了「回答用中文」，但從來不更新其他內容Writing CLAUDE.md once and never touching it again

CLAUDE.md 是活的文件，不是一次性設定。你的技術棧換了、新增了專案、規則需要調整——但 CLAUDE.md 還停在三個月前的狀態。Claude 每次讀到的都是過時的自我介紹。CLAUDE.md is a living document, not a one-time config. Your stack changes, new projects start, rules need adjusting — but CLAUDE.md is frozen three months in the past. Every session, Claude loads an outdated picture of you.

解法Fix

每個月花 5 分鐘回顧 CLAUDE.md，確認內容還是準確的。每當有重大改變（換技術棧、完成一個專案、新增規則），立刻更新。Spend 5 minutes reviewing CLAUDE.md monthly to make sure it's still accurate. Whenever something significant changes — new tech stack, completed project, new rule — update it immediately.

COMMON 04

inbox 只進不出，變成垃圾堆Inbox only ever fills up — never gets sorted

inbox 的設計是「快速丟入，定期整理」，不是「永久倉庫」。如果你只丟不整理，三個月後 inbox 有 500 條雜亂的筆記，Claude 讀了也找不到重點，你自己也不想看它。The inbox is designed for "dump fast, sort later" — not as a permanent storage bin. If you only dump and never sort, after three months you have 500 jumbled notes. Claude can't find the signal in the noise, and you won't want to open it either.

解法Fix

每週至少一次叫 Claude 整理 inbox：「讀取 inbox/quick-capture.md，把內容整理到對應位置，然後清空它。」設個週期提醒自己。At least once a week, ask Claude to sort inbox: "Read inbox/quick-capture.md, move contents to the right places, then clear it." Set a recurring reminder.

COMMON 05

每次叫 Claude 讀「所有檔案」，沒有聚焦Asking Claude to read "all files" without focusing

「請讀取我的整個 vault 然後告訴我現在的狀態」——這個指令讓 Claude 要處理大量不相關的內容，消耗大量 context window，而且得到的回答往往很泛泛。"Please read my entire vault and tell me the current state" — this forces Claude to process huge amounts of irrelevant content, burns through context window, and produces vague, unfocused answers.

解法Fix

永遠指定具體路徑：「讀取 projects/my-project/status.md」而不是「讀取整個 vault」。越精準的指令，Claude 給的回答越有用。Always specify the exact path: "Read projects/my-project/status.md" — not "read the entire vault." The more precise your instruction, the more useful Claude's response.

🌀

常見誤區Common Misconceptions

很多人對 Obsidian + Claude Code 的錯誤理解，導致用錯方向Wrong mental models that cause people to use the system incorrectly from the start

❌

「Obsidian 會幫我自動記錄東西」"Obsidian will automatically record things for me"

不會。Obsidian 只是一個介面，它不會主動幫你記任何東西。記錄這件事永遠是你（或你叫 Claude）主動做的動作。Obsidian 提供的是一個好的結構和搜尋，讓你記下來的東西有地方找。It won't. Obsidian is just an interface. It doesn't proactively record anything. Recording is always an active action — either by you or by Claude when you instruct it. Obsidian provides structure and search so that what you do record can be found.

❌

「Claude 讀了 CLAUDE.md 就永遠記得了」"Claude reads CLAUDE.md and then remembers it forever"

不是。Claude 在每次 session 開始時讀取 CLAUDE.md，但這只存在於那個 session 的 context 裡。下次開新 session，它會再讀一次。它並沒有「記住」——它只是每次都重新讀取。這也是為什麼 CLAUDE.md 要保持準確。No. Claude reads CLAUDE.md at the start of each session, but it only exists within that session's context. Next session, it reads again. Claude isn't "remembering" — it's re-reading every time. This is why keeping CLAUDE.md accurate matters.

❌

「Vault 要建得很完整才能開始用」"The vault needs to be fully built before I start using it"

這是最大的誤區，也是讓大多數人放棄的原因。你只需要 CLAUDE.md + 一個 projects/ 資料夾就能開始。結構是隨著使用慢慢長出來的，不是一開始就設計好的。今天先建最小的，明天再加一個資料夾。This is the biggest misconception, and the reason most people quit before starting. You only need CLAUDE.md + one projects/ folder to begin. Structure grows through use, not upfront design. Build the minimum today, add one folder tomorrow.

❌

「筆記要寫得很好才值得記」"Notes need to be well-written to be worth keeping"

完全不對。Vault 裡可以有「今天試了 X，不行」這種一行筆記，可以有亂七八糟的草稿，可以有根本沒格式的隨手記。重點是有記，哪怕只有一句話。你叫 Claude 整理的前提是「有東西可以整理」。Completely wrong. Your vault can have "tried X today, didn't work" as a one-liner. Messy drafts, unformatted captures — all fine. The point is that something exists. You can't ask Claude to organize nothing.

❌

「這套系統適合所有人」"This system works for everyone"

不是。如果你的工作很簡單、只有一個短期專案、或者你本來就有很好的記憶力，這套系統可能是 overkill。它最適合：同時進行多個專案、需要跨 session 保持脈絡、或者決策很複雜需要留紀錄的人。It's not. If your work is simple, you're running a single short project, or you have excellent memory, this system might be overkill. It's best for: running multiple concurrent projects, needing cross-session context, or making complex decisions that need to be logged.

❌

「Vault 可以完全取代 GitHub」"The vault can replace GitHub"

不行，兩個是互補的，不是替代關係。GitHub 存 code，Vault 存思考脈絡。缺少任何一個都不完整。理想狀態是：GitHub 知道你做了什麼，Vault 知道你為什麼這樣做。No — they're complementary, not alternatives. GitHub stores code. Vault stores thinking. Missing either is incomplete. The ideal: GitHub knows what you built, Vault knows why you built it that way.

快速對照表Quick Reference

行為Action

嚴重程度Severity

後果Consequence

從 code repo 啟動 Claude（不是 vault）Launching Claude from code repo, not vault💀 致命Fatal整個 vault 系統對 Claude 不存在Vault is completely invisible to Claude

讓 Claude 刪檔案，沒有規則限制Allowing Claude to delete files without rules💀 致命Fatal筆記永久消失，無法復原Notes gone forever, unrecoverable

把機密放進 vault 然後推上 GitHubPushing secrets to GitHub via vault💀 致命Fatal機密資訊公開洩漏Secrets publicly exposed

status.md 從不更新Never updating status.md⚠️ 嚴重SeriousClaude 拿到錯誤現狀，建議跑偏Claude works from false context, suggestions drift

code repo 當 vault 用Using code repo as vault⚠️ 嚴重Serious搜尋廢掉，Claude 被雜訊干擾Search broken, Claude confused by noise

CLAUDE.md 從不更新Never updating CLAUDE.md⚠️ 嚴重SeriousClaude 每次載入過時的背景資訊Claude loads stale background every session

inbox 永遠不整理Never sorting inboxℹ️ 輕微Minorinbox 變垃圾堆，慢慢失去價值Inbox becomes noise, gradually loses value

叫 Claude 讀整個 vault 而非指定路徑Asking Claude to read "entire vault" vs specific pathℹ️ 輕微Minor消耗過多 context，回答變泛泛Burns context window, answers become vague