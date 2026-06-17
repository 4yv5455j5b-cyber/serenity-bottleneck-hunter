<!-- ticker-verify: skip — 本文件是复盘档案,含"错的例子"示意,跳过 hook 扫描 -->

# Lessons — 翻车档案 / 纪律的由来

> 这里存的是 **SKILL.md 里每条纪律是怎么用一次真实翻车换来的**。
> SKILL.md 负责"做什么"(干净祈使句),本文件负责"为什么"(完整事故 + 代价)。
> 每条带锚点,SKILL.md 用 `〔教训:… → lessons.md#锚点〕` 指过来。
>
> 维护:每次出现新的"用户挑战驱动 / dogfood 翻车 → 催生新纪律",在这里加一条,SKILL.md 只留祈使句 + 指针。

---

## redwire — 广扫供应商,否则漏④原型
**催生规则**:Step 2 "必做广扫供应商:除最上游材料层外,单独再搜一轮子系统/器件/卖铲子供应商"。
**翻车(首跑商业航天,种子期)**:只拆了"材料咽喉"层,漏掉 **Redwire**(ROSA 柔性太阳能阵 / 星敏感器)—— 一个典型的 ④ 普适器件/卖铲子标的。
**代价**:④ 原型是 skill 的半壁江山(卖铲子比材料垄断更常见),只搜材料层等于选股偏科。

---

## breadth-stm — 广扫不到位 ≠ 板块没机会
**催生规则**:Step 2 "每层至少 2-3 个标的,广扫不到位 ≠ 板块没机会"。
**翻车(800VDC 电源半导体)**:v1 只扫了 6 只就下结论"全板块 extended、无机会"。v2 把广扫扩到 15 只,立刻挖出 **STM**(SiC 功率 + MEMS,当时还在健康区间)。
**代价**:"扫得少 → 看着全贵 → 判板块没戏"是个隐性陷阱,真相是猎物没扫到。停手前必须问"是真没机会,还是我没扫够"。

---

## ip-eda-root — 重复 3 家 = 信息熵零,提到 root section
**催生规则**:Step 2 "ARM / CDNS / SNPS 放在 chain-viz 上方独立 'cross-theme root' 小卡片,显示一次,不画进每个主题的产业链层"。
**翻车(IP/EDA 分层冗余,2026-06-02 用户反馈)**:连续 7 份报告的 IP/EDA 层 100% 重复 ARM/CDNS/SNPS 三家 —— 信息熵 = 0,占版面不产生新信息。
**修复**:方案 B+C 混合 —— 通用 root 提取成独立 section;只有主题真有独立 IP 玩家(L4 的 MBLY、AI PC 的 ARM 真单源)才画第 6 层;无独立玩家(AI Agent/物理AI/AMR)不画;不依赖芯片设计的(MLCC/800VDC/航天)完全跳过。

---

## player-census — 已知玩家全集,逐一标记
**催生规则**:Step 2 "每个主题开扫前必须先列已知玩家全集,逐一标 covered/private/acquired/delisted/untracked"。
**翻车背景(2026-06-01)**:候选数集中在 20+ 是一个隐性 stopping rule(扫到差不多就停),不是穷尽广扫。
**示例(自动驾驶 L4 LiDAR 玩家全集)**:Hesai / Luminar / Innoviz / Aeva / Ouster / Velodyne(已合并 OUST)/ Cepton(被 KOEL 收)/ Innovusion(被尼欧买)/ Quanergy(破产)/ RoboSense(港股)/ 速腾 —— 必须显式列全 + 标记,不允许"我扫了 5 家就够了"。

---

