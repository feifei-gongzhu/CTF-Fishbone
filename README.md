# 🐟 CTF Fishbone Attack Framework v1.0

> Recursive attack protocol for CTF Web challenges — "Every privilege escalation restarts the recon → exploit loop."

[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Version](https://img.shields.io/badge/version-5.1-orange)]()

---

## What is Fishbone?

Fishbone is a **structured attack methodology** for CTF Web challenges, not just another payload collection. It introduces a **recursive spine model** where:

- **Spine (脊梁)** — milestone nodes anchored on privilege levels
- **Upward Bones (向上鱼刺)** — confirmed facts at current level
- **Downward Bones (向下鱼刺)** — recon actions to perform at each level
- **Vector Extensions (鱼刺延伸)** — attack vectors ranked by priority (P0/P0.5/P1/P2)
- **Recursive Trigger** — privilege change OR intel breakthrough → auto-generate next spine node

```
Guest → [Vector X] → www-data → [Intel Y] → [PrivEsc Z] → Root → Flag
```

## Quick Start

Read `FISHBONE.md` and follow the 3-step flow:

```
30s Routing → Recursive Spine → Writeup Archive
```

## Key Features

| Feature | Description |
|---------|-------------|
| **30s Routing Table** | Categorize challenge instantly: white-box (PHP/Python/Java/Node/Go) vs black-box (login/upload/API/search) |
| **Recursive Engine** | Auto-restart recon cycle on every privilege or intel breakthrough |
| **P0.5 Combo Chains** | SSRF+LFI, SQLi+FileWrite, PrototypePollution+RCE — think in composition |
| **Exploit Quick-Ref** | Ready-to-use chains for SQLi, SSTI, LFI, deserialization, prototype pollution |
| **Java Arsenal** | Shiro, Fastjson, Log4j, Spring Boot, Tomcat, Struts2 |
| **Bypass Dictionary** | WAF filter bypass, PHP disable_functions 9-layer bypass, weak-type tricks |
| **White-box Auditing** | Language-specific sink functions and patterns (PHP/Python/Java/Node.js) |
| **Time Discipline** | 35min per node, 10min per vector — explore first, exploit deep later |

## Structure

```
CTF-Fishbone/
├── README.md          # You are here
├── FISHBONE.md        # Full framework (framework body)
└── LICENSE            # MIT
```

## Why Fishbone?

Most CTF references are flat payload dictionaries. Fishbone gives you a **decision engine**:

1. **When stuck** — follow the recursive trigger, go back to recon
2. **When losing time** — the stop-loss hook fires at 10min/35min limits
3. **When choosing** — P0 > P0.5 > P1 > P2 priority system
4. **When done** — standardized writeup template

This is the framework I use in real CTF competitions. It's opinionated, battle-tested, and optimized for speed.

## License

MIT — Use it, fork it, improve it. Attribution appreciated.

---

# 🐟 CTF 鱼骨攻击框架 v1.0

> 递归式 CTF Web 攻击协议 — "每获得新权限，整个搜集→发现→利用循环自动重启。"

## 这是什么？

鱼骨框架是一套**结构化攻击方法论**，而不是简单的 Payload 字典。核心概念：

- **脊梁** — 以权限等级为锚点的里程碑节点
- **向上鱼刺** — 当前节点已确认的事实
- **向下鱼刺** — 基于当前权限的再搜集动作
- **鱼刺延伸** — 按优先级排列的攻击向量
- **递归触发器** — 权限变更或情报突破 → 自动生成下一个节点

## 快速开始

阅读 `FISHBONE.md`，按三步走：

```
30秒路由定方向 → 递归鱼骨推进 → 鱼尾归档
```

## 核心亮点

- **30 秒题型路由** — 白盒 (PHP/Python/Java/Node/Go) vs 黑盒 (登录框/上传/搜索/API)
- **递归引擎** — 每次权限升级自动重启搜集循环
- **P0.5 组合利用** — SSRF+LFI、SQLi+文件写入、原型链污染+RCE
- **利用链速查** — SQLi / SSTI / LFI / 反序列化 / 原型链污染
- **Java 专项** — Shiro / Fastjson / Log4j / Spring Boot / Tomcat / Struts2
- **绕过字典** — WAF 过滤绕过 / PHP disable_functions 9 层绕过 / 弱类型
- **白盒审计** — 按语言的 Sink 函数与审计模式
- **时间纪律** — 单节点 35min / 单向量 10min 止损

## 许可

MIT — 随意使用、Fork、改进。
