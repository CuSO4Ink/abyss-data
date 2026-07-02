---
type: development-hub
status: active
authority: canonical
created: 2026-06-30
updated: 2026-06-30
replaces_all_planning_docs: true
note: 本文件是 abyss-future-planning 的唯一现行文档,其余 13 份已归档至 archive/
tags:
  - abyss/dev-hub
  - abyss/single-source-of-truth
---

# Abyss 开发主控 (DEV HUB)

> 这是 Abyss 开发的**唯一现行文档 / Single Source of Truth**。
> abyss-future-planning 文件夹里其余 13 份规划文档已全部移入 `archive/`,仅作历史追溯,**不再当作指令来源**。
> 所有基于当前方向仍然有效的需求,已抽取、去重、归并到本文件 §3。
> 进度、需求、重点、决策的任何变化,**只在这里更新**。

---

## 0. 怎么用这份文档(铁律)

```text
1. 每次开工:看 §1 当前重点 + §2 看板 → 立刻知道现在该干什么。
2. 新需求/想法:登记到 §3 需求清单(必须带一条 kill criteria 红线)。
3. 做完一件事:更新 §2 看板 + 在 §6 决策日志追加一行(只增不改)。
4. 接入外部 AI:把 §4 边界 + §5 协作契约 + §3 里相关那条需求发给它,不要全仓乱丢。
5. 任何改动遵守 §4 六条边界;碰治理核心面走 §5 升级流程。
```

一句话:**方向一个出口,进度一个看板,需求一个入口,全在这里。**

---

## 1. 当前状态与唯一重点

**一句话现状**
> 自修改引擎已冻结(实测 6% 成功率)。路线回归"主权薄内核 + 外部能力适配器"。
> 内核(源码/规则/schema/prompt/契约)改动改走 **Git PR**;系统成长发生在**记忆/SOP/技能数据层**,而非源码自改写。
> 北极星 = 成为贴合 Owner 工作与生活、降低其认知与操作负担的、受治理的个人认知助手。

**当前状态:Phase 2 已完成 ✅**
```text
Brain Agent 编排中枢三件套已落地:
  R098 LLM 起草提案 · R102 outbox 触发扩展 · R103 外部成果回流整合
```

**当前唯一开发重点(Phase 3 推进中)**
```text
SOP 与自演化数据层 —— 让 Brain Agent 从 Owner 反复交互中发现模式、生成候选 SOP、委派技能。
  → R099 已完成,建议下一项:R100 SOP 候选生成
```

**并行的 meta 工作**
```text
M0 文档收敛 —— 已完成:建立本 HUB 为唯一文档,旧 13 份已归档。
```

> 铁规:不在"当前重点"里的需求,再合理也先进 §3 排队,不插队动手。这是上次过度工程的教训。

**阶段门槛(go criteria — 满足才进下一阶段)**
```text
判断尺度:以"体感"为准 —— 不看做了多少功能,只看 Owner 是否真的因此减负。
每次跨阶段前,Owner 用下面这条自问,答"是"才放行,答"不确定"就停在本阶段继续打磨。

Phase 1 → 2 放行(认知深度):
  自问:主脑现在是否真的记住了跨会话的事、不用我反复重新交代?
  体感信号:我问系统现状能直接答;上下文重建的次数明显下降。

Phase 2 → 3 放行(编排中枢):
  自问:主脑是否真的成了我和外部 AI 之间的统一接口、少了我手动搬运?
  体感信号:主脑起草的提案我愿意采纳;外部成果能回流、不用我手动同步理解。

Phase 3 → 北极星持续逼近(自演化数据层):
  自问:系统是否真的从我的重复行为里长出了省事的 SOP/技能?
  体感信号:重复的活越来越多被沉淀复用;我的操作负担在下降而非上升。

配套刹车:任一阶段若"体感是负担增加而非减少",不进下一阶段,回到 §3 用 kill criteria 收窄或暂停。
```

