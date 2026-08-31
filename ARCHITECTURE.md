# 🧩 龍魂账法 ·模块架构说明

## 核心原则：不重造轮子

```
地基（永不动）
  └── scripts/longhun_base.py   ← 唯一真源，只 import，永不复制修改

扩展层（只加）
  └── scripts/audit_engine.py   ← from longhun_base import ...
  └── scripts/router.py         ← from audit_engine import ...
  └── scripts/lhi_calculator.py  ← from router import ...
  └── scripts/my_new_feature.py  ← from {\u4e0a层模块} import ...
```

## 扩展步骤（每次加功能都这四步）

```python
# 1. 确定继承的起点
# 2. import 层级最高的已有模块
# 3. 只写新加的方法，已有的用 super() 调用
# 4. 测试后 push，不动旧文件
from {\u5df2有模块} import {\u5df2有类}

class {\u65b0功能}({\u5df2有类}):
    def {\u65b0方法}(self): ...
    def {\u91cd写方法}(self):
        base = super().{\u65b9法}()  # 先取父类结果
        return f"{base} | {\u65b0内容}"    # 只加新内容
```

## 文件责任表

| 文件 | 职责 | 可修改？ |
|------|------|----------|
| `longhun_base.py` | 地基：DNA生成+哈希+见证 | ✘ 永不动 |
| `audit_engine.py` | 三色审计引擎 | ✔ 只加 |
| `router.py` | 路由分发器 | ✔ 只加 |
| `lhi_calculator.py` | 健康度指数 | ✔ 只加 |
| `example_extension.py` | 扩展示例 | ✔ 仅供参考 |

## DNA → 哈希 → 见证 → 三色 ：四个细节永不变

1. **DNA格式**：`#龍帳⚡️YYYY-MM-DD-{DR}-{CR}-{AMT}-{SEQ:03d}-UID9622`
2. **哈希公式**：`SHA256(dna|dr|cr|amount|timestamp)[:8].upper()`
3. **见证来源**：仅从 `WITNESS` 字典取，永不硬编码
4. **账簿行标识**：末尾必须有 `✓平`
