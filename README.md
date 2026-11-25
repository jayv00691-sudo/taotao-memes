# 桃桃的表情包

一只白猫桃桃用的表情包图库。

## 结构

```
.
├── manifest.json    # AstrBot 插件读取
├── memes/           # 按情绪分类，一个目录一类
│   ├── happy/
│   ├── sad/
│   ├── confused/
│   ├── surprised/
│   ├── shy/
│   └── meow/
└── previews/
    └── cover.jpg    # 封面（可选）
```

## 两种用法

### 1. AstrBot 表情包管理器

面板 → 插件 → 表情包管理器 → 资源广场 → 「按来源安装」：

| 字段 | 值 |
| --- | --- |
| 仓库 | `jayv00691-sudo/taotao-memes` |
| 分支 | `main` |
| 目录 | `.` |

### 2. agent-expression skill（任意 agent）

```bash
MEME_PACK=/path/to/taotao-memes python3 scripts/pick-meme.py happy
```

返回图片的绝对路径，再由宿主自己发出去。

## 加图

1. 把图片放进对应情绪目录
2. `version` 加一
3. 提交推送