---

## 2. 进度看板

### ✅ 已完成 (done)
```text
请求系统    request_id/type 分离 · Request Envelope · request_types.v1 规则源(已落地)
R085        方向记录 / 决策记录(记忆 v0)
R089        技能注册表(只读声明)
R090        外部需求 outbox 模式
R091        Brain Agent v1 协调器
R092        Brain Agent 接入 LLM(默认 DeepSeek)
R093        Brain Agent 问答 (brain think --question,可交互问答)            [Phase 1]
R094        Brain Agent 跨会话工作记忆 (brain memory)        commit bd0d6e1  [Phase 1]
R095        Brain Agent FSM 状态接入                          commit bd0d6e1  [Phase 1]
R096        原生 tkinter dashboard GUI (CLI 已有 gui 命令)     commit 909e4e9
R097        工作记忆衰减机制(指数衰减/半衰期6h/kind权重/阈值/archive) commit 81bfc24
M0          开发文档收敛(本 HUB + 归档)
R098        LLM 起草提案(brain draft)·brain_proposal.py·brain_propose.md·schema     commit verified
R102        outbox 触发扩展(冷却2h/template_id去重/stale_owner触发/changeset_checkpoint触发)
R103        外部成果回流整合(brain integrate:fulfillment→integration card→working memory)
→ Phase 1(Brain Agent 认知深度)已全部完成。
→ Phase 2(Brain Agent 编排中枢)已全部完成。
```

### 🚧 进行中 / 下一个
```text
Phase 3 推进中:R099 已完成,建议下一项 R100 SOP 候选生成
```

### 📋 已排期 (见 §3)
```text
Phase 3:    R100 SOP 候选 · R101 技能注册表 v1   (R099 ✅ 已完成 / R098/R102/R103 ✅ 已完成)
基础设施:    INF-1 Insight v0 · INF-2 Git 安全自动化 · INF-3 Obsidian 桥
数据层:      MEM-1 记忆分层(衰减部分已由 R097 落地)· MEM-2 记忆记录 schema
代码健康:    M-001/002/003/006/007/008(走 Git PR)
抗熵机制:    AE-1 change budget · AE-2 incident→regression · AE-3 风险分层
```

### 🧊 已冻结 / 已作废 (不要再投入)
```text
R080-R084   Implementation Agent 自修改链(JSON changeset / patch_compiler /
            多层 preflight / 自动恢复)—— 永久冻结。
            代码保留仅作:审计证据 + 反面教材 + 可复用零件。
            复活前提:任何提案须先解释凭什么突破 6% apply 基准。
M-004/M-005  共享 fenced-block parser / agent_runner 拆分 —— 主要服务自修改链,
            随之降级;仅当被 Brain Agent 复用时才重新评估。
```

---

## 3. 需求清单(已从 13 份文档抽取、去重、按当前方向筛选)

> 格式:`[ID] 标题 — 目标 / 来源 / 红线(kill criteria)`
> **每条需求必须带可证伪的止损红线**——这是防止再次过度工程的硬规定。
> 与当前方向冲突或纯服务已冻结自修改链的需求,已剔除,不在此列。

### A 组 · Brain Agent 认知深度(Phase 1 — ✅ 全部完成,见 §2 done)
```text
[R093] ✅ 问答 (brain think --question)         无状态交互问答。来源:Corrected Path §5 L1。
[R094] ✅ 跨会话持久工作记忆 (brain memory)       commit bd0d6e1。来源:Corrected Path §5 L2 + 个人助理愿景 §4。
[R095] ✅ FSM 状态接入                            commit bd0d6e1。来源:Corrected Path §5 L3。
```

