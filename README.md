# chatgpt-novel

《外缘战争》长篇小说协作仓库。

## 协作方式

- 网页 ChatGPT：编剧室 / 编辑部。负责讨论世界观、人物、战争、政治与大纲；只有作者明确拍板后才更新正式档案。
- GitHub：唯一事实来源（Single Source of Truth）。
- 本地 GPT / Codex：正文执行器。读取最新设定、大纲和网文 skill，生成草稿、检查连续性并落盘。

详细规范见 [`AGENTS.md`](AGENTS.md)。

## 目录

```text
背景设定&大纲/
  项目设定基线.md
  设定补丁_v0.2.md
  第一卷总纲.md
  01-20章细纲.md
草稿/
正文/
skills/
  chinese-webnovel-skills/   # git submodule
AGENTS.md
```

## 获取完整仓库与 skill

首次克隆：

```bash
git clone --recurse-submodules https://github.com/turtler000/chatgpt-novel.git
cd chatgpt-novel
```

如果已经普通 clone：

```bash
git pull
git submodule update --init --recursive
```

`skills/chinese-webnovel-skills` 直接引用上游：

https://github.com/tance-mang/chinese-webnovel-skills

这样 skill 保持完整，也可以独立升级，不需要把第三方大型知识库手工复制进本仓库。

## 内容优先级

作者最新明确决定 > 最新设定补丁 > 项目设定基线 > 当前卷纲/阶段细纲 > 已确认正文事实 > 通用网文 skill。

通用 skill 负责“怎么写”，不得擅自改变“发生什么”。

## 当前状态

- 项目设定基线 v0.1：已导入。
- 最新人物/灵能/身份隔离设定：记录于 `设定补丁_v0.2.md`。
- 第一卷总纲：已导入。
- 1—20章细纲 v0.2：已导入。
- 正文：暂不导入此前试写版本；该版本已明确判定为过于平铺直叙，不作为正式文本。
