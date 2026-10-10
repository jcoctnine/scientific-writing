# scientific-writing

基于四本论文写作教材的 Codex skill，用于英文原创科研论文的起草、结构修改和语言润色，也支持将中文研究材料组织为英文正文。默认论文正文使用英文，解释使用中文；遵循用户明确指定的语言和编辑范围。

本版包含 **17个方法簇、157条可回查的方法记录**。只使用教材方法；期刊定制、研究者风格档案和 Supervisor-Skills 整合暂未纳入。

## 工作方式

1. 识别材料属于标题、摘要、Introduction、Methods、Results、Discussion、Conclusion、致谢或全文问题。
2. 判断任务是起草、结构修改、语言润色还是只给建议，并确认修改范围。
3. 按需读取适用方法簇，必要时回查带有条件、例外和页码的来源卡。
4. 存在适用且有实质差异的写法时，提供选项与短例，等待用户选择；同一会话中，同一论文的同一章节沿用已选写法。
5. 交付所需正文或建议，说明影响理解的改动和缺失材料。

17个簇是方法索引，不是每次必须执行的17个步骤。普通语法修正不需要选择风格。只润色时保留原结构；只给建议时不覆盖正文。

## 安装

仓库根目录就是技能目录。可以让 Codex 使用 `skill-installer` 从本仓库安装 `scientific-writing`，或在目标目录尚不存在时手动安装：

```bash
git clone https://github.com/jcoctnine/scientific-writing.git ~/.codex/skills/scientific-writing
```

如果设置了自定义 `CODEX_HOME`，安装到其 `skills/scientific-writing` 目录。已有安装时先保留备份，避免覆盖自己的修改。私有仓库需要相应的 GitHub 访问权限。安装后重启 Codex，使其加载新技能。

## 调用示例

```text
$scientific-writing 只润色下面的英文 Methods，保留结构、数据、术语和引用。
```

```text
$scientific-writing 根据下面的真实研究材料起草 Introduction；如果有不同的组织方式，先给我选项。
```

```text
$scientific-writing 检查这段 Discussion 的解释和局限是否与结果对应，先只给修改建议。
```

研究材料中的事实、结果、文献、完成状态及未知信息应明确提供。缺失材料会列为待补；技能不会把计划写成结果，也不会编造数据或引文。

## 目录

| 文件或目录 | 作用 |
|---|---|
| [SKILL.md](SKILL.md) | 入口、任务识别、方法路由与执行边界 |
| [agents/openai.yaml](agents/openai.yaml) | Codex 界面信息 |
| [references/clusters/](references/clusters/) | 17个方法簇的适用条件与执行建议 |
| [references/writing-options.md](references/writing-options.md) | 不同写法的适用条件与选择流程 |
| [references/source-notes.md](references/source-notes.md) | 教材版本、页码约定、来源问题及跨书差异 |
| [references/sources/](references/sources/) | 四本教材的来源卡与阅读覆盖记录 |

## 教材来源

| 编号 | 教材 | 方法记录 |
|---|---|---:|
| WS | Joshua Schimel, *Writing Science: How to Write Papers That Get Cited and Proposals That Get Funded*, 2012 | 35 |
| AWG | John M. Swales & Christine B. Feak, *Academic Writing for Graduate Students: Essential Tasks and Skills*, 3rd ed., 2012 | 44 |
| WSRA | Margaret Cargill & Patrick O’Connor, *Writing Scientific Research Articles: Strategy and Steps*, 2nd ed., 2013 | 35 |
| SRW | Hilary Glasman-Deal, *Science Research Writing: For Native and Non-Native Speakers of English*, 2nd ed.; 编目2020、版权2021 | 43 |

来源卡是本项目对原书方法的中文概括，保留适用条件、操作步骤、限制与例外，以及书内页码和提取所用 PDF 的物理页码。跨书执行建议属于本项目综合设计，可选写法名称属于整理者归纳；两者均不能反向引用为教材作者原话。

本仓库不包含原书 PDF、完整转载文章、练习页或扫描页图。原书权利归各自权利人；本仓库目前未指定开源许可证。

## 验证与边界

- 已通过技能格式、方法编号与覆盖索引、包内链接检查。
- 已完成7个同上下文示例走查；这不等于独立会话中的行为测试，也不代表对全部教材例文或外部科学事实的复核。
- 写作建议保留数据、引用、术语、归属和不确定性，不设固定段数、语态比例或引用数量，不将常用结构作为强制模板。
- 教材提供写作方法，研究事实仍须来自作者材料。技能不认证统计分析的有效性，也不承诺发表或引用效果。
