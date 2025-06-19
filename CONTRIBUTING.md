# 🤝 贡献指南

感谢您对 Agent PPT 竞赛展示平台的关注！我们欢迎所有形式的贡献。

## 📋 贡献方式

### 1. 添加新的Agent作品

这是最主要的贡献方式。如果您有AI Agent制作的基于源PDF的PPT作品，欢迎添加到平台中。

#### 步骤：

1. **Fork 仓库**
   ```bash
   git clone https://github.com/your-username/Agent-PPT-competition.git
   cd Agent-PPT-competition
   ```

2. **创建Agent目录**
   ```bash
   mkdir [YourAgentName]_Agent
   cd [YourAgentName]_Agent
   ```

3. **准备必需文件**
   - `index.html` - 在线预览页面
   - `[AgentName]_presentation.pptx` - PowerPoint文件
   - `[AgentName]_presentation.pdf` - PDF版本
   - `README.md` - Agent介绍

4. **创建预览页面**
   
   参考 `MiniMax_Agent/index.html` 的结构，创建您的预览页面。基本模板：
   
   ```html
   <!DOCTYPE html>
   <html lang="zh-CN">
   <head>
       <meta charset="UTF-8">
       <title>[Agent Name] - PPT展示</title>
       <!-- 样式和脚本 -->
   </head>
   <body>
       <!-- 您的PPT展示内容 -->
   </body>
   </html>
   ```

5. **更新主页面**
   
   在根目录的 `index.html` 中添加您的Agent卡片：
   
   ```html
   <div class="agent-card">
       <div class="agent-header">
           <div class="agent-icon">[首字母]</div>
           <div class="agent-name">[Agent名称]</div>
       </div>
       <div class="agent-description">
           [Agent描述]
       </div>
       <div class="agent-actions">
           <a href="./[YourAgentName]_Agent/index.html" class="btn btn-primary" target="_blank">
               🎯 在线预览
           </a>
           <a href="./[YourAgentName]_Agent/[AgentName]_presentation.pptx" class="btn btn-secondary" download>
               📥 下载PPTX
           </a>
           <a href="./[YourAgentName]_Agent/[AgentName]_presentation.pdf" class="btn btn-secondary" target="_blank">
               📄 查看PDF
           </a>
       </div>
   </div>
   ```

6. **更新对比表格**
   
   在主页面的对比表格中添加一行：
   
   ```html
   <tr>
       <td><strong>[Agent名称]</strong></td>
       <td>[幻灯片数量]</td>
       <td>[设计风格]</td>
       <td><span class="status-badge status-completed">已完成</span></td>
       <td>[特色功能]</td>
   </tr>
   ```

7. **提交更改**
   ```bash
   git add .
   git commit -m "Add [Agent Name] PPT presentation"
   git push origin main
   ```

8. **创建Pull Request**
   
   在GitHub上创建PR，描述您添加的Agent作品。

### 2. 改进现有功能

- 优化UI/UX设计
- 增加新的交互功能
- 提升性能和兼容性
- 修复bug

### 3. 完善文档

- 改进README
- 添加使用教程
- 翻译文档
- 添加代码注释

## 📝 文件规范

### 目录结构
```
[YourAgentName]_Agent/
├── index.html                    # 必需：在线预览页面
├── [AgentName]_presentation.pptx # 必需：PowerPoint文件
├── [AgentName]_presentation.pdf  # 必需：PDF版本
├── README.md                     # 必需：Agent介绍
├── slides/                       # 可选：单页幻灯片
│   ├── slide1.html
│   ├── slide2.html
│   └── ...
├── images/                       # 可选：图片资源
├── summary.md                    # 可选：制作总结
└── assets/                       # 可选：其他资源
```

### 命名规范

- **Agent目录**: `[AgentName]_Agent/`
- **PPT文件**: `[AgentName]_presentation.pptx`
- **PDF文件**: `[AgentName]_presentation.pdf`
- **预览页面**: `index.html`
- **图片文件**: 使用描述性名称，如 `slide1_preview.png`

### 代码规范

#### HTML
- 使用HTML5语义化标签
- 保持良好的缩进（2个空格）
- 添加必要的meta标签
- 确保可访问性

#### CSS
- 使用CSS变量定义颜色和尺寸
- 采用BEM命名规范
- 确保响应式设计
- 避免使用!important

#### JavaScript
- 使用现代ES6+语法
- 添加适当的注释
- 确保浏览器兼容性
- 避免全局变量污染

## 🎨 设计指南

### 视觉风格
- **色彩**: 使用主题色彩变量
- **字体**: 系统字体栈
- **间距**: 8px基础网格
- **圆角**: 4px-12px
- **阴影**: 层次化阴影

### 交互设计
- **响应时间**: 动画时间 < 300ms
- **反馈**: 提供清晰的交互反馈
- **可访问性**: 支持键盘导航
- **移动端**: 触摸友好的交互

## 🧪 测试要求

### 浏览器兼容性
- Chrome (最新版本)
- Firefox (最新版本)
- Safari (最新版本)
- Edge (最新版本)

### 设备测试
- 桌面端 (1920x1080, 1366x768)
- 平板端 (768x1024)
- 移动端 (375x667, 414x896)

### 功能测试
- 所有链接正常工作
- 文件可以正常下载
- 页面加载速度合理
- 交互功能正常

## 📋 Pull Request 检查清单

提交PR前，请确保：

- [ ] 代码遵循项目规范
- [ ] 添加了必要的文档
- [ ] 测试了所有功能
- [ ] 更新了主页面
- [ ] 文件大小合理（< 50MB）
- [ ] 没有敏感信息
- [ ] 提交信息清晰

## 🐛 问题报告

发现bug？请创建Issue并包含：

1. **问题描述**: 清晰描述问题
2. **重现步骤**: 详细的重现步骤
3. **期望行为**: 期望的正确行为
4. **环境信息**: 浏览器、操作系统等
5. **截图**: 如果适用，添加截图

## 💡 功能建议

有新想法？欢迎创建Feature Request：

1. **功能描述**: 详细描述建议的功能
2. **使用场景**: 说明使用场景和价值
3. **实现思路**: 如果有，提供实现思路
4. **优先级**: 说明功能的重要性

## 📞 联系方式

- **GitHub Issues**: 技术问题和bug报告
- **GitHub Discussions**: 功能讨论和交流
- **Email**: [your-email@example.com]

## 🙏 致谢

感谢所有贡献者的努力！您的贡献让这个项目变得更好。

### 贡献者列表

<!-- 这里会自动更新贡献者列表 -->

---

**再次感谢您的贡献！** 🎉