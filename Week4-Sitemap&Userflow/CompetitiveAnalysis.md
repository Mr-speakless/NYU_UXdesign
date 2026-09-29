# AI 影视创作平台竞品分析

> **研究日期：** 2026-09-28  
> **研究对象：** 可灵 AI、Seedance Canvas（Dreamina）、FLORA、Weavy（现 Figma Weave）、Runway

本分析聚焦 AI 影像创作中的工作流：创作者如何组织镜头与素材、批量生成和筛选结果、回看生成依据，以及与团队成员协作。内容综合官方产品资料与补充的实际使用观察；官方未说明或尚未体验确认的部分会保留为待确认。

## 快速比较

|  | [可灵 AI](https://klingai.com/) | [Seedance Canvas / Dreamina](https://dreamina.capcut.com/ai-video/ai-creative-workspace) | [FLORA](https://flora.ai/product-canvas) | [Weavy / Figma Weave](https://www.figma.com/weave/) | [Runway](https://runwayml.com/) |
|---|---|---|---|---|---|
| **切入方式** | 以自有图像、视频模型为核心的创作平台，并提供创作广场和灵动画布。 | 将多模态创作放进共享 Canvas；Seedance 是其中的视频生成模型。 | 以无限画布和节点连接组织多模型创作流程。 | 以节点画布搭建、批量运行并复用生成工作流。 | 以 Projects 为项目空间，通过 Agent、Sessions、Workflows 和 Assets 完成创作。 |
| **功能 / 工作流程** | 生成图片与视频，使用参考图控制主体；可用故事板规划镜头。创作广场可回看历史图片与提示词；体验中创作广场最多同时生成 3 条视频，灵动画布约可并行生成 3–5 个镜头。 | 在节点中放入输入素材，连接图像与视频生成；支持批量生成，重试时点击生成按钮重新运行。 | 在画布中连接文本、图片、视频和编辑节点；Elements 可复用主体或风格，Batch Node 可将操作用于多个输入；有基础评论。 | 用文本、图片、视频迭代器批量运行节点；工作流可封装成 Tool 分享和复用。 | 在 Project 下开启多个并行 Agent Session；每个 Session 是一次 Agent 操作工作流和素材的创作对话。Assets 可集中管理，生成内容可回看。 |
| **优势** | 生成、故事板与参考素材控制相连；可回看历史生成，已选结果可追溯生成依据并复用角色素材；支持多镜头并行探索。 | 图片、视频和参考素材能在同一画布中衔接；可批量探索方案，生成失败或不满意时可直接重新运行。 | 流程与生成关系可视化；支持多模态节点、一定程度的批量处理及素材复用。 | 批量输入和工作流复用能力明确；复杂流程可封装成较简单的 Tool，供他人使用。 | 项目内的多轮 Agent 对话、工作流和集中素材管理形成连续的创作空间；可回看生成内容，便于从先前工作继续。 |
| **局限 / 不足** | 缺少项目级归类和管理能力。一切镜头都是平级且线形排列。 | 节点输入无法从生成结果反向追溯 | 画布内容增多后导航困难；批量结果不能溯源；按镜头筛选功能未见支持。 | 不支持实时共同编辑和针对输出的团队评审；生成结果需要手动下载、归档。 | Projects、Sessions 与 Assets 提供项目和素材组织。但复杂的项目与镜头组织没有对应管理工具。 |
| **设计机会** | 在生成记录之上补充镜头任务、团队评审、选择决策和接手人，让创作历史成为可协作的项目记录。建立更系统的项目管理系统（类似于Windows的文件管理器） | 保留批量生成效率，同时让每个结果都能回到对应提示词、参考素材和参数，并便于比较、选择与继续修改。 | 简化大型画布的导航；增加按镜头筛选、结果溯源和明确的审批状态，同时保留节点流程的灵活性。 | 为工作流和输出增加轻量协作、在线归档与版本关联，减少依赖个人下载整理。 | 将 Agent 的生成会话和集中素材进一步关联到镜头、素材。同时可以从镜头作为分类单元而不是只有session进行管理。 |

## 主要发现

1. **生成历史不等于完整溯源。** 可灵和 Runway 都能回看生成内容；Dreamina、FLORA 的节点式流程能展示输入与输出的关系，但补充体验显示，结果未必能反向找到其输入。稳定关联“镜头—提示词—参考素材—参数—结果”仍有价值。
2. **批量生成让筛选和归档变成关键步骤。** Dreamina、FLORA 和 Weave 支持不同形式的批量工作；生成数量增加后，需要快速比较、标记入选版本，并保留每个结果的来源。
3. **画布适合创作探索，团队还需要项目秩序。** 节点画布可以呈现创意分支，但团队协作还需要负责人、评审状态、决策理由和交接信息。可灵的生成能力与 FLORA、Weave 的流程能力都不能单独覆盖这些团队需求；Runway 提供项目组织和 Agent 协作，但镜头级关联仍值得确认。
4. **可复用流程和可接续的镜头工作可以并存。** Weave 擅长把流程封装成 Tool；Runway 以 Project 和 Session 组织 AI 协作。面向影视团队，可以把可复用的生成步骤与每个镜头的 brief、素材、候选和评审记录放在一起。

## 资料来源

### 官方资料

- [快手：可灵 AI 3.0 系列上线公告](https://ir.kuaishou.com/zh-hans/node/11216/pdf)
- [快手：可灵 AI 灵动画布公告](https://ir.kuaishou.com/static-files/7d551be0-8fff-43b0-a280-16d0b51f5f54)
- [Dreamina：AI Creative Workspace](https://dreamina.capcut.com/ai-video/ai-creative-workspace)
- [Dreamina：Seedance 2.0 多模态视频生成](https://dreamina.capcut.com/tools/seedance-2-0)
- [FLORA：Canvas 产品页](https://flora.ai/product-canvas)；[Canvas 文档](https://docs.flora.ai/editor/canvas)；[Batch Node 更新说明](https://flora.ai/updates/layer-editor-batch-node-and-little-big-updates)
- [Weave：节点说明](https://help.weavy.ai/en/articles/12292386-understanding-nodes)；[迭代器与批量生成](https://help.weavy.ai/en/articles/12343281-iterators)；[Tools、分享和版本管理](https://help.weavy.ai/en/articles/12267755-tools)
- [Runway：Projects](https://help.runwayml.com/hc/en-us/articles/52474899121555-Introduction-to-Projects)；[Sessions](https://help.runwayml.com/hc/en-us/articles/33545310653203-Generating-with-Sessions)；[Workflows](https://help.runwayml.com/hc/en-us/articles/45763528999699-Introduction-to-Workflows)；[资产管理与分享](https://help.runwayml.com/hc/en-us/articles/25562277393427-How-to-share-an-asset)

### 范围说明

- 可灵创作广场、Dreamina、FLORA、Weave 和 Runway 的具体体验观察来自本次补充记录；平台功能可能因账户、地区和版本不同而变化。
- “设计机会”是根据产品能力和本项目的研究关注点归纳，不代表竞品一定缺少未公开或未体验到的功能。