### B 组 · Brain Agent 作为编排中枢(Phase 2,当前焦点)
```text
注:R096/R097 编号已被实际开发占用 —— R096 = tkinter GUI(909e4e9),R097 = 工作记忆衰减(81bfc24),
    均已完成(见 §2 done)。故本组原"outbox 触发扩展/外部成果回流"顺延为 R102/R103,避免编号冲突。

[R098] ✅ LLM 起草提案        Brain 起草候选提案,Owner 审批(绝不自批)。已完成(brain draft 实测通过)。
                          红线:提案 Owner 采纳率 < 30% → 暂停。
                          增熵约束(生成端治理):起草任一"新增/扩展"类提案前,必须先评估是否存在
                          "砍掉/简化现有"的替代方案达成同样目的;有则优先起草后者。Brain 默认倾向=减法。
                          (注:不设"砍/加比例"自动红线——分类主观+阈值拍脑袋+监控本身增熵,违反薄内核;
                           方向漂移靠 §6 决策日志人工感知,不固化为自动阈值。)
[R102] ✅ outbox 触发扩展      更多需求类型 + 更聪明的触发判断。已完成:冷却机制(template_id 去重,2h 窗口)+
                          新触发(stale_owner_pending ≥ 3 · changeset_checkpoint 近1h applied)。红线:误触发率高于人工登记 → 收窄。
[R103] ✅ 外部成果回流整合      读回 PR/外部结果,压成 feedback card,更新自身理解(闭环关键)。已完成:
                          brain integrate CLI · fulfillment→integration_card→working_memory 全链路。
                          红线:整合后理解与实际代码漂移 → 暂停,先补 cognition 校验。
```

### C 组 · SOP 与自演化数据层(Phase 3)
```text
[R099] 重复模式识别 ✅   从 Owner 反复交互里发现可沉淀模式。红线:识别噪声多于价值 → 停。
[R100] SOP 候选生成        只生成候选,不自动固化。红线:候选需 Owner 二次确认率过低则无意义 → 停。
[R101] 技能注册表 v1       执行委派给外部工具。红线:委派不比直接调用省事 → 停留在 v0 声明。
```

### INF 组 · 基础设施(支撑 Brain Agent,Global Brief 能力顺序里仍有效的部分)
```text
[INF-1] Abyss Insight v0    只读系统状态快照层(活跃 workflow / 完成 / 阻塞 / 完整性)。
                          目标:给 Brain Agent 提供事实依据,而非只靠文档。红线:快照与真实状态不一致 → 先修准确性再扩展。
[INF-2] Git 安全自动化 v0   status/diff 摘要 + checkpoint 建议 + 生成 commit message + Owner 批准后本地 commit。
                          来源:Global Brief §10。边界:禁止 auto-push / 改历史 / 混合系统仓与数据仓。
                          红线:出现一次未经批准的写操作 → 立即停用。
[INF-3] Obsidian/user_data 桥  把已接受的方向记录/决策/工作摘要同步进个人知识层。
                          边界:原始模型输出/失败草稿/噪声日志不得自动提升。红线:私有数据越界暴露 → 停。
```

### MEM 组 · 记忆数据层(个人助理愿景 §4 的可落地部分)
```text
[MEM-1] 记忆分层      L0 当前任务→L5 核心价值边界;默认不是"全记",而是 观察→候选→确认→用→强化→抽象→衰减→归档。
                    ⚠️ 衰减机制已由 R097 落地(指数衰减/半衰期6h/kind权重/阈值/archive),勿重复开发。
                    本项剩余范围:仅"L0-L5 分层"部分(衰减以外)。红线:分层导致检索更复杂而非更清晰 → 停。
[MEM-2] 记忆记录 schema     字段:content/source/evidence/confidence/sensitivity/created_at/last_used/
                          use_count/owner_confirmed/contradicted_by/expires_at/status。
                          红线:schema 太重导致没人愿意记 → 砍到最小必填字段。
```

