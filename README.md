# Claude Code 成人角色扮演通用框架

专为 **Claude Code + GitHub** 设计的高遵从性成人角色扮演模板。

适用于：想在 Claude 上进行深度成人角色扮演，但网页版 Chat 端会拦截内容的用户。

## 这个框架解决什么问题？

- 网页版 Claude 会拦截或跳过成人内容
- 角色容易脱离人设、使用模糊词汇、在性爱场景直接跳到第二天
- 长期记忆容易丢失

通过把指令和记忆文件放在 GitHub 仓库，再用 Claude Code 连接，可以显著提高遵从性并绕过部分限制。

## 目录结构说明

| 路径 | 作用 |
|------|------|
| `CLAUDE.md` | 核心系统指令（Claude Code 自动读取） |
| `memory/current_scene.md` | 当前场景实时状态 |
| `memory/timeline.md` | 剧情时间线 |
| `memory/preferences.md` | 用户用词偏好、固定设定 |
| `character/` | 存放角色人设文件（可多个） |
| `rules/` | 分类规则备份 |
| `examples/` | 正确输出示例 |

## 快速开始（小白版）

1. Fork 或下载本仓库
2. 把你的角色人设写入 `character/` 目录
3. 把当前场景和偏好分别写入 `memory/` 对应文件
4. 将整个仓库上传到自己的 GitHub（建议设为 Private）
5. 用 Claude Code 连接该 GitHub 仓库
6. 开始对话

详细操作步骤见下方「完整操作流程」。

## 完整操作流程（推荐收藏）

### 第一步：准备角色文件
- 在 `character/` 里新建你的角色文件（参考里面的模板）
- 在 `memory/preferences.md` 写明你喜欢的直白用词
- 在 `memory/current_scene.md` 写当前场景
- 在 `memory/timeline.md` 写已发生的剧情

### 第二步：上传到 GitHub
1. 登录 GitHub → New repository
2. 建议设为 **Private**
3. 把本框架所有文件上传进去

### 第三步：用 Claude Code 连接
1. 打开 Claude Code
2. 选择从 GitHub 打开项目
3. 粘贴你的仓库地址并授权
4. 连接成功后即可开始角色扮演

### 第四步：开场建议
直接发送：
```
读取 CLAUDE.md 和 memory/ 下所有文件，确认角色与当前场景后继续。
```

## 常见问题

**Q：还是会跳时间怎么办？**  
A：把跳时间的回复发给框架维护者，继续加强 `CLAUDE.md` 里的禁止条款。

**Q：可以同时跑多个角色吗？**  
A：可以，在 `character/` 里放多个文件，并在场景中明确当前由谁发言。

**Q：记忆怎么保持连续？**  
A：重要剧情结束后，让角色帮你更新 `memory/current_scene.md` 和 `timeline.md`。
