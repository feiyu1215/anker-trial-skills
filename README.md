# anker-trial-skills

安克创新「AI 飞行员试炼」备考 skill 集。**全部为"参考／检查单"类，不替用户下判断、不替用户生成指令**——否则反伤试炼 Prompt 分项。

## 结构（每个子目录 = 一个 skill，Claude Code / WorkBuddy 通用格式）

| skill | 绑定阶段 | 触发 |
|---|---|---|
| `anker-boot-check` | 学习段/轮0 | 开考第一步：官方教学提醒 + 环境验证 + 建文件夹 + 路径声明 |
| `anker-scoring-rubric` | 轮10/11/13 | 整合前、交卷前做评分自检 + "方法复用"一节 |
| `anker-isr-map` | 轮2/5/7/9 | 要框架 / 填 Insight / 填 Strategy / 填 Operation（调时指明哪一段） |
| `anker-read-problem` | 轮1 | 开始读材料前走读题四问 + 秒回验伪 |
| `anker-challenge-triggers` | 轮8(触发)/轮6 | 命中7条件才质疑；轮6 让 AI 反驳我 |
| `anker-coverage-check` | 轮7 | 填 Strategy 时查方案五侧面 + MECE |
| `anker-demo-spec` | 轮0/12 | 定全局约束 / 做 Demo 的无网硬约束 |
| `anker-vague-rewrite` | 轮10 | 整合前虚词清零 |
| `anker-role-brief` | 轮0 | 定全局约束时的角色定义结构 |

## 设计铁律
- skill 输出 = 「该覆盖的清单 / 该问自己的问题 / 该守的约束」→ OK
- skill 输出 = 「替你写好的指令 / 替你做的分析」→ NO
- 每个 skill 的 `description` 写死触发轮次/条件，不写宽触发（不过载）。

## 部署（考场侧）
1. 本仓库 = **9 个 skill + docs/ 两份作战手册**（`完整打法.html` / `答题执行手册.html`），一次 clone 全带走。
2. 考场云桌面激活后：
   ```
   git clone https://github.com/feiyu1215/anker-trial-skills .claude/skills
   ```
   → 9 个 skill 自动识别（可用性 ≠ 激活，按轮调用）；
   → 浏览器 file:// 打开 `docs/答题执行手册.html`（P0–P13 复制+填空）和 `docs/完整打法.html`（时间表+纪律）。
3. 私有库，仓库内不含任何账号凭据。

## 本地预览（备考）
可直接把本目录作为技能源使用；或复制到用户级 `~/.workbuddy/skills/` 让本地 WorkBuddy 识别。