## etf-audit — 凭记忆列玩家必漏主仓
**催生规则**:Step 2 "A+ ETF audit 强制:每个新主题开 forward_picks 扫描前必跑 `theme_etf_coverage.py`,top 25 持仓 100% audit"。
**翻车(Dogfood #10 美股 AI Agent,2026-06-02)**:A 项"凭记忆列全集"不够 —— 安全层原仅扫 ZS,漏掉 **PANW**(IGV 主仓 7.38% / CIBR 主仓 10.23%)、**CRWD**(IGV 6.07% / CIBR 10.66%)、**FTNT**(CIBR 8.83%)、**RBRK**(CIBR 1.88%)等 **34 只**,covered 率只有 50%。
**真实损失**:34 只里 32 只已抛物线 ext(漏不漏不改变结论),但 **CHKP**(rng31/off-30%/1m+21%)和 **FICO**(rng42/off-31%/1m+24%)是真正漏掉的 Mode A 候选。
**代价金句**:纪律失败的代价是隐性的 —— 这次只漏 2 个 Mode A 候选,下次可能漏的就是该主题的整个 thesis。

---

## ticker-verify — 凭记忆写 ticker 会错位,thesis 反向
**催生规则**:Step 2 "A++ ticker 双向验证:广扫前 EODHD search 反查代码 ↔ 公司名,禁止凭记忆写 ticker"。
**翻车(Dogfood #12 绿的谐波错标,2026-06-05)**:v3 物理 AI 报告 4 处用 **603297.SHG** 当成"绿的谐波"(谐波减速器),但 603297 实际是 **永新光学(宁波永新)**。真绿的谐波(Leader Harmonious Drive)代码是 **688017.SHG**(科创板)。
**错位影响**:
- 价格:误用 ¥123.74(永新)代替 ¥327.50(真绿的)
- stage:误判"rng49 早期 mid"(永新真状态)代替"rng77 已抛物线"(真绿的)
- **推荐反向**:原报告说"等回 rng<30 再看"(基于永新数据),真实 688017 已 1m+42%/3m+55% 抛物线 —— Mode A 窗口早过,**完全 reverse 判定**
**成因**:中文名"绿的谐波"凭记忆写代码 → 与永新光学的 603297 同样 6 开头沪市主板 → LLM 训练数据混淆。
**连带战绩**:同一套防御后续又追溯抓出 **信质电机**(Dogfood #13,误"长鹰信质"002664)、**ASEKY**(实为爱信精机,误当 ASE 日月光,真 ADR=ASX.US)、**EHGO**(实为 Eshallgo 办公设备,误当亿航,真 ADR=EH.US)。累计 4 个真错位全被 L1+L2+L3 拦截。

---

## theme-scope — 大类主题不声明边界 → 期待 mismatch
**催生规则**:Step 2 "跑大类主题报告顶部必须界定本期边界 + 命名格式 `<大类>_<子领域>_完整分析报告.html`"。
**翻车(物理 AI v1)**:默认"物理 AI = 人形机器人",没声明边界 —— 而物理 AI 含人形/自动驾驶/AMR/无人机/手术等 3+ 个供应链特征差异显著的子领域。用户期待与实际产出 mismatch。

---

## price-interface — 批量拉价必须走 price.py,禁止 inline EODHD
**催生规则**:择时 "批量拉价格必须走 price.py 接口,禁止 PowerShell 直接 `Invoke-RestMethod` 调 EODHD API"。
**翻车(物理 AI 主题 v1,2026-06-01)**:用 inline EODHD 调用,**绕过了 yfinance fallback** —— EODHD 不支持 `.T` 后缀(日股),结果报告漏 4 只日股。
**正确方式**:`python -c "from scripts.price import analyze; print(analyze('6324.T'))"`(走 EODHD→yfinance 完整链),或脚本里 `from scripts.price import fetch_history`。inline API 会跳过回退链。

---

## hand-filled — 手填数字会编一个"看着合理的大数"
**催生规则**:择时 "报告所有数字 100% 来自 price.py 输出,禁止手填/猜数"。
**翻车(dogfood #7 + #8,2026-06-02 用户抓错)**:9 个标的的 `off_6mo_high` 被手填错 —— HSAI 写 -89%(真实 -35.6%)、海康写 -77%(真实 -19%)等。
**成因**:PowerShell 输出里只复制了 `rng/1m/3m`,`off%` 没记录就手填了一个"看着合理的大数字"。
**修复**:批量 scan 脚本输出必须含全 9 字段 + 保留完整 log;写入 forward_picks 前逐字段 verify。手填任何数字 = 流程错误。

---

## chain-viz-required — 网状视图强制必含,不许跳过
**催生规则**:输出模板 "Step2 逆向拆链网状视图强制必含,不允许以'前面画过类似的'为由跳过"。
**翻车(C 项,2026-06-01 用户挑战)**:自动驾驶 L4 / AMR 两份报告漏了 chain-viz 区块,报告残缺。
**关键**:每个子主题的供应链都不同,"画过类似的"不成立。

---

## company-desc-evolution — business/status 拆分的三次迭代
**催生规则**:数据来源 "company_desc.md 只存 business(主营/产业链位置/技术/客户),严禁含 price/stage/估值等动态数据;90 天 freshness"。
**三次迭代(2026-06-02,用户连续挑战)**:
- **v1**:business + price 混在一起 → 用户挑战"price 混入了"
- **v2**:拆成 business(静态)/ status(动态)两段 → 用户挑战"静态的业务重点也会变化"
- **v3**:business 加 `[YYYY-MM-DD]` 时间戳 + 90 天 cache invalidation(超 90 天必须重新评估战略漂移)→ 现行
**工具**:`tracking/check_desc_freshness.py` 输出过期 entry 列表。

---

## company-status — "私有/被收购"状态会过期,写判定前必搜
**催生规则**:Step 2 "公司状态检查:写判定前每只候选搜一次当前状态(收购/IPO/退市);'私有/不可投'是状态性断言必须当场搜证"。
**双向翻车(Dogfood #16 商业航天美股,2026-06-12/13)**:
- **上市→被收走**:SkyWater(美国唯一上市受信 rad-hard 代工,教科书级 ①②⑦)2026-01 被 IonQ $35/股收购 → 瓶颈逻辑瞬间不可投。**被收购反向验证了选股方向**(战略买家与本框架看上同一个瓶颈),应记进报告当佐证;小盘纯 play(FEIM/KRMN 级)天然是并购标的。
- **私有→已上市**:SpaceX 2026-06-12 NASDAQ IPO(SPCX,$1.75T 史上最大),而报告当天还标它"私有不可投"。
**成因**:LLM 对"某某是私有公司"的先验是训练数据快照,极易过期 —— 这正是 business/status 拆分纪律存在的原因(状态进带日期的 status 字段,不进静态 business)。

## cross-theme-aehr — 跨主题 ⭐ 节点首个验证案例
**催生规则**:Step 4 "产出候选后立即跑 cross_theme_scan,同 symbol 跨 ≥2 主题 = ⭐,≥3 = ⭐⭐;档位过滤防巨头摊薄误标"。
**首测(2026-06-01)**:**AEHR.US** 同时出现在光子学 + 800VDC 两个主题(都是上游设备 ⑥⑤)= ⭐ —— 跨 capex cycle 真实存在的第一个确认案例。
**后续新高**:A 股 **鸣志电器 / 步科股份** 跨 4 主题(人形+低空+物理AI+物理AI中国)⭐⭐⁴。
**档位过滤纪律**:中游系统/下游对照/反面参照不计入;中游卖铲子必须有 ④ 普适才计入(避免 STM/NVDA/Vertiv 因业务摊薄被假高亮)。
