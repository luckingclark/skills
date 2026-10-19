# Skills

用于整理、分享和安装 AI 技能的仓库。每项技能放在独立目录中，以 `SKILL.md` 为入口，配套文件随目录一并保存。

目前包含 `leader`：将需求整理为目标清楚、背景充分、步骤可执行、结果可核查的任务书，供本地 AI 执行者或网页版模型使用。

`leader` 基于 [KKKKhazix/khazix-skills 中的 leader](https://github.com/KKKKhazix/khazix-skills/tree/main/leader) 修改。README 的用途说明、目标要素与使用流程参考了[原仓库 README 的 leader 部分](https://github.com/KKKKhazix/khazix-skills/blob/main/README.md)，并按本版本的实际行为重新编写。具体调整见 [leader 的修改说明](leader/README.md#相对于原版的主要调整)。

## 技能目录

| 技能 | 用途 | 使用说明 | 指令入口 |
|---|---|---|---|
| `leader` | 需求澄清、目标拆解、研究任务规划与可复制提示词编制 | [leader 使用说明](leader/README.md) | [SKILL.md](leader/SKILL.md) |

## 安装与调用

在具备技能安装能力的 Codex 环境中，可以发送：

```text
请安装这个技能：
https://github.com/luckingclark/skills/tree/main/leader
```

安装来源是本仓库的 `leader` 目录。请完整保留其中的 `references/`，不能仅复制 `SKILL.md`。安装后，在环境识别到该技能的对话中调用：

```text
使用 leader，帮我整理以下需求并拆解目标：
……
```

需要交给无法访问本地资料的网页版模型时，可以补充：

```text
目标执行环境是网页版模型，不能读取本地文件或技能。
请先读取我提供的材料，再将执行所需的事实、约束和说明直接融入任务书。
正文不引用本地文件名、路径或技能名称。
请采用严谨、清楚的书面表达，并给出可直接复制的完整任务书。
```

详细的手动安装方法、输入建议和使用示例见 [leader 使用说明](leader/README.md)。

## leader 的工作方式

`leader` 先识别任务类型、执行环境和已有材料，再整理目标、范围、工作依赖、交付物与完成条件。仅在缺少的信息会实质改变任务时提出必要问题。

- **书面表达**：措辞准确、清楚，避免口语化决策用语与夸张承诺。
- **背景自足**：面向无法访问本地材料的执行者，直接提供必要内容。
- **范围准确**：示例用于说明深度或格式，不自动成为研究范围的边界。
- **方法适配**：分别处理实施、研究及混合任务的步骤和验收方式。
- **证据明确**：区分事实、默认假设、待核实信息及实际验证结果。

产出是一份可复制的 Markdown 任务书。任务书编制完成后，将其交给目标执行者；实际执行能力取决于所用环境、工具和已授予的权限。

## 仓库结构

```text
skills/
├── README.md
└── leader/
    ├── README.md
    ├── SKILL.md
    ├── LICENSE
    └── references/
        ├── anatomy.md
        └── style.md
```

后续技能可采用同样的独立目录结构，并在各自说明中注明来源、使用方法与适用许可。
