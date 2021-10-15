# 本地研发流程



### 提交规范

为了增强 Commit Message 的可读性：人类可读和机器可读。

并且能够在每次发版的时候，能够明确的提取出每个版本的 Change Note。此处的Change Note 特指面向研发同学的Change Note，当产品对外发布的时候还需要产品同学接入来确定对应的 Release Note。

忠实的记录每一个 Commit 相关性信息，以备在 CodeReview、回溯修改等场景中提供更多的上下文。

Commit Message 格式

> &lt;&gt; 表示必选字段

> \[ \] 表示可选字段

每次提交， Commit Meessage 都包括三个部分： Header、Body、Footer

```text
[[options]]<type>[(scope1,scope2)]: <description>

[optional body]

[optional footer(s)]
```

实例：

```text
[T1223]feat(byteview): implatation the online office
we add an feature called online office to increase the efficicence of work form home model.
prd: http://feishu.cn/prd/xxxxxxx
test: http://feishu.cn/test/xxxxxxx
design: http://feishu.cn/design/xxxxxxx
jiraid: SUITE-XXX
Changed-Id: hjkskjxjhsjdfkjdklfsjdf
```

提供给机器可读的数据使用 : 格式（注意这里是使用的英文半角的 ":"），这种格式在 Header 和 Footer中会大量使用。

#### Header

提交信息头部由四部分组成：type（类型），scope（生效范围），options\(选项\), description（概述）。其中类型和概述是必选字段，用来描述该 Commit 影响的内容。

type（类型）

type 用于说明 commit 的类别，在头部中只允许出现一次 type 标记，并且只允许使用下面7个标识：

| type | 说明 |
| :--- | :--- |
| feat | 新功能，当你的 Commit 是为了添加新的功能feature的时候，需要使用该标记。也包括修改现有的功能，让现有功能有不一样的表现。 |
| fix | 修补bug |
| refactor | 重构（即不是新增功能，也不是修改bug的代码变动）。注意，如果在重构的过程中，有新的功能点加入要讲这个修改升级到 feat 类型。 |
| docs | 只是修改了文档，没有动相关的功能。如果一个 commit 既修改了功能也修改了文档，则以修改功能为主。 |
| style | 格式变化，只是修改了一下代码格式或者目录结构。对于功能不产生影响。 |
| test | 测试相关的改动，例如修改了测试脚本，或者增加了测试相关的代码。 |
| chore | 构建过程或辅助工具的变动。注意这里是专指构建及辅助工具的变更。请不要滥用这个标签来表述一些无法明确归类的类型。 |

一般仓库中的物料，我们分成以下几中类型：代码、测试相关物料、文档、辅助工具。上述几个类型的切分理由是，按照提交影响到的物料进行分类。

一般需要说明的对于代码的变动优先级要大于对于其他物料的变动，feat、fix、refactor类型主要描述代码的修改，这两个类型的优先级要高过其他类型。当一个修改涉及到多种物料的修改的时候，以代码变动的类型为主，在header中标注为对应类型。其他的物料修改可以在 body 中进一步阐述。

在上述通用格式之外，对于每一种类型列出了更加详细的规范，在提交类型的Commit Message的时候需要遵循其规范：

* ​​

#### scope（范围）

​scope​用于说明 commit 影响的范围，这里鉴于以往个技术栈使用scope字段来表示影响的业务单元。影响的业务​​。注意scope可以用 "," 进行分割，以表示影响的业务范围。

除了业务单元外，额外增加以下scope：

| scope | 含义 |
| :--- | :--- |
| ui | 影响了UI界面，需要相关同学关注。 |

示例：

`feat(byteview,feed,ui): impletation the online office`

options \(选项\)

选项是用来描述一个 提交 的特殊信息，一般用于能够快速的将某些信息提供给阅读者查看。同时设计改功能也是为了兼容目前在套件客户端内的一些使用现状。

选项是footer中的配置信息前置，选项中内容一般会同时出现在头部和尾部中。

目前支持的选项为 SUITE、LBID，更多可以参考 [Footer](https://bytedance.feishu.cn/docs/doccnNrl1B4hJ7du9YYTA83M7Ob#5M9MBk) 介绍

| suite | suite为套件在jira中的代码，使用该key可以标注对应的jira的jiraid |  |
| :--- | :--- | :--- |
| lbid | 阻塞性的bugid，用于nest系统发版使用。 |  |

#### description （概述）

deescription 是 commit 目的的简短描述，不超过50个字符。请使用 英文 描述，不要使用中文。

> 以动词开头，使用第一人称现在时，比如​change​，而不是​changed​或​changes​

> 第一个字母小写

> 结尾不加句号（​.​）

#### Body

Body 部分是对本次 commit 的详细描述，可以分成多行。请使用 英文 描述，不要使用中文。

为了能够让看到 Commit Message 的人更好的理解你的修改的含义，可以参考：​​ 。

下面是一个范例。

`More detailed explanatory text, if necessary. Wrap it to`

`about 72 characters or so.`

`Further paragraphs come after blank lines.`

`- Bullet points are okay, too- Use a hanging indent`

#### Footer

footer用来增加一些额外的信息的信息，使用: 格式。tag除非某些特殊系统的要求，请使用小写来描述。footer是个可选字段，是为了让看到这个commit的同学能够，能够获取到关于这个commit的更多上下文。

支持的格式如下：

| key | 含义 | 是否必填 | 附注 |
| :--- | :--- | :--- | :--- |
| prd | 产品需求文档 | 如果是 feat 或者 fix 类型，建议必填 |  |
| test | 测试文档 | 建议必填 |  |
| design | 设计文档 | 建议必填 |  |
| metrics | 涉及到的埋点变更，如果这个需求涉及到了埋点数据的变更，需要使用metrics标签来标注一下，哪些事件收到了影响。来记录里面有多少perf、稳定性的埋点（包括端和后台的）。 |  | 例如，修改了event\_push\_message 则需要增加metics: event\_push\_message。尤其是对于一些影响perf和metrics影响的事件 |

