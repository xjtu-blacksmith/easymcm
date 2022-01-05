# 一个简洁、易用的美赛 LaTeX 模板: easymcm

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/xjtu-blacksmith/easymcm)](https://github.com/xjtu-blacksmith/easymcm/releases)
![GitHub All Releases](https://img.shields.io/github/downloads/xjtu-blacksmith/easymcm/total)

easymcm 是一个为美国大学生数学建模竞赛（MCM）准备的简易 LaTeX 模板。它二次开发自 LaTeX 宏包 `mcmthesis` 于 2013 年发布的 `v5.0` 版本，原作者是[王昭礼](http://www.latexstudio.net)。

> 事实上，`easymcm` 与另一美赛 `mcmthesis` 的最新版本并无关联，后者为一个文档类（class）而非一个宏包（package）。该文档类现由 [Liam0205](https://github.com/Liam0205/mcmthesis/releases/) 维护。

关于 `easymcm` 的说明及其来由，详见原作者[黑山雁的博客](https://xjtu-blacksmith.cn/program/easymcm)。2019 年时，easymcm 宏包由[黑山雁](https://github.com/xjtu-blacksmith)移交给[钱院学辅](https://qyxf.site)组织管理；到 2020 年，因若干原因，本模板再次移回到黑山雁个人名下。

## 发布渠道

[![GitHub Repo stars](https://img.shields.io/github/stars/xjtu-blacksmith/easymcm?style=social)](https://github.com/xjtu-blacksmith/easymcm)
[![Gitee Repo stars](https://gitee.com/xjtu-blacksmith/easymcm/badge/star.svg?theme=dark)](https://gitee.com/xjtu-blacksmith/easymcm/stargazers)

开发和分享此宏包，并无功利目的，仅是为了方便初学者的使用；基于此目的，作者不会将该宏包发布到 CTAN 之上，仅供国内用户学习使用。

- GitHub（主要分发平台）：<https://github.com/xjtu-blacksmith/easymcm>
- Gitee（国内镜像）：<https://gitee.com/xjtu-blacksmith/easymcm>

## 使用说明

本模板中包含的主要文件为两个：

- `easymcm.sty`：宏包文件，定义了论文的各项样式、配置；
- `PAPER.tex`：论文正文，用于撰写论文的具体内容。

后者可根据用户的需要修改为其他名称，例如队伍控制号为 1234567 的队伍可将 `PAPER.tex` 改名为 `1234567.tex` 再编译，这样将直接得到文件名符合官方要求的 `1234567.pdf` 文件。

在这两份文件中，均有详细的注释说明。若用户需要局部修改样式（如修改某处的字号、段间距），在 `PAPER.tex` 中对应位置用分组 + 命令的方式就可解决；若用户需要修改全局样式（如修改正文的默认段间距），则可先到 `easymcm.sty` 文件中检查是否有对应的命令进行设置，若有可直接修改其参数，若无可自行添加。

## 编译方式

本份模板允许使用 `pdftex`、`xetex`、`luatex` 等各个通行引擎编译，兼容老旧的 CTeX 套装。

若您使用 CTeX 套装，建议您在[发布](https://github.com/qyxf/easymcm/releases)页面上下载**带有 ANSI 字样**的文件，否则文件中的中文注释将在 CTeX 套装的 WinEdt 编辑器中显示为乱码；反之，若您使用的是比较新的发行版本，请不要使用带有 ANSI 字样的版本。

如您身处比较流畅的国际网络环境中（例如，能够访问 Google），推荐您使用 [Overleaf](https://overleaf.com) 在线编译，以减少各类错误的发生。下载本模板的 `zip` 压缩包，并上传至 Overleaf 中作为项目，即可快速编辑、编译。

## 联系作者

本模板目前由[黑山雁](https://github.com/xjtu-blacksmith)维护。若在使用过程中出现任何问题，可通过以下方式联系作者：

- 在本模板的[讨论页面](https://github.com/xjtu-blacksmith/easymcm/discussions)发布帖子（推荐，但需要注册 GitHub 账号）；
- 通过作者的邮箱 xjbs@protonmail.com 联系作者（不推荐，作者很可能不会回复你）。
