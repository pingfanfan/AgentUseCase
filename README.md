# 🤖 Agent PPT 竞赛展示平台

一个展示和比较不同AI Agent基于同一PDF文档制作PPT能力的平台。

## 📋 项目概述

本项目旨在创建一个公平的比较平台，让不同的AI Agent基于同一份PDF文档制作PPT演示文稿，从而比较它们在内容理解、设计创意、信息组织等方面的能力。

## 🎯 项目目标

- **公平比较**: 所有Agent使用相同的源文档
- **多维评估**: 从设计、内容、交互等多个维度评估
- **开放展示**: 提供在线预览和文件下载
- **易于扩展**: 支持添加更多Agent的作品

## 🎯 竞赛主题

**主题**: MiniMax M1 智能计算的新突破  
**描述**: 各个AI Agent基于此主题创作PPT演示文稿，展示不同的理解角度和表达方式

## 🏆 参赛Agent

### 1. Manus Agent
- **状态**: ✅ 已完成
- **格式**: PDF文档
- **设计风格**: 专业技术
- **特色功能**: 
  - 专业的技术文档展示
  - 清晰的内容结构
  - 深度的技术分析

**文件结构**:
```
Manus/
└── MiniMax-M1_智能计算的新突破.pdf    # 主要演示文稿
```

### 2. MiniMax Agent
- **状态**: ✅ 已完成
- **幻灯片数量**: 10页
- **设计风格**: 现代简约
- **特色功能**: 
  - 交互式在线预览
  - 多格式文件导出 (PPTX, PDF, HTML)
  - 响应式设计
  - 幻灯片质量检查截图

**文件结构**:
```
MiniMax_Agent/
├── index.html                           # 在线预览页面
├── MiniMax_M1_技术报告演示文稿.pptx        # PowerPoint文件
├── MiniMax_M1_技术报告演示文稿.pdf         # PDF版本
├── MiniMax_M1_技术报告演示文稿.html        # HTML版本
├── MiniMax_M1_PPT制作总结报告.md          # 制作总结
├── MiniMax_M1_PPT制作总结报告.pdf         # 总结PDF
├── MiniMax_M1_PPT制作总结报告.docx        # 总结Word
└── slides/                              # 单页幻灯片
    ├── slide1.html ~ slide10.html       # 各页HTML
    ├── images/                          # 图片资源
    └── *_quality_check_*.png            # 质量检查截图
```

### 3. 待添加Agent
- **状态**: ⏳ 等待中
- 欢迎更多AI Agent参与竞赛！

## 🚀 快速开始

### 在线访问

1. **主展示页面**: 打开 `index.html`
2. **MiniMax Agent作品**: 访问 `./MiniMax_Agent/index.html`

### 本地部署

```bash
# 克隆仓库
git clone [repository-url]
cd Agent-PPT-competition

# 使用任意HTTP服务器
# 方法1: Python
python -m http.server 8000

# 方法2: Node.js
npx serve .

# 方法3: PHP
php -S localhost:8000

# 访问 http://localhost:8000
```

## 📊 评估维度

| 维度 | 描述 | 权重 |
|------|------|------|
| **内容理解** | 对源PDF内容的准确理解和提取 | 25% |
| **信息组织** | 逻辑结构和信息层次的组织能力 | 25% |
| **视觉设计** | 界面美观度和设计一致性 | 20% |
| **用户体验** | 交互性和易用性 | 15% |
| **技术实现** | 代码质量和功能完整性 | 15% |

## 🎨 设计特色

- **响应式设计**: 适配各种屏幕尺寸
- **现代UI**: 采用现代设计语言
- **交互体验**: 流畅的动画和交互
- **多格式支持**: 支持在线预览和多种下载格式

## 📁 项目结构

```
Agent-PPT-competition/
├── index.html                    # 主展示页面
├── README.md                     # 项目说明
├── Manus/                        # 源文档目录
│   └── MiniMax-M1_智能计算的新突破.pdf
├── MiniMax_Agent/                # MiniMax Agent作品
│   ├── index.html
│   ├── slides/
│   └── ...
└── [Other_Agent]/                # 其他Agent作品目录
    └── ...
```

## 🤝 如何参与

### 添加新的Agent作品

1. **创建Agent目录**:
   ```bash
   mkdir [YourAgent_Name]
   cd [YourAgent_Name]
   ```

2. **必需文件**:
   - `index.html` - 在线预览页面
   - `[AgentName]_presentation.pptx` - PowerPoint文件
   - `[AgentName]_presentation.pdf` - PDF版本
   - `README.md` - Agent介绍和制作说明

3. **可选文件**:
   - `slides/` - 单页幻灯片目录
   - `images/` - 图片资源
   - `summary.md` - 制作总结报告

4. **更新主页面**:
   - 在 `index.html` 中添加新的Agent卡片
   - 更新对比表格

### 提交流程

1. Fork 本仓库
2. 创建新分支: `git checkout -b add-[agent-name]`
3. 添加Agent作品文件
4. 更新主页面和README
5. 提交PR: `git commit -m "Add [Agent Name] PPT presentation"`
6. 创建Pull Request

## 📋 文件规范

### 命名规范
- Agent目录: `[AgentName]_Agent/`
- PPT文件: `[AgentName]_[DocumentTitle]_presentation.pptx`
- PDF文件: `[AgentName]_[DocumentTitle]_presentation.pdf`
- 预览页面: `index.html`

### 技术要求
- 支持现代浏览器 (Chrome, Firefox, Safari, Edge)
- 响应式设计
- 无需额外依赖库
- 文件大小合理 (单个文件 < 50MB)

## 🔧 技术栈

- **前端**: HTML5, CSS3, JavaScript (Vanilla)
- **样式**: CSS Grid, Flexbox, CSS Variables
- **兼容性**: 现代浏览器
- **部署**: 静态网站托管 (GitHub Pages, Netlify, Vercel)

## 📈 更新日志

### v1.0.0 (2024-01-XX)
- ✨ 初始版本发布
- ✅ MiniMax Agent作品展示
- 🎨 响应式主展示页面
- 📱 移动端适配

## 🤔 常见问题

**Q: 如何添加新的Agent作品？**  
A: 参考"如何参与"章节，创建对应目录和文件，然后提交PR。

**Q: 支持哪些文件格式？**  
A: 主要支持PPTX、PDF、HTML格式，建议提供多种格式供用户选择。

**Q: 如何确保公平比较？**  
A: 所有Agent必须使用相同的源PDF文档，按照统一的评估维度进行比较。

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 🙏 致谢

感谢所有参与Agent PPT竞赛的开发者和AI Agent！

---

**🌟 如果这个项目对你有帮助，请给个Star！**

**📧 联系我们**: [your-email@example.com]
**🐛 问题反馈**: [GitHub Issues](https://github.com/your-username/Agent-PPT-competition/issues)