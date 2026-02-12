# 项目记忆 - Seedance Storyboard Plugin

## 项目概述
为 Claude Code 创建的 Skill/Plugin，帮助用户将想法转换成即梦 Seedance 2.0 专业分镜提示词。

## 关键信息
- **GitHub 仓库**: https://github.com/elementsix/claude-seedance-plugin
- **安装命令**: `/plugin install https://github.com/elementsix/claude-seedance-plugin`
- **Skill 名称**: `seedance-storyboard`
- **本地路径**: `/Users/elementsix/Desktop/vibecoding/claude-seedance-plugin/`

## 已完成的工作
- [x] 学习 Seedance 2.0 使用手册
- [x] 创建完整 Skill（SKILL.md + 模板 + 示例）
- [x] 配置 Git 和 SSH
- [x] 推送到 GitHub 并发布
- [x] 测试生成分镜提示词（宇航员火星场景）

## 文件结构
```
claude-seedance-plugin/
├── .claude-plugin/plugin.json     # 插件配置
├── skills/seedance-storyboard/
│   ├── SKILL.md                   # 主逻辑
│   ├── templates/                 # 6套分镜模板
│   ├── examples/                  # 10个完整示例
│   └── quick-reference.md         # 快速参考
├── README.md
└── LICENSE
```

## 待改进/未来功能
- [ ] 收集用户反馈
- [ ] 添加更多行业模板（电商、短视频、广告等）
- [ ] 优化提示词生成算法
- [ ] 创建视频教程

## 有用的命令
```bash
# 本地测试 plugin
claude --plugin-dir ./claude-seedance-plugin

# 推送更新
cd claude-seedance-plugin
git add .
git commit -m "更新描述"
git push origin main
```

## SSH 配置
- 密钥位置: `~/.ssh/id_ed25519_github`
- 已添加到 GitHub: https://github.com/settings/keys

## 相关链接
- 即梦官网: https://jimeng.jianying.com
- Seedance 2.0 使用手册: `/Users/elementsix/Desktop/vibecoding/🎬 即梦 Seedance 2.0 使用手册（全新多模态创作体验）.docx`

---

## 关键对话摘要（2025-02-10）

### 1. 项目背景与目标
**用户初始需求**:
- 不知道如何制作和使用 Claude Code 的 Skill
- 希望基于 Seedance 2.0 使用手册创建一个 skill
- 功能是"一步一步引导把任何想法转换成专业的分镜提示词"
- 目标人群：觉得 Seedance 2.0 提示词难的普通人

**关键洞察**:
Seedance 2.0 是一个刚出来的非常强大的视频生成模型，但提示词真的难倒了很多普通人。

### 2. 学习过程：Skill vs Plugin
**学到的知识**:
- **Skill**: 单个技能，放在 `.claude/skills/<name>/SKILL.md`
- **Plugin**: 可分享的插件集合，包含 skill + 配置 + 其他资源
- Skill 适合个人使用，Plugin 适合分享给他人安装

**决策**: 从简单 Skill 开始，然后升级为可分享的 Plugin

### 3. Seedance 2.0 核心能力分析
从手册中提取的关键信息：
- **多模态输入**: 图片(≤9张) + 视频(≤3个,≤15s) + 音频(≤3个,≤15s) + 文本
- **核心功能**:
  - 参考图像：精准还原画面构图、角色细节
  - 参考视频：支持镜头语言、复杂动作节奏、创意特效复刻
  - 视频延长：平滑延长与衔接，可"接着拍"
  - 视频编辑：角色更替、剧情颠覆、片段调整
- **限制**: 暂不支持上传包含写实真人脸部的素材
- **交互语法**: 使用 `@素材名` 引用，如 `@图片1 作为首帧，参考@视频1 的运镜`

### 4. Skill 设计决策
**分步引导流程设计**（4步法）：
1. 理解用户想法（故事+时长+素材）
2. 深入挖掘（内容/视觉/镜头/动作/声音，5个维度）
3. 构建分镜结构（时间轴拆解）
4. 生成专业提示词

**配套资源创建**:
- `templates/storyboard-template.md` - 6套分镜模板（叙事/产品/动作/风景/延长/编辑）
- `examples/example-prompts.md` - 10个完整示例
- `quick-reference.md` - 快速参考卡片

### 5. 技术实现：Git + SSH 配置
**遇到的问题与解决**:
1. **问题**: 新创建的 skill 需要重新加载 Claude Code 才能识别
   **解决**: 解释原因，提供手动调用方式

