# Org 门面 README — 引言段落版本记录

`profile/README.md` 里**标题 + tagline 下面那一段话**在各次提交中的表述。方便回溯「我们原来怎么说的」。

---

## 当前版本（最新）

**Commit:** `c97b45a` — docs(profile): restore local copy (skills, extensions, ClawHub, Plugin SDK)

> OpenClawHQ is an open community building skills, extensions, and developer tools for [OpenClaw](https://github.com/openclaw/openclaw) — the personal AI assistant you run on your own devices. We exist because one team can't cover every use case. The path forward is distributed: community-driven skills, shared tooling, open knowledge.

---

## 版本 1 — 初版（init）

**Commit:** `d8830a7` — feat: init org profile and community defaults

> OpenClawHQ is an open community building plugins, connectors, and tools for the proactive AI ecosystem. We exist because one team — no matter how strong — can't cover every use case. With 500+ PRs flowing through OpenClaw daily, the path forward isn't more people. It's a better architecture: distributed, plugin-native, community-driven.

---

## 版本 2 — 改成 skill-native

**Commit:** `7b1dbda` — Update README.md

> OpenClawHQ is an open community building plugins, connectors, and tools for the proactive AI ecosystem. We exist because one team — no matter how strong — can't cover every use case. With 500+ PRs flowing through OpenClaw daily, the path forward isn't more people. Distributed, skill-native, community-driven It's a better architecture.

（注意：这里 "community-driven" 和 "It's" 之间少了一个冒号，下一版修了。）

---

## 版本 3 — 同上 + bullet 加「Skills & Packages」

**Commit:** `e2218d8` — Update README.md

引言段落与版本 2 相同：

> OpenClawHQ is an open community building plugins, connectors, and tools for the proactive AI ecosystem. We exist because one team — no matter how strong — can't cover every use case. With 500+ PRs flowing through OpenClaw daily, the path forward isn't more people. Distributed, skill-native, community-driven It's a better architecture.

（本节只记引言；当次提交里「What gets built here」的 bullet 改成了 Plugins & **Skills & Packages** & Extensions。）

---

## 版本 4 — 冲突解决时加冒号

**Commit:** `81fd390` — docs(profile): resolve merge conflict, keep org copy

> OpenClawHQ is an open community building plugins, connectors, and tools for the proactive AI ecosystem. We exist because one team — no matter how strong — can't cover every use case. With 500+ PRs flowing through OpenClaw daily, the path forward isn't more people. Distributed, skill-native, community-driven**:** it's a better architecture.

（仅把 "It's" 前的缺冒号补成 "community-driven: it's"。）

---

## 小结（仅引言一句的演变）

| 版本 | 核心表述 |
|------|----------|
| 1 初版 | plugins, connectors, and tools / proactive AI ecosystem / 500+ PRs / distributed, **plugin-native**, community-driven |
| 2–4 | 同上，但改为 **skill-native**；版本 4 补了冒号 |
| 5 当前 | **skills, extensions, and developer tools** / **OpenClaw** 链接 / **personal AI assistant, your own devices** / **community-driven skills, shared tooling, open knowledge**（不再提 500+ PRs） |

如需恢复某版引言，可从本文件复制对应段落到 `profile/README.md` 使用。
