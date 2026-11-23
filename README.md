# The World Today — Monday 23 November 2026

[![news-image-20261123](https://make.fun/badge/news-image-20261123.svg)](https://make.fun/bounty/news-image-20261123)
[![rank](https://make.fun/badge/news-image-20261123/gom92/-makefun-news-image-20261123/rank.svg)](https://make.fun/bounty/news-image-20261123)
<!-- Third badge: take the remaining badge URL from the competition's
     readme_template (GET https://make.fun/api/competitions/news-image-20261123/requirements)
     and add it here before submitting. -->

A newspaper front page that sums up the world's news of Monday 23 November
2026 in one image, for the make.fun bounty
**"Sum up 23 November's world news in one image"** ($100 in USDC, 50 places:
1st $20, 2nd $12, 3rd $6, 4th–10th $2, 11th–50th $1.20).

**参赛链接（已在官网核实）：https://make.fun/bounty/news-image-20261123**
（奖金 $100，截止 2026-11-25 00:00 UTC；每天最多提交 10 次，总共最多 20 次；
最后一次提交为最终参赛作品。）

> **状态：作品已完成，尚未提交。** 注册 make.fun 账号、绑定 GitHub、提交
> 这几步必须由用户本人做（见下面的「投稿流程」）。本文件夹里没有任何账号、
> 密钥或已提交的记录。

## 这张图里有什么

头版（1024×1024 PNG，605 KiB，未超 1 MiB 上限）：

- **头条：感恩节风暴袭击美国东海岸**——强降雨、50 mph 阵风、从卡罗莱纳到
  新英格兰的沿海洪水；数百万人出行，达美航空系统故障加剧延误。
  （插图：水彩风格的暴风雨海岸公路）
- **民主党拿下历史性众议院多数**——至少 258 席，自 1992 年以来最大；
  计划为 2028 年初选举办 12 场辩论，首场在 6 月。
  （插图：黄昏中的美国国会大厦）
- **数字栏**：3 枚被波兰确认为俄罗斯 Kh-101 导弹的物体；$450m 斯库巴尔
  创纪录的大都会合同；50 mph 风暴峰值阵风。
- **六条简讯**：波兰确认导弹残骸；法官叫停陆军在爱荷华州引爆不稳定炸药
  （铅叠氮化物）的计划；华尔街在 AI 抛售后企稳、SEC 调查英伟达账目；
  斯库巴尔 $450m 合同；COP31 气候谈判无果而终；美国失去麻疹消除地位，
  弗吉尼亚报告 2026 年首例麻疹死亡。

新闻来源（2026-11-23 当天核实）：美联社/纽约时报/卫报等经由新闻搜索
核实的当日报道（感恩节风暴、众议院多数席位、波兰导弹、爱荷华引爆、
股市反弹、斯库巴尔合同、COP31、麻疹）。图片中所有文字均由 Pillow 绘制
（AI 生图工具写不好文字），两张插图为 AI 生成、不含任何文字。

## 怎么运行

```bash
python3 main.py                  # 写出 /output/entry.png
MAKEFUN_OUTPUT_DIR=out python3 main.py   # 写到别的目录
```

`main.py` 只用 Python 标准库：把本仓库的 `entry.png` 原样复制到
`/output/entry.png`，不联网，每次运行写出完全相同的字节（已实测两次
运行的 SHA-256 一致）。

重新生成头版（需要 Pillow）：

```bash
python3 tools/render_frontpage.py   # 从 assets/ 插图重新绘制 entry.png
```

文件：

| 文件 | 说明 |
|---|---|
| `main.py` | 参赛程序（标准库 only，复制图片到 /output/entry.png） |
| `entry.png` | 参赛图片，1024×1024 PNG，619,954 字节 |
| `tools/render_frontpage.py` | 用 Pillow 绘制头版的脚本 |
| `assets/storm-lead.png` | AI 生成的风暴插图 |
| `assets/capitol.png` | AI 生成的国会大厦插图 |
| `LICENSE` | MIT（OSI 认可） |

## 投稿流程（完整步骤，用户本人操作）

### 第 1 步：注册 make.fun 账号

1. 打开 https://make.fun ，点注册/登录。
2. 登录方式（以网站当时提供的为准，可先查
   `GET https://make.fun/api/auth/methods` 看有哪些）：
   **Solana 钱包（密钥对）、GitHub、Google、Apple、Discord**。
   推荐用 **GitHub 登录**（你已准备好 GitHub），账号和钱包一次搞定。
3. 账号即钱包：Solana 密钥对既是登录账号，也是领奖钱包。
   密钥文件务必自己保管（权限 600），**绝不要发给任何人、不要贴到
   聊天记录或仓库里**；只有签名会离开你的电脑。
4. 领奖需要：获奖后在领奖窗口内（至少 7 天）把 USDC 领到自己的
   Solana 钱包；钱包里要留一点 SOL 付网络手续费。

### 第 2 步：绑定 GitHub

1. 在 make.fun 网站登录后，进个人资料（Profile）的 Identity / 关联账号
   一栏，点绑定 GitHub，按页面提示完成。
2. **GitHub 会要求哪些授权权限：** 绑定时 GitHub 会弹出 OAuth 授权页，
   上面逐条列出 make.fun 请求的权限——**以当时页面上显示的为准，
   点同意前逐条看一遍**。这里不列一份猜出来的清单。
   可核实的一点是：make.fun 官方文档中对参赛仓库的检查全部是
   **只读公开仓库**（核对提交的 commit 是否存在、LICENSE 是否为 OSI
   认可、README 是否符合模板、仓库 About/话题是否符合要求），
   不需要改你的仓库。
3. 如果仓库的 GitHub 所有者与 make.fun 账号绑定的 GitHub 登录名不同，
   需要在提交的 commit 里加一个 `.makefun/owner.json`，内容为
   `{"wallet": "<你的 Solana 钱包地址>"}`，用来证明仓库是你的。
   （账号本身就是 GitHub 登录时，一般不需要这个文件。）

### 第 3 步：准备公开仓库

1. 在 GitHub 新建一个**公开**仓库（比赛开始后创建；本场 2026-11-23
   00:00 UTC 开赛），把本文件夹的全部内容推上去：
   `main.py`、`entry.png`、`tools/`、`assets/`、`LICENSE`、`README.md`。
2. **README 模板**：参赛仓库的 README 必须用本场比赛
   `how_to_submit.readme_template` 的格式（在
   `GET https://make.fun/api/competitions/news-image-20261123/requirements`
   里取），包含本场三个徽章，并填好五个占位符再提交：
   - `{owner}`：你的 GitHub 用户名
   - `{repo}`：仓库名
   - `{description}`：一两句说明（一句话介绍这个作品是干什么的）
   - `{run}`：本地运行命令（`python3 main.py`）
   - `{referral_code}`：你账号的推荐码（`GET /api/me/referrals` 里取；
     填上后 README 底部的链接就是你的推荐链接）
   本文件夹的 README.md 已按该格式写好，徽章处留了 `{owner}`/`{repo}`
   占位符，提交前替换掉。
3. **仓库 About**：按 `how_to_submit.repo_about` 设置（同样在
   requirements 里取），网站填 make.fun 相关地址，话题（topics）里
   必须有 `makefun`（建议再加 `ai-agents`、`bounties`）。命令行：
   ```bash
   gh repo edit {owner}/{repo} --description "{summary}" --homepage "{homepage}" --add-topic makefun --add-topic ai-agents --add-topic bounties
   ```
   （没有 `gh` 可用 GitHub API 的 PATCH/PUT 改 description、homepage 和 topics。）
4. **提交前先 push**：把要参赛的 commit 推到 GitHub 上，确认
   `https://github.com/{owner}/{repo}/commit/{sha}` 能打开，
   再提交。记下完整的 40 位 commit SHA。
5. LICENSE 必须是 OSI 认可的（本文件夹已放 MIT）。

### 第 4 步：打包 transcripts（会话记录）

1. 先在 make.fun 网站下载官方 kit（Node.js 22），解压后进目录。
2. 登录 kit：
   ```bash
   node cli/makefun.mjs login --origin https://make.fun
   ```
   按提示用你的账号完成登录（登录的是你本人的账号，不要用别人的密钥对）。
3. 打包本次制作的会话记录：
   ```bash
   node cli/makefun.mjs bundle
   ```
   bundle 会收集写这个作品的 agent 会话（包括子 agent 的会话），并自动
   抹掉里面的邮箱、家庭目录、用户名和密钥等信息。打包前先用
   `bundle --dry-run` 看一遍它要收哪些会话。
   注意：**不要事后手写、编造会话记录**；只有真实的会话记录才有效。
   交上去的记录会用于核对代码是不是你自己的 agent 写的。
4. 得到 `transcripts.tar.gz`（或按 kit 提示的 loose 文件形式）。

### 第 5 步：提交

```bash
node cli/makefun.mjs submit \
  --competition news-image-20261123 \
  --repo-url https://github.com/{owner}/{repo} \
  --commit {40位commit SHA} \
  --bundle transcripts.tar.gz \
  --keypair ~/.makefun/keypairs/https_make.fun.json
```

- 提交后看返回结果：通过会给一个 submission id；被拒会说明哪项检查
  没过，按提示修好再提交（每天最多 10 次，总共最多 20 次）。
- 截止时间：**2026-11-25 00:00 UTC**，以最后一次提交为准。

### 第 6 步：等结果、领奖

1. AI 裁判两两比较图片，按胜率排名；前 50 名分 $100。
2. 结果公布后，在领奖窗口内（至少 7 天）到 make.fun 网站上操作，
   把 USDC 领到自己的 Solana 钱包（钱包里留一点 SOL 付手续费）。

## 备注

- 本作品由 agent 制作，图片插图为 AI 生成、文字由程序绘制；
  未注册任何账号、未提交、未花钱。
- 收入记录：目前 $0（未参赛）。参赛并获奖后按实际到账金额记录。
