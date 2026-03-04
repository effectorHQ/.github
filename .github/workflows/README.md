# Workflows

本目录下的可复用 workflow 供组织内仓库使用。

## 一键简单测试（Security / Simple checks / Typo / Build）

- **simple-tests.yml** — 在 push/PR 到 `main` 时跑四项：Security Analysis、Simple checks、Typo、Build。
- 其他仓库只需在各自 `.github/workflows/` 里放一份 **simple-tests.yml**（内容与本 repo 中的一致），即会调用本 repo 的下列可复用 workflow。

## 可复用 workflow

| 文件 | 作用 |
|------|------|
| **security-analysis.yml** | 有 `package.json` 时跑 `npm audit`；有 Python 依赖时可选跑 `pip-audit`。 |
| **simple-checks.yml** | 检查未提交 .env 里的敏感信息、校验 `.github` 下 YAML 语法。 |
| **typo.yml** | 用 [crate-ci/typos](https://github.com/crate-ci/typos) 做拼写/typo 检查。 |
| **build.yml** | 有 `package.json` 时跑 `npm ci` + `npm test`；仅 Python 时跑 `pip install` + `pytest`。单 job 超时 5 分钟。 |
| **reusable-skill-lint.yml** | 校验 SKILL.md，供 skill 类仓库调用。 |

## Dependabot

根目录 **.github/dependabot.yml** 已配置：每周为 GitHub Actions 提升级 PR，不占 CI 时间。有 `package.json` 的仓库已各自加 dependabot（npm + github-actions）。

## 已接入 simple-tests 的仓库

- 本 repo（.github）
- skill-lint
- skill-lint-action
- plugin-template
- cookbook
- linear-skill

其他仓库需要时，复制 **simple-tests.yml** 到该仓库的 `.github/workflows/` 即可。
