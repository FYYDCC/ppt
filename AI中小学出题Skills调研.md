# AI 中小学出题 Skills 汇总

> 调研时间：2026 年 10 月。适用于支持 Agent Skills（`SKILL.md`）的工具：Claude Code、Claude.ai、Cursor、Codex、Gemini CLI 等。

## 一、总表

| # | Skill | 语言 / 适用地区 | 学段 | 学科 | 主要功能 | 答案校验 | 输出格式 | 来源 |
|---|---|---|---|---|---|---|---|---|
| 1 | 测评设计师 `xiaozhi-teach-exam-designer` | 简体 / 大陆 | 义务教育、高中 | 全学科 | 按课标四级出双向细目表、控制难度配比、评分细则、考后返修清单 | 出题自检清单 | 文本、表格 | [360 技能中心](https://skillhub.360.com/skills/qizhitang/xiaozhi-teach-exam-designer) |
| 2 | exam-paper-generator | 简体 / 大陆 | 中小学 | 全学科 | 确认需求后出组卷方案，确认后出卷，输出教师版和学生版 | 脚本校验分值和结构 | HTML | [GitHub](https://github.com/susirial/solo_com_gen_exam) |
| 3 | exam-generator（中国中小学试卷生成器） | 简体 / 大陆 | 小学、初中 | 语数英理化生史地政 | 按知识点、题型、难度出整卷 | 联网交叉验证，标注置信度 | 标准试卷版式 | [Skills Directory](https://www.skillsdirectory.com/skills/whyzsm-exam-generator) |
| 4 | teacher-kit | 简体 / 大陆 | 小学到研究生 | 全学科 | 教案、试题、大纲、课件大纲、说课稿 | 无 | 文本 | [GitHub](https://github.com/dongsheng123132/teacher-kit) |
| 5 | gaokao-expert | 简体 / 大陆 | 高中 | 全学科 | 高考命题指导与试题评审（七个维度） | 人工评审框架 | 文本 | [GitHub](https://github.com/staruhub/ClaudeSkills/blob/main/lab/Geek-skills-gaokao-expert/SKILL.md) |
| 6 | 智能组卷出题 | 简体 / 大陆 | 中小学 | 全学科 | 试卷正文、答题卡、参考答案、评分标准 | 未说明 | 平台内输出 | [扣子](https://xiaping.coze.com/skill/3e125d51-dbbc-4b10-9d0d-dc5f14fd93a2) |
| 7 | lecture-builder | 简体 / 大陆 | 中学 | 含图含公式学科 | 把已有知识点和题目文档合成讲义 | 无（使用原题） | Word（学生版、教师版） | [GitHub](https://github.com/dhcnsa-netizen/lecture-builder) |
| 8 | ExamLoop | 简体 | 大学为主，可用于高中 | 文理通用 | 资料提炼、出题练习并批改、解题讲解、模拟出卷 | 自动批改 | HTML | [GitHub](https://github.com/munyoung-ovo/ExamLoop) |
| 9 | teaching-exam-skills | 繁体 / 台湾 | 初中 | 数学 | 段考出题与审题、双向细目表、情境题、几何配图、小游戏 | 审题模式 | Word、SVG、HTML | [GitHub](https://github.com/mathruffian-dot/teaching-exam-skills) |
| 10 | tw-edu-skills | 繁体 / 台湾 | K-12 | 全学科 | 素养导向试题、学习单、评量规准、防 AI 作弊评量等 19 个技能 | 无 | 多种 | [GitHub](https://github.com/fw1201/tw-edu-skills) |
| 11 | k12-teacher-skills（Anthropic 官方） | 英文 / 美国 | K-12 | 数学为主 | 1–3 题形成性小测，干扰项来自已知误区，附教学建议 | 官方评测框架 | 文本 | [GitHub](https://github.com/anthropics/k12-teacher-skills) |
| 12 | Quiz Generator（SkillMedev） | 英文 | 通用 | 全学科 | 先定 Bloom 分布再出题，干扰项对应误区，答案附理由 | 理由和误区说明 | 文本 | [GitHub](https://github.com/SkillMedev/skills/blob/main/skills/quiz-generator/SKILL.md) |
| 13 | quiz-generator（pm-claude-skills） | 英文 | 通用 | 全学科 | 每题标注难度和 Bloom 层级，附答案解析 | 解析 | 文本；提供 Cursor `.mdc` 版 | [GitHub](https://github.com/mohitagw15856/pm-claude-skills) |
| 14 | Assessment/Quiz/Test Generator | 英文 / 美国 | K-12 | 全学科 | 联网查课标、DOK 分布、评分量规、A/B 卷 | 联网查询 | 可打印格式 | [Claude SkillHub](https://claudeskillhub.com/skills/assessment-quiz-test-generator) |
| 15 | AI Quiz & Worksheet | 英文 / 美国 | K-12 | 全学科 | DOK 标签、错误选项原因、出口票、特殊需求学生版本 | 错误选项说明 | 可打印练习单 | [AI Agents Library](https://www.aiagentslibrary.com/skills/ai-quiz-worksheet/) |
| 16 | bloom-taxonomy-quiz-builder | 英文 | 通用 | 阅读类为主 | 读入材料，每个 Bloom 层级出一题并逐题确认 | 逐题确认 | JSON | [GitHub](https://github.com/bobuel/bloom-taxonomy-quiz-builder-skill) |
| 17 | Teacher worksheet 命令 | 英文 | K-12 | 数学、阅读、词汇 | 三层分层练习单，附分步答案 | 无 | 文本 | [GitHub](https://github.com/alexclowe/awesome-claude-cowork-plugins/blob/main/teacher/commands/worksheet.md) |
| 18 | education-agent-skills | 英文 | 通用 | 全学科 | 165 个循证教育技能，含试卷效度检查、形成性评价选择 | 效度和信度审查 | 报告 | [GitHub](https://github.com/GarethManning/education-agent-skills) |
| 19 | math-worksheets | 英文 | 小学到高中 | 数学 | 练习卷、分步答案、知识点小结 | **SymPy 强制校验** | LaTeX PDF | [ClawHub](https://clawhub.ai/trondw/skills/math-worksheets) |
| 20 | math-skill | 英文 | 小学到高中 | 数学 | 解题、出练习单、诊断，支持拍照识题 | SymPy 校验脚本 | 文本、图像 | [GitHub](https://github.com/googlarz/math-skill) |
| 21 | reading-comprehension-text-adapter | 英文 | 中小学 | 英语 | 测量并改写文本难度（CEFR），设计阅读题，检查题型搭配 | 脚本检查 | 文本 | [Vector Skills](https://agenticskills.vector-ai-lab.com/skills/reading-comprehension-text-adapter/) |
| 22 | cefr-reading-coach | 英文 | 中学及以上 | 英语 | 把真实文章改写到指定 CEFR 等级并练习 | 无 | 文本、音频 | [GitHub](https://github.com/ystyleb/cefr-reading-coach) |
| 23 | docx / pdf / xlsx / pptx（Anthropic 官方） | 通用 | — | — | 生成 Word 试卷、PDF、细目表、讲评课件 | 渲染后自查版面 | Office、PDF | [GitHub](https://github.com/anthropics/skills) |

---

## 二、通用安装方法

后面各节如果没有写专门的安装命令，就按下面的方法装。

1. **下载 Skill 文件夹**（含 `SKILL.md` 的那个目录）：
   ```powershell
   git clone https://github.com/<作者>/<仓库>.git
   ```
2. **复制到 Skills 目录**：
   | 工具 | 目录 |
   |---|---|
   | Claude Code（个人） | `C:\Users\<用户名>\.claude\skills\<skill名>\` |
   | Claude Code（项目） | `<项目>\.claude\skills\<skill名>\` |
   | Cursor | `C:\Users\<用户名>\.cursor\skills\<skill名>\` 或 `<项目>\.cursor\skills\` |
   | Claude.ai 网页 | 设置 → Skills → 上传 zip 或 `.skill` 文件 |
3. **一键安装**（仓库支持时）：
   ```powershell
   npx skills add <作者>/<仓库> [skill名] -a claude-code
   ```
4. **使用**：新开对话，直接说触发语（如"帮我出一份初二数学期中试卷"），AI 会自动加载对应 Skill。
5. **安全**：Skill 可能包含可执行脚本，安装前先看一遍 `scripts/` 目录。

---

## 三、各 Skill 介绍与使用教程

### 1. 测评设计师 `xiaozhi-teach-exam-designer`

**介绍**：面向教师的规范命题工具，目标是"按双向细目表命题"而不是拼凑题目。认知层级采用 2022 版课标的四级（了解 / 理解 / 掌握 / 运用），并附与 Bloom 的对照表。内置规则：
- 难度按 基础:中等:较难 = 6:3:1 起步。
- 认知层级按分值配比，如终结性测评为 了解 15% + 理解 30% + 掌握 40% + 运用 15%；"运用"层不得为 0，校内测评不超过 20%。
- 新题生成前自检：有解、唯一、不超纲、与细目表对齐。
- 评分标准分为过程分和结果分。
- 考后根据难度（P 值）、区分度（D 值）给出返修清单和讲评错题清单（只读统计，不自己判分）。

**使用教程**：
1. 在 [360 技能中心页面](https://skillhub.360.com/skills/qizhitang/xiaozhi-teach-exam-designer) 下载 Skill，按通用方法放入 Skills 目录。它属于 `xiaozhi-teach-*` 系列，学科出题、学情分析等由同系列其他 Skill 负责，可按需一并安装。
2. 说明测评类型和范围：
   > 帮我出一份八年级数学第十九章《一次函数》的单元测试，终结性，满分 100 分，90 分钟。
3. 先审核它给出的双向细目表（知识点 × 四级），按班级学情调整配比。
4. 确认后让它生成或改编题目，并输出评分细则。
5. 考后把得分统计交给它，获取返修清单。

---

### 2. exam-paper-generator（make-exam 项目）

**介绍**：工程化程度最高的中文组卷 Skill。固定流程为：确认学段、年级、学科、分值、题型 → 输出组卷方案 → **等待确认** → 生成试卷 → 归一化和校验 → 渲染。自带脚本：
- `validate_plan.py`：检查题量、分值和总分是否一致
- `normalize_paper.py`：统一试卷结构
- `validate_paper.py`：校验试卷结构
- `render_html.py`：用 Jinja2 模板渲染教师版（含答案、解析、知识点）或学生版（题目和作答区）

**使用教程**：
1. 下载并安装依赖：
   ```powershell
   git clone https://github.com/susirial/solo_com_gen_exam.git
   Copy-Item solo_com_gen_exam\exam-paper-generator $HOME\.claude\skills\ -Recurse
   pip install jinja2
   ```
2. 在 AI 对话中说：
   > 出一份小学五年级数学期末试卷，满分 100 分，含选择、填空、计算、应用题。
3. 检查它输出的组卷方案（题型、题量、分值），确认或修改。
4. 确认后它会生成试卷并调用脚本校验。也可以手动运行：
   ```powershell
   python scripts/validate_plan.py plan.json
   python scripts/normalize_paper.py paper.json -o paper.normalized.json
   python scripts/validate_paper.py paper.normalized.json
   python scripts/render_html.py paper.normalized.json --variant teacher -o teacher.html
   python scripts/render_html.py paper.normalized.json --variant student -o student.html
   ```
5. 用浏览器打开 HTML，打印或另存为 PDF。

---

### 3. exam-generator（中国中小学试卷生成器）

**介绍**：覆盖小学和初中的语文、数学、英语，以及初中的物理、化学、生物、历史、地理、政治。题型包括选择、填空、判断、简答、计算、作文。出题后联网搜索标准答案交叉验证，并标注置信度：多源一致为高、单源为中、需人工确认为低。在 Skills Directory 的安全扫描中评分为 A。

**使用教程**：
1. 在 [Skills Directory 页面](https://www.skillsdirectory.com/skills/whyzsm-exam-generator) 安装，会装到当前项目的 `.claude/skills`。
2. 确保 AI 工具可以联网搜索（验证答案时需要）。
3. 按以下格式提需求：
   > 帮我出一套初一数学试卷：知识点为有理数运算，5 道选择、5 道填空、2 道计算，中等难度，60 分钟。
4. 重点复核标为"中"或"低"置信度的题目。

---

### 4. teacher-kit（TeacherKit AI 备课助手）

**介绍**：五合一备课工具（教案、试题、课程大纲、课件大纲、说课稿），MIT 协议。能根据"三年级""初二"等表述识别学段，并按新课标核心素养写目标。出题时默认 5 道题，每题标注题型和难度星级，附答案、解析、考查知识点汇总表。认知层级控制较弱，适合轻量使用。

**使用教程**：
1. 安装：
   ```powershell
   git clone https://github.com/dongsheng123132/teacher-kit.git
   New-Item -ItemType Directory -Force $HOME\.claude\skills\teacher-kit
   Copy-Item teacher-kit\SKILL.md $HOME\.claude\skills\teacher-kit\
   ```
2. 触发语中带"出题""试卷"即可：
   > 给初二物理《压强》出 10 道题，选择 6 道、简答 4 道，难度中等。
3. 如需同时备课，可先让它写教案，再基于教案出配套练习。

---

### 5. gaokao-expert（高考命题专家）

**介绍**：基于"一核四层四翼"评价体系的高考命题和评审助手。给出命题"四要四不要"（要真实情境、要考素养、要价值引领、要科学规范；不要偏怪题、不要照搬教材、不要套路、不要价值偏差），以及评审"七个维度"（知识点覆盖、能力层级、情境设计、难度、创新性、育人价值、科学规范）。作者说明不用于中考和日常作业命题。

**使用教程**：
1. 从 [staruhub/ClaudeSkills](https://github.com/staruhub/ClaudeSkills) 克隆，把 `lab/Geek-skills-gaokao-expert/` 整个目录复制到 Skills 目录（包含 `references/`）。
2. 出题：
   > 以新能源汽车电池回收为情境，出一道高考化学非选择题，含评分标准。
3. 审题：粘贴已有高三模拟卷，说"按七个维度评审这份试卷"。
4. 命题趋势类问题会联网搜索当年信息，需开启联网。

---

### 6. 智能组卷出题（扣子平台）

**介绍**：扣子（Coze）平台上的组卷技能，按科目、知识点、难度、题型生成试卷，支持单元测、月考、期中期末、模拟考，一次输出试卷正文、答题卡、参考答案和评分标准。

**使用教程**：
1. 打开 [技能页面](https://xiaping.coze.com/skill/3e125d51-dbbc-4b10-9d0d-dc5f14fd93a2)，登录扣子账号后添加到自己的智能体或直接对话使用。
2. 输入科目、年级、知识点、难度和题型要求。
3. 该技能只在扣子平台内运行，不能直接装到 Claude Code 或 Cursor。

---

### 7. lecture-builder（讲义制作）

**介绍**：适合**已有题库**的中学老师。把"知识点文档 + 题目文档（+ 解析版）"合成学生版和教师版两份 Word 讲义：学生版每题后留答题区，教师版附【答案】【详解】。原图、原公式、原表格完全保留，排版为 A4、1.5 倍行距、黑体标题、宋体正文，带目录和页码。

**使用教程**：
1. 安装：把仓库放到 `C:\Users\<用户名>\.claude\skills\lecture-builder\`。需要 Python；Word 可选（用于固定目录和页码，只有 WPS 时打开后按 F9 更新域）。
2. 准备 `.docx` 文件：知识点文档（必需）、题目文档（必需）、题目解析版（可选，没有则只出学生版）。
3. 把文件交给 AI，说：
   > 用这份知识点和题目做学生版和教师版讲义。
4. 也可手动运行：
   ```powershell
   python scripts/extract_outline.py "知识点.docx" > kp.txt
   python scripts/extract_outline.py "题目.docx" > q.txt
   # 参照 references/example_config.json 编写 config.json
   python scripts/lecture_engine.py --config config.json --open
   ```

---

### 8. ExamLoop

**介绍**：期末复习工具，四个功能：资料速通（上传 PPT/PDF 提取考点和答题模板）、出题练习（按难度出题并自动批改）、解题讲解、模拟出卷（生成 HTML 试卷）。面向学生自学，老师也可以用来从课件快速提取考点并出题。

**使用教程**：
1. 安装（Windows 推荐用 npx）：
   ```powershell
   npx skills add munyoung-ovo/ExamLoop
   ```
2. 在 Claude Code 中输入 `/examloop 速通`，或加载后直接说触发词：`速通`、`出题`、`解题`、`出卷`。
3. 典型用法：先上传课件说"速通"，再说"出题，第三章，中等难度 10 道"，最后说"出卷"。

---

### 9. teaching-exam-skills（初中数学，繁体）

**介绍**：初中数学专项技能集，题目按修订版 Bloom 层级设计：
- `jh-math-exam`：出题模式产出题目卷、答案卷、双向细目表三份 Word；审题模式审核已有试卷并给出层级统计和偏差提示。
- `jh-math-context-questions`：结合生活情境出非选择题，Word 中公式用 OMML。
- `jh-math-geometry`：生成三角形、四边形、圆、坐标系、立体图等几何 SVG，可插入 Word/PPT。
- `teaching-minigames`：把知识点做成小游戏 HTML 和二维码。

**使用教程**：
1. 安装：
   ```powershell
   git clone https://github.com/mathruffian-dot/teaching-exam-skills.git
   Copy-Item teaching-exam-skills\skills\* $HOME\.claude\skills\ -Recurse
   ```
2. 几何配图需要 Python；发布小游戏到 GitHub Pages 需要自备 GitHub Token。
3. `jh-math-context-questions` 里写死了作者本机的生图脚本路径，不需要配图可忽略，或改成自己的路径。
4. 出题时可要求用简体输出：
   > 用简体中文出一份八年级下册数学期中试卷，含双向细目表和几何配图。
5. 审题时上传试卷 Word 或图片，说"审核这份试卷"。

---

### 10. tw-edu-skills（台湾 K-12，繁体）

**介绍**：19 个教学技能，基于台湾 108 课纲。与出题相关的有：
- `tw-edu-exam-generator`：素养导向试题，含阅读素材
- `tw-edu-worksheet-creator`：学习单
- `tw-edu-rubric-designer`：评量规准
- `tw-edu-formative-assessment`：出口票、提问策略
- `tw-edu-anti-ai-assessment`：防 AI 代写的评量设计

**使用教程**：
1. 安装全部或单个：
   ```powershell
   npx skills add FW1201/tw-edu-skills --all -a claude-code
   npx skills add FW1201/tw-edu-skills tw-edu-exam-generator -a claude-code
   npx skills list -a claude-code
   ```
2. 直接说"设计一份试卷""做一份学习单"。
3. 用于大陆教学时，在要求中说明"按人教版教材和 2022 版课标"，并要求简体输出。

---

### 11. k12-teacher-skills（Anthropic 官方）

**介绍**：Claude for Teachers 内置技能的开源版本，由 Anthropic 与 Learning Commons 合作开发，附评测框架。包含 4 个技能，与出题最相关的是 `k12-check-for-understanding`：针对一条数学课标生成 1–3 题的课堂小测，干扰项取自有文献记录的学生误区，并附教师指南，说明学生选了每个选项之后下一步该怎么教。另外 3 个是教案生成、分层教学和备课辅助。

**使用教程**：
1. 克隆 [anthropics/k12-teacher-skills](https://github.com/anthropics/k12-teacher-skills)，把需要的技能目录复制到 Skills 目录。
2. 这些技能默认调用 Learning Commons 知识图谱（美国各州课标），没有该连接时，需要在提示中自行给出课标内容，或修改 `SKILL.md` 去掉相关步骤。
3. 使用：
   > 针对"分数的大小比较"出 3 道课堂小测题，干扰项要对应学生常见错误，并告诉我选错后该怎么补救。

---

### 12. Quiz Generator（SkillMedev）

**介绍**：方法论最清晰的通用出题 Skill。流程：
1. 收集输入：目标、年级、用途、题量和时长、已知误区、形式限制。
2. 出题前先声明 Bloom 分布。如果全是记忆题必须重新平衡；单元测试中记忆和理解层得分不超过 50%。
3. 干扰项来自误区。
4. 答案附理由，并说明每个干扰项对应的误区。

交付物包括按层级分组的题目、汇总表（题号、层级、题型、分值），以及分开的学生版和教师版。

**使用教程**：
1. 克隆 [SkillMedev/skills](https://github.com/SkillMedev/skills)，复制 `skills/quiz-generator/` 到 Skills 目录；也可以在 [skillme.dev](https://skillme.dev/skill/quiz-generator) 加载。
2. 用中文提需求时注明"用中文输出"：
   > 用中文给初三化学《酸和碱》出 10 题单元测验，学生常见误区是"pH 越大酸性越强"。
3. 也可用于审题："检查这些选择题的质量"。

---

### 13. quiz-generator（pm-claude-skills）

**介绍**：通用出题 Skill。每题标注"难度 · Bloom 层级"，选择题为 4 个选项，3 个干扰项都要合理，答案附一行解析。规定不得留空题，信息不全时也要先出完整版本并标注假设范围。仓库同时提供 Cursor 规则版本（`.mdc`）。

**使用教程**：
1. Claude Code：复制 `skills/quiz-generator/` 到 Skills 目录。
2. Cursor：复制 `exports/cursor/pm-education/quiz-generator/quiz-generator.mdc` 到项目 `.cursor/rules/`。
3. 使用：
   > 出一份初一生物《细胞》测验：8 道选择、2 道简答，难度由易到难。

---

### 14. Assessment/Quiz/Test Generator

**介绍**：K-12 完整测评生成器。流程：收集要求（学科、年级、主题、题型、DOK 层级）→ 联网查询课标和核心概念 → 按 DOK 分布出题 → 答案和评分量规 → 排版（分值、时长）→ 可选生成 B 卷防抄袭 → 教师说明（课标覆盖、常见误区、分层建议）。

**使用教程**：
1. 在 [Claude SkillHub 页面](https://claudeskillhub.com/skills/assessment-quiz-test-generator) 下载并放入 Skills 目录。
2. 需要开启联网。
3. 使用：
   > 出一份初二物理《浮力》测试，DOK 1–3，含评分量规，同时生成 A、B 两套卷。
4. 它默认按美国课标，使用时说明"按中国人教版初中物理课标"。

---

### 15. AI Quiz & Worksheet

**介绍**：可在 ChatGPT、Claude、Gemini 中使用的出题 Skill。每题标 DOK 1–4，每个错误选项写一句"学生为什么会选它"，简答题附评分指南。支持出口票（1–3 题检测本课目标），以及面向英语学习者、特殊需求学生和资优生的分层版本。

**使用教程**：
1. 在 [AI Agents Library 页面](https://www.aiagentslibrary.com/skills/ai-quiz-worksheet/) 下载 `SKILL.md`。
2. Claude Code 或 Cursor 放入 Skills 目录；ChatGPT 或 Gemini 可以把内容粘贴到自定义指令或 Gem 中。
3. 使用：
   > 做一份小学四年级《小数加减法》练习单，带作答格子，主要为 DOK 2，加两道 DOK 3 拓展题。

---

### 16. bloom-taxonomy-quiz-builder

**介绍**：基于材料出题。读入课文或文章，先列出可考主题和理由，再询问主题、语气、题型、年级，然后每个 Bloom 层级出一题，每题经老师确认后再出下一题，最后导出 JSON，可导入题库或学习平台。

**使用教程**：
1. 下载仓库中的 `bloom-taxonomy-quiz-builder.skill`，在 Claude.ai 的设置 → Skills → Upload Skill 上传；Claude Code 则复制 `SKILL.md` 到 Skills 目录。
2. 上传或粘贴一篇课文，说"根据这篇材料出一组阅读理解题"。
3. 逐题确认或修改，最后导出 JSON。

---

### 17. Teacher worksheet 命令

**介绍**：分层练习单生成命令，每份分三层（待提高 / 达标 / 拓展），层内由易到难，附分步答案。按学科给出格式：数学题附图示和例题，阅读理解题覆盖 Bloom 五个层级，词汇题包括词库、填空、配对和近反义词。

**使用教程**：
1. 克隆 [awesome-claude-cowork-plugins](https://github.com/alexclowe/awesome-claude-cowork-plugins)，在 Claude Code 中安装 `teacher` 插件，或把 `teacher/commands/worksheet.md` 复制到 `.claude/commands/`。
2. 在 Claude Code 中输入 `/worksheet`，再描述需求：
   > 三年级数学，两位数乘一位数，每层 8 题。

---

### 18. education-agent-skills

**介绍**：165 个循证教育技能，分 20 个领域，CC BY-SA 4.0 协议，只收录有实证支持的方法。与出题相关的有：
- `assessment-validity-checker`：从效度、信度、真实性三方面检查试卷，例如发现"阅读理解题实际在考写作"。
- `assessment-design-orchestrator`：根据评价目的推荐评价方案。
- `formative-assessment-technique-selector`：按课堂时机选择形成性评价方式。
- 记忆科学类技能（提取练习、间隔、交错）：用于设计复习题组。

**使用教程**：
1. 克隆 [GarethManning/education-agent-skills](https://github.com/GarethManning/education-agent-skills)，把需要的技能目录（如 `skills/curriculum-assessment/assessment-validity-checker/`）复制到 Skills 目录。不建议一次装 165 个。
2. 适合在出卷后审卷：
   > 用效度检查器审一下这份试卷，指出哪些题测的不是它声称要测的能力。

---

### 19. math-worksheets

**介绍**：数学练习卷生成器，输出三份 PDF：学生练习卷、分步答案、知识点小结。用 LaTeX + TikZ 排版，用 tectonic 编译，无需安装完整 TeX。**关键机制**：编译前必须写验证 JSON，用 SymPy 逐题校验（解方程、因式分解、展开、求值、求零点等）；校验失败不允许生成 PDF；作图题和证明题标为 `manual` 交人工检查。

**使用教程**：
1. 从 [ClawHub](https://clawhub.ai/trondw/skills/math-worksheets) 获取 Skill 并放入 Skills 目录。
2. 安装依赖：
   ```powershell
   pip install sympy
   # 安装 tectonic：https://tectonic-typesetting.github.io
   ```
3. 使用：
   > 出一份初三《二次函数》练习卷，10 题，由易到难，含坐标系作图题。
4. 验证 JSON 示例（AI 会自动写）：
   ```json
   {"id": 1, "type": "solve", "expr": "x**2 - 5*x + 6", "expected": [2, 3]}
   ```
5. 中文 PDF 需要在 LaTeX 中加入中文支持（如 `ctex` 宏包），可在提示中要求。

---

### 20. math-skill

**介绍**：严谨解题 Skill，按"梳理题目 → 选择方法 → 分步推导 → 独立验证"作答。自带 `math_verify.py`（表达式等价、导数、积分、方程解、极限、反例）、`math_visualize.py`（作图）、拍照识题辅助脚本。支持 `exam`、`tutor`、`worksheet`、`diagnostic`、`primary-school` 等模式。

**使用教程**：
1. 安装：
   ```powershell
   git clone https://github.com/googlarz/math-skill.git
   Copy-Item math-skill $HOME\.claude\skills\ -Recurse
   pip install sympy numpy matplotlib
   ```
2. 出题时指定模式：
   > 用 worksheet 模式出 8 道初二一元二次方程练习，并验证每题答案。
3. 也可以用于核对别的 Skill 生成的答案：粘贴题目和答案，要求"逐题验证"。

---

### 21. reading-comprehension-text-adapter

**介绍**：英语阅读题设计工具。用脚本按句长、高频词覆盖率、Flesch 指数估算文本 CEFR 等级，然后通过拆长句、替换或注释生词、解释习语等方法改写到目标难度。题目分预测、主旨、细节、推断、词义猜测、个人回应几类，并用脚本检查题型搭配，例如是否缺主旨题、B1 以上是否缺推断题、判断题答案是否一边倒。

**使用教程**：
1. 从 [Vector Agentic Skills 页面](https://agenticskills.vector-ai-lab.com/skills/reading-comprehension-text-adapter/) 获取并放入 Skills 目录。
2. 流程：
   ```powershell
   python scripts/text_level.py original.txt --target B1
   # AI 改写后再次运行，直到显示 OK
   python scripts/question_mix.py questions.txt --level B1 --key T F T NG
   ```
3. 使用：
   > 把这篇文章改写成适合初二学生的难度（约 A2+），出 5 道阅读题，答案注明所在段落。

---

### 22. cefr-reading-coach

**介绍**：英语阅读练习教练。抓取真实文章，改写到 12 个 CEFR 子级（A1.1–C2.2）中的指定级别，保留原文结构；每次练习记录学生的薄弱点，下次针对性改写；生词附音标和朗读音频（基于 edge-tts）。偏个人练习，老师可以借用"改写真实文章"的方式准备阅读材料。

**使用教程**：
1. 克隆 [ystyleb/cefr-reading-coach](https://github.com/ystyleb/cefr-reading-coach) 并放入 Skills 目录；需要音频时 `pip install edge-tts`。
2. 首次运行会测定水平，之后每天说"开始阅读练习"即可。

---

### 23. docx / pdf / xlsx / pptx（Anthropic 官方文档 Skills）

**介绍**：Claude 内部使用的文档处理技能，源码公开（但不是开源协议）。用途：`docx` 生成或编辑 Word 试卷，生成后转图片自查版面；`pdf` 生成或读取 PDF 试卷；`xlsx` 输出题库表、双向细目表、成绩表；`pptx` 生成讲评课件。和上面任意出题 Skill 搭配使用。

**使用教程**：
1. Claude Code 中执行：
   ```text
   /plugin marketplace add anthropics/skills
   /plugin install document-skills@anthropic-agent-skills
   ```
2. 其他工具：克隆 [anthropics/skills](https://github.com/anthropics/skills)，复制 `skills/docx` 等目录到 Skills 目录。依赖 pandoc、LibreOffice、Poppler 等，详见各 `SKILL.md`。
3. 使用：
   > 把刚才的试卷导出为 Word，学生版和教师版各一份，A4 排版；双向细目表导出为 Excel。

---

## 四、推荐搭配

| 场景 | 推荐组合 |
|---|---|
| 大陆中小学单元测试、期中期末 | 测评设计师（细目表）+ exam-paper-generator（流程和双版本）+ docx |
| 数学 | jh-math-exam 或 math-worksheets + math-skill（答案验证）+ jh-math-geometry（配图） |
| 英语阅读 | reading-comprehension-text-adapter + docx |
| 课堂小测 | k12-check-for-understanding + AI Quiz & Worksheet（出口票） |
| 已有题库排讲义 | lecture-builder |
| 审卷 | gaokao-expert（高中）+ assessment-validity-checker |

## 五、注意事项

1. 多数仓库是 2026 年的个人项目，关注度低，建议先试用再决定是否长期使用。
2. 英文 Skill 依据美国课标，繁体 Skill 依据台湾 108 课纲，用于大陆教学需要在提示中指定教材版本和课标。
3. 即使有脚本校验，作图题、开放题、阅读材料的价值导向和版权仍需教师人工审核。
