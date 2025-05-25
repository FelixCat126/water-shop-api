# 水商城脚本使用指南

## 📁 脚本目录结构

```
scripts/
├── init/           # 初始化脚本
│   └── system-init.js    # 系统初始化（首次部署必需）
├── tests/          # 测试脚本
│   └── comprehensive-test.js  # 综合功能测试
├── data/           # 数据脚本
│   ├── generate-*.js     # 数据生成脚本
│   └── create-*.js       # 数据创建脚本
└── utils/          # 工具脚本
    └── script-manager.js # 脚本管理工具
```

## 🚀 使用方法

### 首次部署
```bash
# 系统初始化（创建超级管理员等）
node scripts/init/system-init.js
```

### 功能测试
```bash
# 运行综合功能测试
node scripts/tests/comprehensive-test.js
```

### 脚本管理
```bash
# 查看和整理脚本
node scripts/utils/script-manager.js
```

## 📝 开发规范

1. **测试脚本**：放入 `tests/` 目录，开发完成后可删除
2. **初始化脚本**：放入 `init/` 目录，用于系统部署
3. **数据脚本**：放入 `data/` 目录，用于生成测试数据
4. **工具脚本**：放入 `utils/` 目录，提供辅助功能

## ⚠️  注意事项

- 初始化脚本只在首次部署时运行一次
- 测试脚本可以重复运行用于验证功能
- 数据脚本会检查重复，避免重复创建
- 定期清理不需要的临时脚本