### AE 组 · 抗熵机制(Minimal Anti-Entropy Kernel,轻量优先)
```text
[AE-1] change budget 模板    每个 AI 改动前声明:allowed_paths / forbidden_paths / max_files /
                          schema_change_allowed / governance_change_allowed 等。防止小修变大改。
                          红线:模板比改动本身还累 → 简化为"只声明 allowed_paths + max_files"。
[AE-2] incident→regression  可复现或高风险事故,必须转成 test-scaffold 里的永久回归测试。来源:抗熵内核 §7。
[AE-3] 风险分层处理          low-risk 轻量 / 工程改动 走 change budget + 测试 / 治理核心改动 走 §5 升级。
```

### M 组 · 代码健康维护(走 Git PR,非自修改)
```text
[M-001] integrity 检查模块化拆分        [M-002] Context Broker 任务检测改结构化规则
[M-003] workflow_tick 拆成显式状态处理器  [M-006] 抽取共享 repo path policy
[M-007] CLI parser 注册模块化            [M-008] 加最小 style/lint guardrails
来源:Source Code Maintenance Roadmap。统一红线:任一项 PR 超出 change budget 范围 → 拆小重提。
（M-004/M-005 已降级,见 §2 冻结区）
```

### 杂项 inbox(想清楚再升级为带 ID+红线 的正式项)
```text
- 把 6%/166 失败数据固化成 harness 一条"已证伪路径"禁令 + 基准线
- 把冻结系统的 workflow 引擎 / context broker 剥离给 Brain Agent 复用(评估范围)
- 规则发布/pull 机制:让标准写一次入 rules/ 后被各模块 pull(请求系统已部分实现)
```

---

## 4. 不可动摇的边界(从宪法/治理/抗熵浓缩;改这些须走 §5)

```text
1. Owner 是最终权威。LLM / Agent / 外部 AI 输出都只是"候选材料",不是事实、批准或动作(candidate before accepted)。
2. Brain Agent 只认知/协调/分解/对齐/整合,不执行、不审批、不绕过护栏、不自授权、不开无限循环。
3. 外部 AI 是可替换的专家资源,不拥有方向、记忆、治理、执行权;不得假设缺失上下文、不得臆造文件内容。
4. 内核只通过 Git PR 演化;数据层(记忆/SOP/技能)在治理下成长。自演化 = 数据层成长,≠ 源码自改写。
5. 任何有意义的改动:可观测、可审计、可回滚、可审查。
6. 治理核心面(见下)的改动 = meta-governance 请求,需 Owner 显式审查 + 延迟激活 + 旧规则比对 + 回滚预案。
```

**治理核心受保护面(protected surfaces)**
```text
Self Evolution · Harness · Owner approval · 权限边界 · 记忆写入/提升策略 · 上下文披露策略 ·
Git 权限 · 外部 AI 权限 · 请求生命周期规则 · ABYSS.md/宪法级规则 ·
rules/policy.yaml · rules/governance.yaml · rules/system_brief.yaml · 定义变更/批准/权限的 contracts
```

**权限分层(主权薄内核战略,L0 最松 → L10 最严)**
```text
L0-L2 对话/读取 可较自动 | L3-L4 建/改文件 需 scope+diff 预览 | L5 跑命令 需说明+风险 |
L6 本地 commit 需 Owner 批准 | L7 user_data 需溯源/隐私检查 | L8 更广目录 默认拒绝(临时授权) |
L9 浏览器/办公系统 需人工认证 | L10 破坏性操作 一般禁止或强确认
判断规则:决定"Abyss 是什么"的 → 主权,自己拥有;只是"帮 Abyss 做事"的 → 能力,可经 adapter 借用。
```

---

## 5. 外部 AI 协作契约(归并自 External Developer Protocol + Brain Agent v0)

**外部 AI 必读切入顺序**
```text
本 HUD(§1/§4/§5 + §3 相关需求) → ABYSS.md → 宪法 → rules/system_brief.yaml →
SYSTEM_MAP.md → rules/modules.yaml → 相关 contracts(仅契约级工作时)→ 源码(仅需实现/验证时)
```