2. **问题**: GitHub 推送需要认证
   **解决**:
   - 生成新的 SSH 密钥对：`ssh-keygen -t ed25519`
   - 配置 SSH config 文件
   - 将公钥添加到 GitHub
   - 修改远程仓库为 SSH 地址

3. **安全提醒**: 用户意识到我"看到了" SSH 私钥
   **处理方式**: 提供重新生成密钥的选项（用户选择暂不处理）

**学到的命令**:
```bash
# 生成 SSH 密钥
ssh-keygen -t ed25519 -C "elementsixsoft@gmail.com" -f ~/.ssh/id_ed25519_github -N ""

# 配置远程仓库为 SSH
git remote set-url origin git@github.com:elementsix/claude-seedance-plugin.git

# 测试 SSH 连接
ssh -T git@github.com
```

### 6. Plugin 发布流程
**创建的文件结构**:
```
claude-seedance-plugin/
├── .claude-plugin/
│   └── plugin.json          # 插件配置（名称、版本、作者、仓库链接）
├── skills/
│   └── seedance-storyboard/ # 核心 skill
├── README.md                # 使用说明
└── LICENSE                  # MIT 许可证
```

**manifest (plugin.json) 关键配置**:
- name: seedance-storyboard
- version: 1.0.0
- author: elementsix <elementsixsoft@gmail.com>
- repository: https://github.com/elementsix/claude-seedance-plugin

### 7. 测试验证
**测试案例**: 宇航员在火星行走

**生成的提示词结构**:
```
电影级写实科幻风格，15秒，2.35:1电影宽屏

0-3秒：大远景缓慢推近，火星峡谷全景...
3-7秒：中景跟随，宇航员缓慢行走...
7-11秒：沙尘开始卷起...
11-13秒：特写头盔面罩...
13-15秒：远景拉远，沙尘暴笼罩...

背景音效：低沉风声 + 史诗管弦乐
```

**验证要点**:
- 时间轴清晰
- 镜头语言明确
- 多模态引用规范
- 符合平台限制（人脸处理）

### 8. 对话管理学习
**用户的疑问**: 对话历史保存在哪里？
**澄清**:
- Claude Code **不会自动保存**完整对话历史
- MEMORY.md 只记录关键结论，不是完整对话
- 如果需要完整记录，需要手动复制或截图

**最佳实践建立**:
- 项目级 MEMORY.md（放在项目目录）
- 全局 MEMORY.md（放在 `~/.claude/MEMORY.md`）
- 重要信息及时保存到文件，不要依赖对话历史

### 9. 关键决策记录
**已做的决策**:
- [x] 使用分步引导而非一次性生成
- [x] 创建完整的模板和示例资源
- [x] 使用中文优化（针对中文用户）
- [x] 发布为 MIT 许可证开源项目
- [x] 使用 SSH 而非 HTTPS 进行 Git 操作

**待决策/改进**:
- [ ] 是否添加更多行业模板（电商、教育、新闻等）
- [ ] 是否创建视频教程
- [ ] 是否收集用户反馈进行迭代

### 10. 下次继续的切入点
**可以立即做的事**:
1. 添加新的分镜模板（如电商带货、知识付费、品牌宣传）
2. 优化提示词生成逻辑（根据用户反馈）
3. 创建使用教程或演示视频
4. 推广给 Seedance 用户社区

**技术改进方向**:
- 添加更多 Seedance 2.0 的高级功能示例
- 创建"提示词优化器"子功能
- 添加常用镜头语言的快捷选择

---

## 经验总结

### 做得好的地方
1. 完整阅读了 Seedance 2.0 手册，提取了核心信息
2. 设计了清晰的分步引导流程
3. 创建了丰富的配套资源（模板+示例+速查）
4. 成功配置了 SSH 并推送到 GitHub
5. 测试验证了 skill 的实际效果

### 学到的教训
1. **Skill 需要重启 Claude Code 才能识别** - 新创建的 skill 不会立即生效
2. **SSH 配置比 HTTPS 更方便** - 虽然初次配置复杂，但后续免密码
3. **MEMORY.md 很重要** - 跨会话保持上下文的关键
4. **用户安全意识** - 用户对 SSH 私钥安全很敏感，需要及时解释

### 关键工具/资源
- **Seedance 2.0 手册**: `/Users/elementsix/Desktop/vibecoding/🎬 即梦 Seedance 2.0 使用手册（全新多模态创作体验）.docx`
- **官方 Plugin 示例**: `~/.claude/plugins/marketplaces/claude-plugins-official/`
- **SSH 密钥**: `~/.ssh/id_ed25519_github`
- **GitHub 仓库**: https://github.com/elementsix/claude-seedance-plugin
