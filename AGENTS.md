# AGENTS.md — 给 AI Agent 的工作指引

本文件面向自动化 AI Agent。人类读者请看 [README.md](README.md)。

## 这个仓库是什么

`meddev-reg-path-checker` 是一个**行业接入域配置包**，不是可运行的 SDK。核心资产是四个 JSON 文件。域 ID `meddev`，当前状态 RESERVED（样板域）。

## 可用的工作命令

```bash
cat domain.manifest.json   # 本域声明
cat gate-map.json           # 阻断规则
cat checker.io.json         # MCP 核验器契约
```

## 约定（Do）

- 修改属性或红线时，**必须同步** `domain.manifest.json` 与 `gate-map.json`。
- 认领后填注 `operator` 与 `checker_endpoint`。

## 禁止（Don't）

- 不要改动 `LICENSE` 的版权主体（© 2026 SynomosAI）。
- 不要输出「可上市 / 可销售 / 已合规」等放行结论——分类界定与注册审批权在药监部门。
- 不要删除 `privacy.json` 或其必填字段。
- 不要在仓库内提交任何密钥或真实运营方数据。

## 边界

本仓专注**医疗器械 · 注册与备案路径**域；不覆盖产品临床评价、生产质量体系核查、进口注册等子域的专业判定。