**外部 AI 必须遵守的治理路径(任何有意义的改动)**
```text
proposal → approval → workflow → ChangeSet → validation → Harness review →
Owner approval → executor apply → report
（当前内核改动等价走:Issue → 外部 AI 出 PR → CI(abyss check / compileall / summary --check)→ Owner review → merge）
```

**外部 AI 必须用的返回格式**
```text
task_understanding / modules_touched / files_touched / proposed_changes /
validation_performed / risk_assessment(low|medium|high) / architecture_alignment /
cognition_update_required(yes|no) + minimum_disclosure_layer / open_questions / recommended_next_step
```

**外部 AI 禁止**
```text
自批/自执行 · 绕过 Harness/Owner · 扩展 agent 权限 · 改治理规则 · 假设缺失上下文 ·
把候选输出当已接受 · 大范围无关重写 · 同步密钥/token · 把高风险建议当可直接实施
高风险(治理/执行/权限/自动化扩展/删数据/跨仓状态变更)一律上交 Owner。
```

**升级流程(碰治理核心面时)**
```text
声明为 governance-core change → 提供 旧规则比对 + 风险评估 + 验证计划 + 回滚预案 →
Owner 显式审查 → 治理语义变更时延迟激活 → 通过后才生效。
```

---

## 6. 决策日志 (append-only,只增不改)

```text
2026-06-30  冻结 Implementation Agent 自修改链(6% 成功率);内核改走 Git PR(原 Corrected Development Path)。
2026-06-30  建立本 HUB 为唯一现行文档;13 份旧规划文档全部归档至 archive/;可用需求已抽取并入 §3。
2026-06-30  对照代码/提交历史核实并修正 5 处漂移:R093/094/095(已完成,Phase 1 收官)移入 done;
            R096=GUI(909e4e9)、R097=记忆衰减(81bfc24) 已占用编号并完成;原 B 组描述顺延为 R102/R103;
            MEM-1 衰减部分标注已由 R097 落地;当前焦点更新为 Phase 2(建议 R098)。
2026-06-30  R098 补增熵约束:采用生成端治理(Brain 默认减法,扩张类提案须先找简化替代);
            明确否决"砍/加比例"自动红线(自身增熵、违反薄内核);方向漂移靠 §6 人工感知。
2026-06-30  R098 实现完成:新增 brain_proposal.py(brain draft CLI)· brain_propose.md prompt ·
            brain_proposal.v1.schema.json。Brain 调 LLM 起草候选提案,经解析+归一化+校验后
            写入 .local/runtime/process/brain_proposals/。candidate_material_only=True,
            no_approval_granted=True。待 Owner 实测验收后正式移入 done。
2026-06-30  R098 实测验收通过:brain draft 命令成功调用 DeepSeek,生成结构化提案(本次为 no_action —— 
            系统稳定时 Brain 正确判定无需改动),validation=PASS,anti-entropy 减法约束生效。
            R098 正式移入 done;下一开发重点更新为 R102 outbox 触发扩展。
2026-07-01  R102 实现完成:扩展 external_adapters.yaml 新增 2 个触发模板(notify_owner_on_stale_pending_items ·
            checkpoint_after_changeset)。brain.py _evaluate_triggers 重构:冷却机制(_is_in_cooldown,
            TRIGGER_COOLDOWN_HOURS=2.0,按 template_id 跨全状态去重替代旧 type-only pending 检查);
            新增 _check_stale_owner_items(≥3 pending 触发)+ _check_recent_changeset_applied(近1h applied 触发)。
            brain_tick 移除 needs_skipped(冷却在 _evaluate_triggers 内部过滤)。实测:触发→冷却生效→registry check PASS。
2026-07-01  R103 实现完成:新增 brain_integrate() · _assess_fulfillment() · render_brain_integrate_json()。
            闭环:fulfilled needs → read_fulfillment → integration_card(abyss.integration_card.v1,写 feedback_cards/)
            → save_working_memory_entry(写 working_memory/)。确定性评估:error/success 信号检测 + 类型特定 notes。
            CLI:brain integrate 子命令注册。实测:模拟 fulfilled need → integrate → integration card + working memory
            均正确生成,working memory 中可检索到整合记录。测试数据已清理。
            R102/R103 正式移入 done;Phase 2(Brain Agent 编排中枢)收官;下一开发重点更新为 Phase 3 R099 模式识别。
2026-07-01  §1 新增"阶段门槛(go criteria)"小节:为三个 Phase 各定一条"体感为准"放行标准
            (以 Owner 是否真的减负判断,不设硬指标),与单需求 kill criteria 形成"刹车+油门"配套。
2026-07-02  R099 实现完成:新增 brain_patterns() · 5 个确定性检测器 · render_brain_patterns_json()。
            5 个检测器:topic_frequency(brain_responses 关键词)· proposal_type_distribution(brain_proposal 类型)
            · owner_decision_pattern(owner_inbox 决策)· trigger_frequency(outbox template_id)· assessment_repeat(assessment 指纹)。
            纯确定性,无 LLM。生成 candidate_insights(advisory only) + noise_risk 评估。
            CLI:brain patterns [--json] 子命令注册。实测:5 个检测器正确运行,
            检出 10 个 topic 关键词 · 3 种 proposal 类型 · 1 个 owner 决策模式 · noise_risk=low。
            abyss check / compileall / summary --check 全绿。
            R099 正式移入 done;Phase 3 首项完成;下一开发重点更新为 R100 SOP 候选生成。
```

