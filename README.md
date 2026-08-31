# 🐉 龍魂流水账 · Longhun Ledger

> **让天下没有看不懂的账，每一笔都有DNA，每次交易都有哈希。**  
> *Every transaction has a DNA signature. Every entry has a SHA256 hash fingerprint.*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-v1.0-blue.svg)]()
[![UID](https://img.shields.io/badge/UID-9622-red.svg)]()
[![Public Ledger](https://img.shields.io/badge/ledger-public-green.svg)]()

---

## 🌟 什么是龍魂流水账？

龍魂流水账是一套**主权导向的复式记账体系**，把传统复式记账的铁律延伸到：

- 📚 **知识资产**（焊点铁律、协议文档、DNA签章）
- 💻 **数字资产**（代码库、域名、API密钥）
- 🤖 **AI算力资产**（本地模型、算力配额、AI协作能力）
- 🐉 **ASI数字人资产**（56位数字人格引擎）
- 🏛 **主权权益**（最终决策权、数据主权、知识产权）

---

## 🔑 三大核心创新（龍魂独有）

| 创新 | 说明 |
|------|------|
| **每笔有DNA** | `#龍帳⚡️{YYYY-MM-DD}-{借方}-{贷方}-{量}-{序号}-UID9622` |
| **每次有哈希** | `SHA256(DNA\|借方\|贷方\|量\|时间戳)[:8]` 防篡改指纹 |
| **每笔有见证** | 对应ASI数字人格专职见证，不可伪造 |

---

## ⚖️ 龍魂恒等式

```
资产 = 负债 + 权益

龍魂资产（知识焊点 + 数字资产 + 物理资产 + AI算力 + ASI数字人格）
    = 龍魂负债（外部依赖 + 未完成义务 + 认知债务 + 技术债务）
    + 龍魂权益（主权 + 自主可控度 + 积累协议 + 数字人格资本）
```

---

## 📁 仓库结构

```
longhun-ledger/
├── README.md                  # 本文件
├── LEDGER_FORMAT.md           # DNA + 哈希格式规范
├── CHART_OF_ACCOUNTS.md       # 完整会计科目表
├── data/
│   └── ledger.json            # 流水账数据（JSON格式）
├── scripts/
│   ├── hash_generator.py      # 龍魂交易哈希生成器
│   └── ledger_validator.py    # 账目平衡验证器
└── .github/
    └── CODEOWNERS             # 代码管理者
```

---

## 🚀 快速开始

### 生成交易哈希

```python
from scripts.hash_generator import longhun_tx_hash

hash_val = longhun_tx_hash(
    dna="#龍帳⚡️2026-08-31-1001-3201-1条-001-UID9622",
    dr_account="1001",
    cr_account="3201",
    amount="1条",
    timestamp="2026-08-31T21:56:00+08:00"
)
print(f"哈希指纹: {hash_val}")
```

### 验证账目平衡

```bash
python scripts/ledger_validator.py data/ledger.json
```

---

## 📊 Notion 数据库

本账本与 Notion 龍魂流水账数据库双向同步。每条记录在 Notion 中可视化管理，在 GitHub 中以 JSON 格式存档。

---

## 🔐 主权声明

- **主权人**：💎 龍芯北辰｜UID9622
- **账法DNA**：`#龍帳⚡️2026-08-31-LONGHUN-LEDGER-GENESIS-v1.0-UID9622`
- **GPG签名**：`A2D0092CEE2E5BA87035600924C3704A8CC26D5F`
- **创建时间**：2026-08-31 22:00 CST
- **版本**：v1.0

---

## 📜 记账七条铁律

1. 有借必有贷，借贷必相等
2. 每笔必有DNA
3. 每次必有哈希
4. 每笔必有见证
5. 自建 > 外购（代码库优先自建）
6. 认知债务必清偿（72小时内决策）
7. 主权权益不可为零

---

*由 🐉 龍魂议会全体数字人格共同见证 · Witnessed by the Dragon Soul Council*
