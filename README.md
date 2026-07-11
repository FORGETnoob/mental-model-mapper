# 🧠 认知对齐 CogAlign

> 不看代码写得对不对，看写代码的人脑子里想的是不是一回事。

检查不同模块对同一个概念的理解是否一致。扫描类型定义、枚举、命名、注释，检测认知冲突和隐含假设矛盾，生成认知地图报告。

## 为什么需要它？

- 三个模块在说 "User"，说的是三个完全不同的东西 → 认知对齐会发现
- OrderController 有 4 个状态，PaymentController 只认识 3 个 → 认知对齐会标红
- 模块 A 假设 id 不可变，模块 B 悄悄改了 id → 认知对齐会检测

这些不是 bug，但它们是**认知债务**——总有一天会变成 bug。

## 安装

```bash
npx skills add FORGETnoob/mental-model-mapper
```

## 使用方式

```
/cogalign                              # 分析当前目录
检查这个项目的认知对齐                    # 自然语言触发
扫描 src/ 的认知冲突                     # 聚焦子目录
order 和 payment 对 User 的理解一致吗    # 指定概念对比
```

## 与其他 Skill 的关系

| Skill | 做什么 | 什么时候用 |
|-------|--------|-----------|
| **cogalign** | 认知一致性、隐含假设 | 接手老项目、重构前 |
| code-review | bug、性能、简化 | 每次改代码前 |
| nuwa-skill | 蒸馏人的思维 → AI 角色 | 创建角色 prompt |

## License

MIT