---

## 7. 归档索引(13 份旧文档去哪了 / 其精华吸收到哪)

> 全部位于 `archive/`。需要追溯原始论证时再查;日常开发不必读。

```text
Corrected Development Path 2026-06-30.md   冻结决定+Git PR 模型   → 已并入 §1/§2/§4/§5
Global Direction Brief.md                  §1-16 规则+能力顺序     → 边界并入 §4、基础设施并入 §3 INF 组(§17 已作废)
Vision.md                                  五大架构+原始迁移阶段   → 架构观念为背景;迁移阶段已被本 HUB 取代
Brain Agent v0.md                          Brain 角色能做/不能做   → 并入 §4(2) + §5
External Developer Protocol.md             外部 AI 协作+返回格式   → 并入 §5
Meta Self-Evolution Governance.md          治理核心面+升级流程     → 并入 §4 protected surfaces + §5 升级流程
Sovereign Thin Kernel ... Strategy.md      主权薄内核+权限分层L0-10 → 并入 §1 定位 + §4 权限分层
Minimal Anti-Entropy Kernel.md             抗熵五件套+change budget → 并入 §3 AE 组 + §4
Personal Cognitive Assistant Vision.md     北极星+记忆分层/衰减     → 并入 §1 北极星 + §3 MEM 组
Standardized Request System ...md          request 语义+发布机制    → 大部分已实现(§2 done);余项进 §3 inbox
Source Code Maintenance Roadmap ...md       M-001~M-008 维护项      → 并入 §3 M 组(M-004/005 降级)
Archive - Vision Before Development Plan    历史快照                → 纯历史,可忽略
Archive - Vision Discussion                 历史快照                → 纯历史,可忽略
Archive - Vision Expanded Mainline          历史快照                → 纯历史,可忽略
```

---

_维护提示:本文件保持精简,只承载"重点/进度/需求/边界/协作/决策"。详细原始论证留在 archive/;不要把它重新养成一堆散文档。_
�成一堆散文档。_
只承载"重点/进度/需求/边界/协作/决策"。详细原始论证留在 archive/;不要把它重新养成一堆散文档。_
