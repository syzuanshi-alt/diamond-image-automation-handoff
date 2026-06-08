# 钻石自动化生图项目 GitHub 接力版

这是一个面向美国用户的钻石电商批量生图工作流项目。这个文件夹是 GitHub 接力版，只保存可维护的工作流、Obsidian 知识库、提示词干跑样本和项目状态，不保存大量图片、视频、压缩包或临时输出。

## 目录结构

- `Obsidian-Diamond-Image-KB/`：核心 Obsidian 知识库，所有业务规则、产品规则、人物场景框架、自动化模板都在这里。
- `prompt-runs/`：提示词干跑结果，当前有效参考版本是 `2026-06-02-scale-50-v6`。
- `PROJECT_STATE.md`：当前项目状态，新的 Codex 必须先读。
- `AGENTS.md`：给 Codex 的项目级执行指令。
- `MIGRATION_GUIDE.md`：新电脑接力操作步骤。

## 新电脑打开方式

1. 在新电脑上从 GitHub `git clone` 这个仓库。
2. 用 Codex 打开本项目根目录。
3. 用 Obsidian 打开 `Obsidian-Diamond-Image-KB/`。
4. 让新 Codex 先读取：
   - `AGENTS.md`
   - `PROJECT_STATE.md`
   - `Obsidian-Diamond-Image-KB/00-总控/新电脑接力入口.md`
5. 继续推进前，先确认当前有效版本是 `prompt-runs/2026-06-02-scale-50-v6`。

## 当前阶段

当前处于第一阶段：图片素材关卡建设。

已完成：
- 独立 Obsidian 知识库。
- 产品 DNA 一致性规则。
- 彩钻比例规则，10 套最多 1 套。
- 人物、场景、动作、镜头框架。
- 50 套提示词干跑 V6。
- 图片自动审核规则草稿。

下一步建议：
- 不要直接上 100 套生图。
- 先用 V6 规则小批量生成 2-5 套图片。
- 根据图片问题反推自动审核规则。
- 再逐步扩到 10 套、50 套、100 套。

## GitHub 使用原则

这个项目包含商业选品逻辑、提示词框架和自动化规则，建议只同步到 private GitHub 仓库。

不要长期把大量生成图片放进 GitHub。图片素材应单独放本地盘、网盘、NAS 或对象存储。GitHub 主要保存知识库、规则、脚本、提示词和项目状态。
