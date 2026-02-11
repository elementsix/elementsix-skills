# 🎬 Seedance Storyboard - ElementSix Skills

<p align="center">
  <img src="https://img.shields.io/github/stars/elementsix/elementsix-skills?logo=github&logoColor=white&labelColor=333&color=ffb700&style=for-the-badge" alt="stars" />
  &nbsp;
  <img src="https://img.shields.io/github/forks/elementsix/elementsix-skills?logo=github&logoColor=white&labelColor=333&color=3498db&style=for-the-badge" alt="forks" />
  &nbsp;
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-2ecc71?style=for-the-badge&labelColor=333&logo=open-source-initiative&logoColor=white" alt="license" /></a>
  &nbsp;
  <img src="https://img.shields.io/badge/Version-1.1.0-blue?style=for-the-badge&labelColor=333" alt="version" />
</p>

<p align="center">
  <b>将任何想法转换成即梦 Seedance 2.0 专业分镜提示词的 Claude Code Skill</b>
</p>

## 📖 简介

Seedance 2.0 是即梦（剪映）推出的强大多模态 AI 视频生成模型，但写出好的提示词对普通人来说很困难。这个 Skill 通过一步步引导，帮你把简单的想法转换成专业的分镜提示词。

## ✨ 功能特点

### 🎯 核心能力
- ✅ **分步引导** - 从想法到完整提示词的完整流程
- ✅ **覆盖全能力** - 支持 Seedance 2.0 所有功能（多模态、延长、编辑等）
- ✅ **专业模板** - 内置 6 套分镜模板
- ✅ **中文优化** - 专门针对中文用户设计

### 🚀 v1.1.0 新增功能
- 🔥 **视频延长** - 在已有视频基础上"接着拍"，平滑衔接
- 🔥 **复杂运镜** - 希区柯克变焦、环绕跟拍、一镜到底精准复刻
- 🔥 **特效复刻** - 变装特效、粒子特效、拼图转场等创意效果
- 🔥 **角色一致性** - 保持人物形象的连续叙事能力
- 🔥 **多场景融合** - 无缝转场、空间转换自由创作

## 🚀 安装方法

### 📋 前置条件

- 需要先安装好 [Claude Code](https://claude.ai/code)

### 🛠️ 安装步骤

```bash
# 1. 添加 Marketplace
/plugin marketplace add elementsix/elementsix-skills

# 2. 安装 Skill
/plugin install seedance-storyboard@elementsix-skills
```

### ✅ 生效确认

- 安装好后**退出 Claude Code，重新进入**，`/seedance-storyboard` 命令就生效了

## 🔄 更新技能

将 Skill 更新到最新版本：

1. 在 Claude Code 中运行 `/plugin`
2. 切换到 **Marketplaces** 标签页（使用方向键或 Tab）
3. 选择 `elementsix-skills`
4. 选择 **Update marketplace**

也可以选择 **Enable auto-update** 启用自动更新，每次启动时自动获取最新版本。

![更新技能步骤](assets/update-skill.png)

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

## 💡 实战示例

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

### 示例 2：希区柯克变焦（v1.1.0 新增）

**素材**：@图片1(男人形象)、@图片2(电梯场景)、@视频1(参考运镜)

**提示词**：
```
参考@图片1的男人形象，他在@图片2的电梯中，完全参考@视频1的所有运镜效果
还有主角的面部表情，主角在惊恐时希区柯克变焦，然后几个环绕镜头展示电梯内视角
电梯门打开，跟随镜头走出电梯，男人环顾四周
```

### 示例 3：视频延长创作（v1.1.0 新增）

**素材**：@视频1(原视频)、@图片1-2(角色参考)

**提示词**：
```
延长15s视频，参考@图片1、@图片2的驴骑摩托车的形象
画面1：侧面固定镜头，驴骑着摩托车冲出棚栏，旁边的鸡受到惊吓
画面2：驴骑着摩托在沙地盘旋，俯拍盘旋特技，掀起烟雾
画面3：背景雪山，驴骑着车从山坡飞越过
广告语"Inspire Creativity, Enrich Life"通过遮罩形式出现
```

### 示例 4：变装特效（v1.1.0 新增）

**素材**：@视频1(参考特效)、@图片1(首帧人物)、@图片2(最终形象)

**提示词**：
```
将@视频1的首帧人物替换成@图片1，完全参考@视频1的特效和动作
手里的花蕊长出玫瑰花瓣，裂纹在脸部向上延伸，逐渐被杂草覆盖
人物双手拂过脸部，杂草变成粒子消散，最后变成@图片2的长相
```

**更多示例**见 `skills/seedance-storyboard/README.md`

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

### 📊 技术参数

| 输入类型 | 支持格式 | 数量限制 | 大小限制 |
|---------|---------|---------|---------|
| **图片** | jpeg, png, webp, bmp, tiff, gif | ≤ 9 张 | < 30 MB |
| **视频** | mp4, mov (2-15s) | ≤ 3 个 | < 50 MB |
| **音频** | mp3, wav (≤15s) | ≤ 3 个 | < 15 MB |
| **文本** | 自然语言描述 | - | - |
| **混合上限** | **12 个文件** | | |

> 💡 提示：视频参考会消耗更多生成额度，建议优先上传对画面影响最大的素材

### 🎯 核心功能

| 功能 | 说明 |
|------|------|
| **多模态输入** | 图片、视频、音频、文本自由组合创作 |
| **参考图像** | 精准还原画面构图、角色细节、服装样式 |
| **参考视频** | 支持镜头语言、复杂动作节奏、创意特效复刻 |
| **视频延长** | 平滑延长与衔接，可"接着拍" |
| **视频编辑** | 角色更替、剧情颠覆、片段调整、场景融合 |
| **基础增强** | 物理规律更合理、动作更自然、指令理解更精准 |

## 📝 提示词语法

### 基础语法
使用 `@素材名` 引用多模态素材：

```
@图片1 作为首帧
@图片2 作为角色形象参考
@视频1 参考运镜方式
@音频1 用于配乐
```

### 高级用法

| 场景 | 语法示例 |
|------|---------|
| **首帧 + 视频动作** | `@图片1 为首帧，参考@视频1 的打斗动作` |
| **视频延长** | `将@视频1 延长 5s`（生成长度选"新增部分"时长） |
| **角色替换** | `将@视频1 中的女生换成@图片1 的形象` |
| **完整运镜复刻** | `完全参考@视频1 的所有运镜效果和表情` |
| **多视频融合** | `在@视频1 和@视频2 之间加场景，内容为 xxx` |
| **参考视频声音** | `使用@视频1 的背景音乐和节奏` |

## 🔗 即梦平台信息

- **官网**：https://jimeng.jianying.com
- **入口**：Seedance 2.0 - 全能参考 / 首尾帧

### ⚠️ 重要限制

- **暂不支持写实真人脸部素材**（图片和视频均会被系统自动拦截）
- **视频参考会消耗更多生成额度**
- **视频像素范围**：640×640 (480p) 至 834×1112 (720p)
- **混合输入总上限**：12 个文件

### 💡 使用建议

1. 优先上传对画面或节奏影响最大的素材
2. 多模态素材多时，务必检查 @对象标注是否清楚
3. 视频延长功能：选择的生成长度应为"新增部分"的时长
4. 复杂运镜可用"完全参考@视频1的所有运镜效果"确保精准复刻

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
