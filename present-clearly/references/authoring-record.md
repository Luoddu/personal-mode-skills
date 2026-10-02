# 呈现模式：来源与验证记录

任务：`P0-SKL-001`（个人 Skill 本地任务编号，不属于其他项目的路线图）。日期：2026-10-02。版本：1.0.0。

## 执行约定

- 角色：个人 Skill 作者与本次仓库交付负责人。
- 授权：用户认可执行草稿并明确允许实施；随后允许上传到存放既有个人 Skill 的 GitHub 仓库。
- 目标：论文、汇报和个人思考中的一段呈现稿；正文保留用户立场，必要提醒另列；支持自然与书面程度连续调整。
- 写集：个人 `present-clearly/` 的 `SKILL.md`、`agents/openai.yaml`、本记录；同名公开仓库中的对应三个文件及 README 使用说明。独立 checkout 可保留不进入提交的本机校验器与 Git guard 副本，用于显式路径提交和二次扫描；不作为公开 Skill 的依赖。
- 发布目标：既有公开仓库 `Luoddu/personal-mode-skills`；不改变可见性，不上传整个个人配置目录或既有 Skill 的本机作者记录。
- 非目标：其他 Skill、全局指令、项目治理、运行时接入、模型或权限配置、第三方包安装、自动化、子 Agent。
- 基线：公开仓库 `main@f42d4acb7cd8adcee4a6bb4e5241a1574dcb69a9`；本次目标目录原先不存在，独立 checkout 无修改。写集与其他项目及其 worktree 不重叠，属绿灯。
- 独占资源：新 Skill 目录与本次独立 checkout；无业务 task/run、数据库、端口或服务控制权。
- 预算：一个纯指令 Skill；本机格式与只读发现验证、作者场景审阅；不新增模型评测、子 Agent、依赖或长期进程。技术重试按已查明根因与原授权范围处理；身份或权限失败停止对应发布。
- 复核点：写入前、验证后、提交前及上传前检查目标文件、并发变化、显式文件清单与公开内容范围。
- 回滚：将个人 Skill 目录移出扫描位置并保留副本；公开仓库用后续还原提交撤销本次新增，不改写历史。已加载会话可直接退出该模式。

## 四处预检

1. **当前现状：已核对。** 本机个人 Skill 没有 `present-clearly`；公开目标仓库已有 `think-clearly` 和 `battle-plan`。用户已确认通用表达、正文沿其观点、质疑段外，以及连续调整表达程度。
2. **官方路径：已核对。** 使用本机 Codex CLI 0.159.2、本机 skill-creator 的 YAML frontmatter、个人安装位置与验证指引（`SKILL.md` 第 147–168 行）；读取其 `references/openai_yaml.md` 第 30–49 行的 UI 字段、默认提示及调用策略。CLI 自身的 app-server 帮助和该版本生成的 `v1/InitializeParams.json`、`v2/SkillsListParams.json`、`v2/SkillsListResponse.json` 用于核对只读发现请求，不以旧版本记录冒充当前兼容证据。不改变第三方运行语义。
3. **既有实现：已核对。** 复用本机 `manuscript-optimizer` 的读者视角、具体表达与证据边界，参考 `think-clearly` 和 `battle-plan` 的模式触发与作者记录。此前定向搜索项目 Learning/helper/scripts/integrations 未找到本模式实现；与研究结论相关的统计或论文审查不作为本 Skill 的强制依赖。
4. **同类验收：已核对。** 个人 `think-clearly`、`battle-plan` 作者记录区分原生格式/发现与真实模型行为；项目验收区未找到本模式的行为实测。沿用这种证据分级，不继承其通过结论。

本机官方作者指引快照 SHA-256：`skill-creator/SKILL.md=CCCD291077EC57C6F50CA6529F0F3FB93212DA09473EFFB2FCEC808E81B21288`；`skill-creator/references/openai_yaml.md=7039D465B05342CBACF861F08D20192AB1EEEE112BC5D8FF0FB66234756887A9`。这些是已读取文件的版本证据，不作为公开 Skill 的运行依赖。

## 设计依据与来源

核心规则来自用户在本次对话中确认的写作姿态及输出偏好；本文件归纳约定，不公开原始对话、私人路径或机器配置。以下公开材料只作写作理念参考，不是运行依赖，也不宣称社区一致赞同所有判断。

