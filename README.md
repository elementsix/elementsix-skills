# 🎬 Seedance Storyboard - ElementSix Skills

<p align="center">
  <img src="https://img.shields.io/github/stars/elementsix/elementsix-skills?logo=github&logoColor=white&labelColor=333&color=ffb700&style=for-the-badge" alt="stars" />
  &nbsp;
  <img src="https://img.shields.io/github/forks/elementsix/elementsix-skills?logo=github&logoColor=white&labelColor=333&color=3498db&style=for-the-badge" alt="forks" />
  &nbsp;
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-2ecc71?style=for-the-badge&labelColor=333&logo=open-source-initiative&logoColor=white" alt="license" /></a>
</p>

将任何想法转换成即梦 Seedance 2.0 专业分镜提示词的 Claude Code Skill。

## 📖 简介

Seedance 2.0 是即梦（剪映）推出的强大多模态 AI 视频生成模型，但写出好的提示词对普通人来说很困难。这个 Skill 通过一步步引导，帮你把简单的想法转换成专业的分镜提示词。

## ✨ 功能特点

- ✅ **分步引导** - 从想法到完整提示词的完整流程
- ✅ **覆盖全能力** - 支持 Seedance 2.0 所有功能（多模态、延长、编辑等）
- ✅ **专业模板** - 内置 6 套分镜模板和 10 个完整示例
- ✅ **中文优化** - 专门针对中文用户设计

## 🚀 安装方法

### 前提条件

- 已安装 [Claude Code](https://claude.ai/code)

### 安装步骤

```bash
# 1. 添加 Marketplace
/plugin marketplace add elementsix/elementsix-skills

# 2. 安装 Skill
/plugin install seedance-storyboard@elementsix-skills

# 3. 重启 Claude Code（重要！）
# 退出 Claude Code 后重新进入，命令 /seedance-storyboard 才会生效
```

> ⚠️ **注意**：安装完成后必须**退出并重新进入 Claude Code**，命令 `/seedance-storyboard` 才能正常使用。

## 🎯 使用方法

安装后，输入以下命令使用：

```bash
/seedance-storyboard
```

然后 Claude 会一步步引导你：

1. **理解想法** - 你想讲什么故事？
2. **深入挖掘** - 风格、镜头、动作、声音
3. **构建分镜** - 按时间轴拆解镜头
4. **生成提示词** - 输出可直接使用的专业提示词
5. **优化建议** - 提供改进和多模态素材建议

## 💡 示例

### 示例 1：古风舞蹈

**你的想法**："一个女孩在樱花树下跳舞"

**生成的提示词**：
```
电影级写实风格，15秒，16:9宽屏，日落黄金时刻的温暖氛围

0-3秒：远景缓慢推近，海平线夕阳，女孩剪影站在沙滩上，裙摆被海风吹动
3-7秒：中景环绕镜头，女孩开始旋转起舞，长发和裙摆飞扬，夕阳逆光形成轮廓光
7-11秒：近景跟随移动，女孩面向镜头舞动，表情自由愉悦，海浪轻拍沙滩作为背景
11-13秒：特写手部动作，手指划过夕阳，光影在指尖流转
13-15秒：远景拉远，女孩在落日余晖中定格，画面渐暗

背景音效：海浪声 + 轻柔的钢琴配乐
```

### 示例 2：产品广告

**你的想法**："展示一款新手机"

**更多示例**见 `seedance-storyboard/examples/example-prompts.md`

## 📁 文件结构

```
elementsix-skills/
├── .claude-plugin/
│   └── marketplace.json              # Marketplace 配置
├── README.md                         # 本文件
└── skills/
    └── seedance-storyboard/          # 主 Skill 目录
        ├── SKILL.md                  # Skill 核心逻辑
        ├── README.md                 # Skill 详细说明
        ├── quick-reference.md        # 快速参考卡片
        ├── templates/
        │   └── storyboard-template.md    # 6套分镜模板
        └── examples/
            └── example-prompts.md        # 10个完整示例
```

## 🎬 Seedance 2.0 核心能力

- **多模态输入**：图片（≤9张）、视频（≤3个）、音频（≤3个）、文本
- **参考图像**：精准还原画面构图、角色细节
- **参考视频**：支持镜头语言、复杂动作节奏、创意特效复刻
- **视频延长**：平滑延长与衔接，可"接着拍"
- **视频编辑**：角色更替、剧情颠覆、片段调整

## 📝 提示词语法

使用 `@素材名` 引用多模态素材：

```
@图片1 作为首帧
@图片2 作为角色形象参考
@视频1 参考运镜方式
@音频1 用于配乐
```

## 🔗 即梦平台信息

- **官网**：https://jimeng.jianying.com
- **入口**：Seedance 2.0 - 全能参考 / 首尾帧
- **限制**：暂不支持写实真人脸部素材

## 🤝 贡献

欢迎提交 Issue 和 PR！

## 📄 许可证

MIT License

---

## ⭐ Star History

<p align="center">
  <a href="https://star-history.com/#elementsix/elementsix-skills&Date">
    <img src="https://api.star-history.com/svg?repos=elementsix/elementsix-skills&type=Date" alt="Star History" width="800" />
  </a>
</p>
