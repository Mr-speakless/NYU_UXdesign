# User Journey Map — Lucas

## 用户、情境与目标

- **用户（Actor）：** Lucas，参与 AI 影视制作的创作者；此图只呈现他的个人经历，不代表团队统一流程。
- **情境（Scenario）：** Lucas 收到分阶段的 art treatment 和镜头分工后，为一个 shot 准备项目资料、casting 和 still，生成视频候选，接收 Frame 评审并修改。
- **目标（Goal）：** 交付 art director 批准、剪辑师可继续使用的 shot，同时保留足够的生成上下文，以便需要时回溯和修改。
- **预期（Expectations）：** 项目背景和 shot 要求可复用；stills 与视频候选能追溯到来源、prompt、模式和参数；收到评审意见后能定位要修改的环节。
- **旅程范围：** 从收到本批任务与 art treatment 开始，到镜头通过评审并交接，或根据反馈回到相应环节继续修改。**本任务和Henry的Journey Map相比更加只聚焦在视频和图片生成的环节上，相对而言更加聚焦。**

本图参照 Nielsen Norman Group 的 [Journey Mapping 101](https://www.nngroup.com/articles/journey-mapping-101/) 组织：一个具体 actor 与情境，配合高层阶段中的行动、想法/需求、情绪和改进机会。阶段归纳 Lucas 的整个镜头制作经历，不是每一次点击或生成操作的逐步日志。访谈内容由采访者复述；表格中的想法是研究者归纳的问题，不是逐字引语。

## Lucas 的当前旅程

情绪估值使用 **1（困难/负向）到 5（顺畅/正向）** 的方向性刻度。Lucas 没有给情绪打分；数值是根据访谈内容推断的研究估计，不是量化测量。

| 阶段 | 接触点与阻碍 | Lucas 的行动 | 想法与需求 | 情绪估计 | 改进机会 |
|---|---|---|---|---|---|
| **1. 接收批次与方向** | Art treatment、leader、客户决策和镜头分工。项目按批次推进；后续批次可能沿用、改变或推翻早期工作。背景资料可能保留，但 prompt 和 still 经常需要调整。（Lucas） | 接收 art treatment 和分配的镜头，确认当前批次交付范围；客户需求还没确定的镜头先等待。 | 现在哪些镜头已经可以做？哪些应该等客户决定？如果下一批改变方向，之前哪些内容可以保留？ | **2.5/5** — 批次范围和方向可能变化。（推断） | 清楚标出当前批次、待确认决定和可复用的项目背景，方便 Lucas 从正确的范围开始制作。 |
| **2. 建立项目上下文** | Claude、本地文件夹、Project Setting、scene/shot 文件夹。Lucas 估计整理一个干净的项目包约需 2–3 小时；经常需要重复性介绍项目和文件夹的用法。（Lucas） | 使用 Claude 提取 art treatment 中的镜头指导和参考图，整理 Project Setting、batch、scene 和 shot 文件夹，并把固定要求放在对应镜头下。 | Claude 是否理解整个项目、单个镜头及输入素材的位置？使用它之前还需要准备和说明多少内容？ | **2.5/5** — 资料整理后更有序，但前置设置负担较重。（推断） | 让项目背景和 shot 文件结构可以复用，减少重复说明及准备 Claude 输入所花的时间。 |
| **3. 准备 Casting 与 still 输入** | Nano Banana、Kling Elements、ComfyUI、客户真实场景图片、art treatment 参考。角色 casting 可上传为 Kling Elements 后用 `@` 引用；其他参考仍需手动放入 ComfyUI。（Lucas） | 用 Nano Banana 生成人物面部和全身三视图，并上传到 Kling Elements。再把角色、客户真实场景、art treatment 构图参考和 shot brief 组合到 ComfyUI，准备 still。 | 人物、客户真实环境、art treatment 参考和 shot brief 是否在 still 里协调一致？ | **3.5/5** — casting 和关键输入准备好后，更有把握继续制作。（推断） | 在 still 制作时把 casting、客户真实场景、art treatment 参考和 shot brief 一起查看，避免手动找素材和处理参考冲突。 |
| **4. 生成与细调 Still** | ComfyUI、raw assets、still 候选和节点参数。重开生成图可以找回设置，但需要手动回溯；从 raw 重新抽样会耗时，图生图更快但可能损失画质。（Lucas） | 检查人物、真实环境、构图、光线和 Novi 风格；挑选 still，或从 raw 素材重做、基于已选图片进行图生图修改。 | 问题来自素材、构图、prompt 还是生成方式？怎样从产生当前版本的准确输入继续修改？ | **2.5/5** — 选择和细调需要反复尝试，也要在时间与画质间权衡。（推断） | 让选中的 still 保留与 raw 输入及 ComfyUI 设置的关联；支持从原始素材重做或基于选中图修改，并保留版本关系。 |
| **5. 评审与定位问题** | Claude、Kling AI、共享生成账户、Frame、art director。视频模式包括首帧、首尾帧和 Omni；共享账户同时最多运行 20 条视频生成，超出任务排队。候选与 prompt、still、模式和参数有时分开保存。（Lucas） | 让 Claude 基于项目背景、Novi style、shot brief 和 still 扩写视频 prompt；测试不同视频模式，分批生成并比较候选，再上传选中的视频到 Frame。 | 哪种模式和 prompt 产生了这个候选？能否比较不同分支，同时保留每个候选的输入和设置？ | **2/5** — 分支多、生成有随机性，候选和来源不易追踪。（推断） | 把每个视频候选与对应 still、逐镜头 prompt、Kling 模式和设置关联；让共享生成队列状态可见。 |
| **6. 修改并交接** | Frame、ComfyUI、Kling 历史、本地文件夹和剪辑交接。评审意见简短，Lucas 需要判断要回到哪一步；替换后的 still 可能和最新视频版本脱节。（Lucas） | 阅读 art director 的通过或修改意见，判断问题来自 still/source、prompt、motion、mode 或 settings。通过后选定版本交给剪辑；未通过则回到相应环节重新生成并提交。 | Frame 意见具体对应哪个输入？替换一项素材时，怎样保留仍然有效的部分并继续迭代？ | **2.5/5** — 通过后有推进感；返工时仍要自行诊断根因。（推断） | 让评审意见指向具体候选及其来源，并帮助定位应修改 still、prompt 还是生成模式。 |

## 旅程中的机会重点

1. **减少前置重复说明：** 让项目 context 和常用文件结构能够被后续 batch 复用。
2. **保持素材到结果的关联：** 将 casting、场景参考、still、逐镜头 prompt、生成模式、参数和视频候选连在一起。
3. **支持从有效版本继续：** 可以从 still 或视频候选回到它的输入和设置，并沿用仍然有效的内容。
4. **让反馈更容易转成下一步：** 将 Frame 短评关联到准确候选，并区分需要修改的是 still/source、prompt/motion 还是模式/参数。

这些是根据当前旅程识别的机会，并非已验证的产品功能。Lucas 目前没有系统记录不同难度 shot 的全流程时间、stills 数量或迭代次数；若要衡量改善，应先记录代表性镜头的准备时间、回溯次数和返工原因。

## 证据与边界

- 行动、工具、批次组织和平台限制来自 Lucas 的访谈补档及追问回答；记录是采访者复述，不是逐字稿。
- 想法/需求由访谈描述归纳；情绪分值是研究者估计，不是 Lucas 自评。
- Claude 文件整理、Casting 工作流、目录结构和生成习惯均为 Lucas 的个人做法，不应视为团队标准。
- Omni 时长/镜头数和共享账户并发限制，是 Lucas 对其工作环境的描述，未独立核验。

## 参考

- Sarah Gibbons, Nielsen Norman Group, [Journey Mapping 101](https://www.nngroup.com/articles/journey-mapping-101/), 2018（页面于 2026-07-15 reviewed）。
- Week 2《访谈记录 04：Lucas（个人工作流补档）》及追访回答。