- [Nature Portfolio：How to write your paper](https://www.nature.com/nature-portfolio/for-authors/write)：主要发现清楚可见，图文围绕核心信息。咨询阶段获得官方搜索文本；后续直接打开遇到站点身份跳转，未据此声称完成全文读取。
- [Zhang, 2014：Ten Simple Rules for Writing Research Papers](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003453)：目标读者、逻辑顺序与内容取舍。
- [Academia Stack Exchange：How important is storytelling…](https://academia.stackexchange.com/questions/215231/how-important-is-storytelling-when-submitting-a-grant-application-or-even-a-sci/215306)：已读取公开讨论，区分帮助理解的叙述与为叙述扭曲材料；这是参与者观点，不是共识或方法效果证明。
- 本机 `manuscript-optimizer/SKILL.md` 第 48–63、230–235、250–268、291–309 行：读者模型、主信息、必要推理、定量锚点与具体表达。新 Skill 自行编写，不复制完整上游 Skill。

## 验收基线

| 场景 | 正常功能 | 同时检查的边界 |
| --- | --- | --- |
| 明确调用并提供观点 | 直接给一段成稿，保留主旨与力度 | 不擅改立场，不只回复模式已开启 |
| 原话含绝对判断 | 正文沿用户意图整理，实质质疑在段外 | 不自动改为折中结论，不增加事实背书 |
| 连续自然/书面调整 | 基于最近一版继续调整，表达程度可辨认 | 不改变核心意思，不堆口头填充词或正式套话 |
| 只有观点没有数据 | 完成观点表达 | 不补造数据、经历或证据 |
| 普通观点无实质缺口 | 直接成稿 | 不强加反方或提醒 |
| 介绍、引用或编辑口令 | 正常解释或编辑 Skill | 不误启动模式 |
| 论文中包含条件与负例 | 保留影响判断的边界并凝练表达 | 不为顺畅删掉关键反例或把猜想升级为事实 |

## 验证结果

- **原生格式与发现：已验证。** Codex CLI 0.159.2 的短时 stdio app-server 仅执行 `initialize`、`initialized`、`skills/list`。个人 Skill 目录与独立仓库目录两个 cwd 均只发现一个 `present-clearly`，均为 `scope: user`、`enabled: true`，目标错误列表为空；中文 UI 名称、简介及包含 `$present-clearly` 的默认提示正确。服务器正常退出，退出码 0。没有 `thread/start`、`turn/start` 或额外模型调用。
- **编码与副本：已验证。** 三个 Skill 文件以严格 UTF-8 解码，无 BOM、CR 或替换字符；引用的本地文件存在，个人安装与待提交副本逐字节相同。原始检查输出留在 checkout 的 Git 本机管理目录，不公开用户路径或其他 Skill 清单。
- **创建时的 Python 校验器限制：历史事实。** 初次创建时 Python 的 `import yaml` 返回 `ModuleNotFoundError`，与既有作者记录一致；当时未重复执行依赖 PyYAML 的 quick validator，也未安装依赖，采用 Codex 原生解析作为格式与发现证据。用户随后授权补齐依赖，当前官方 Python 校验结果见下方补齐记录。
- **作者场景审阅：已完成，非独立模型行为评测。** 逐项核对上述七组正反约束，并使用下列实际成稿检查表达程度及段外提醒。口令规则仍是模型指令，不是确定性的关键词 hook；跨会话效果和不同模型的长期可靠性尚未验证。
- **发布内容边界：已审阅。** 仅三个新 Skill 文件与 README 使用说明；不发布私人对话原文、机器路径、凭证、个人配置、原有 Skill 作者记录或本机 Git guard。提交通过显式路径 task-commit 完成工作树预扫、staged 二次扫描及消息检查。最终上传结果以 GitHub commit 与远端回读为准。

## 作者场景产出

以下是作者依照规则实际撰写并检查的示例，使用本次已确认的写作观点；不是额外模型调用或独立盲测。各版保留“呈现发现、让读者判断”的主张及“不需要证明百分之百正确”的力度。

**自然一点：** 写论文时，我要先让读者看到一个有意思的发现，再带他看清它意味着什么。核心发现尽早讲明白，挑出最能说明问题的细节，把必要的解释说清楚，也坦诚交代不确定性和适用范围。我不需要证明自己百分之百正确，只需要把实际看见的东西清楚地呈现出来，让读者自己判断。

**再自然一点：** 写论文，我想做的就是把一个有意思的发现拿给你看：我们看到了什么，哪里值得注意，它又意味着什么。先把发现说清楚，再带你看具体的细节；哪些地方还不确定、在哪些条件下成立，也一起交代。我不需要证明自己百分之百正确，把实际看到的东西讲清楚，最后由你来判断。

**书面一点：** 论文写作应以清楚呈现发现为出发点：尽早说明核心发现，用关键事实与具体细节引导读者理解，并明确交代研究的不确定性和适用范围。作者无需证明自己百分之百正确，而应坦诚呈现实际观察及其意义，为读者提供作出判断所需的信息。

**再书面一点：** 论文写作的重心应是对发现的清晰呈现。作者应尽早交代核心发现，围绕主要信息组织必要证据与具体细节，说明关键推理，并如实界定不确定性及适用条件。写作无需以证明作者百分之百正确为目标；其任务是完整、坦诚地呈现实际观察及其意义，使读者能够据此形成判断。

**段外提醒示例：** 提醒：论文仍需交代证据如何支持结论，关键反证不能因凝练表达而省去。这里的“由读者判断”不会免除作者解释关键推理的责任。

**仅有观点、无数据的合成用例：** 输入“我认为午睡能帮助我下午更专注，但我没有做过统计”。输出“我认为午睡能帮助我在下午更专注。不过，这一判断尚未经过统计验证。”保留输入中的判断与边界，没有添加效果百分比、观察经历或研究结论；无需另加重复提醒。

**引用与退出的审阅：** “解释‘呈现模式，书面一点：’是什么意思”应解释用法；“退出呈现模式”应结束当前模式。已核对规则支持这两项，尚未做独立会话回放，不将静态审阅写成行为实测通过。

Learning 判断：`none`。本次是已确认个人写作协议的首版落地，尚无多次真实使用验证的新工程教训；不修改其他项目的 Learning 文档。

## 校验依赖补齐（2026-10-02）

- 授权补充：用户明确允许按需安装 PyYAML。写集增加当前 Python 的用户级 site-packages；Skill 正文及 UI 配置保持不变，只更新本记录及仓库副本。
- 四处复核：① Python 3.13.3 的 `yaml` 导入缺失，pip 25.0.1 已存在；② 固定 PyYAML 6.0.3 官方发行物和同 tag README，MIT 许可证，Python >=3.8，有 CPython 3.13 Windows x64 wheel；③ 复用现有 quick_validate.py，不修改校验器或安装其他依赖；④ 复用本任务此前原生解析与发现记录，新增官方 Python 校验结果，不扩大到其他 Skill。
- 官方来源：[PyPI 6.0.3](https://pypi.org/project/PyYAML/6.0.3/)、[同版本 README](https://github.com/yaml/pyyaml/blob/6.0.3/README.md)，固定 tag 原文第 23–25 行展示 `yaml.safe_load`，第 46–53 行说明 MIT 许可证。采用原生 pip 安装官方 wheel，以官方发行元数据冻结 `pyyaml-6.0.3-cp313-cp313-win_amd64.whl`，SHA-256 为 `79005a0d97d5ddabfeeea4cf676af11e647e41d81c9a7722a193022accdb6b7c`；只安装匹配的二进制 wheel，强制 hash，不升级 pip 或安装其他包。
- 验收：当前 Python 能导入固定版本并解析 Skill 的合法 YAML；非法 YAML 仍被拒绝；官方 quick validator 对个人安装与仓库副本均通过。场景行为评测的边界保持不变。
- 回滚：若需撤销，仅用同一 Python 卸载本次用户级 PyYAML；原生发现检查仍可使用。此次不创建新的工程 Learning 条目，因为该缺依赖现象与恢复路径已有证据，未形成新的跨任务教训。
- **当前结果：已验证。** `python -m pip install --user --index-url https://pypi.org/simple --only-binary=:all: --no-deps --require-hashes` 配合固定版本/hash requirements 安装成功；`yaml.__version__` 为 `6.0.3`。合法映射与列表经 `yaml.safe_load` 解析正确，缺少闭合括号的 YAML 抛出 `yaml.YAMLError`。`python -X utf8 quick_validate.py <个人 Skill 目录>` 与同命令的仓库副本均返回 `Skill is valid!`、退出码 0。Skill 正文和 UI 元数据未变，未把格式验证升级为独立行为评测。
