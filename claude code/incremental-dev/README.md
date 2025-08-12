# 增量开发实践指南 (Incremental Development Practice Guide)

## 📌 概述
这是一份强调渐进式开发、小步快跑的 Claude Code 配置文件，源自 Chris Dzombak 的最佳实践文章。

📄 **可用版本**：
- [CLAUDE.md](./CLAUDE.md) - 英文原版
- [CLAUDE-zh.md](./CLAUDE-zh.md) - 中文翻译版

## 🎯 适用场景
- 复杂功能的逐步实现
- 需要频繁测试和验证的项目
- 团队协作开发
- 重构遗留代码
- 学习新技术栈时的探索性开发

## ✨ 核心特性

### 1. **3次尝试规则**
- 遇到问题最多尝试3次
- 避免在错误方向上浪费时间
- 强制停下来反思和寻找替代方案

### 2. **TDD 工作流**
- 先写测试，再写实现
- 每次提交都必须通过所有测试
- 小步快跑，增量提交

### 3. **清晰的决策框架**
优先级排序：
1. 可测试性
2. 可读性
3. 一致性
4. 简单性
5. 可逆性

### 4. **质量底线**
- 永不绕过提交钩子
- 永不禁用测试
- 永不提交无法编译的代码

## 📊 效果展示

### Before (没有配置)
```
AI: 我将重构整个系统架构...
[生成大量复杂代码]
[测试失败]
AI: 让我再试一次完全不同的方法...
```

### After (使用此配置)
```
AI: 我将分3个阶段实现：
Stage 1: 添加单元测试 ✓
Stage 2: 最小功能实现 ✓  
Stage 3: 优化和重构 ✓
每个阶段都确保测试通过后再继续。
```

## 🔧 使用方法

### 英文版
```bash
# 将配置文件复制到项目根目录
cp "claude code/incremental-dev/CLAUDE.md" ./CLAUDE.md
```

### 中文版
```bash
# 使用中文版配置
cp "claude code/incremental-dev/CLAUDE-zh.md" ./CLAUDE.md
```

## 📚 原始来源
- **文章**: [Getting Good Results from Claude Code](https://www.dzombak.com/blog/2025/08/getting-good-results-from-claude-code/)
- **作者**: Chris Dzombak
- **发现**: [X (Twitter) 讨论](https://x.com/ShenHuang_/status/1954687442868752698)

## 💡 核心理念
> "增量优于全部重构，代码要清晰而非聪明"

将高级工程师的思维模式系统化，让 AI 从工具变成有章法的"准同事"。