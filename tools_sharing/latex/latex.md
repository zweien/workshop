[[TOC]]

---

# LaTeX 使用心得

> TeX 是高德纳 (Donald E.Knuth) 开发的、以排版文字和数学公式为目的的一个计算机软件。
LaTeX 为 TEX 基础上的一套格式，令作者能够使用预定义的专业格式以较高质量排版和印
刷他们的作品。

- 优点：
  - 适用于科技文献排版，便于生成复杂表格和数学公式
  - 学位论文、主流期刊、会议模板
  - 专业排版元素，如脚注、交叉引用、参考文献、目录等
  - 熟悉数学公式，可用于 markdown 等文档格式
  - 基于文本，方便代码管理
  - 制作学术报告 Slides

- 缺点：
  - 需要掌握一门新语言
  - 非所见即所得 (WYSIWYG)
  - Debug

## 安装

- TeX 发行版推荐：[TeX Live](http://tug.org/texlive/)
  - 包含完整的 TeX 相关软件、宏包、字体等
  - 跨平台 Win、Linux、MacOS
  - 安装完整光盘镜像，一次安装终身受用
  - 包含完整的文档，`texdoc`
  - 自带轻量级编辑器：TeXworks
- 编辑器推荐：
  - [TeXstudio](http://texstudio.sourceforge.net/): 首推，高效编辑环境
  - [Overleaf](https://www.overleaf.com/)：在线、协同，部分 WYSIWYG
  - [BaKoMa](http://www.bakoma-tex.com): 真正的 WYSIWYG，但收费
  - 其它文本编辑器：VS Code、Sublime Text、Atom，配合相应插件也可实现一键编辑预览
  
## 基本语法

### LaTeX命令与环境

- 以 \ 开头
- 大小写敏感
- 命令参数，用 `{}` 表示
  - 可选参数 `[]` 表示
- 环境：局部生效，`\begin` 与 `\end` 包裹，环境名成对出现

```latex
\begin{env name}{args}[optional args]
...
\end{env name}
```

### 文档结构

- 导言区
  - 以 `\documentclass` 命令开头
  - `\usepackage{ }` 调用宏包


## Tips

- 绘图

## 资源

- 一份不太简短的LATEX2ε介绍，系统自带`texdoc`
- 数学公式 Short math guide for latex，系统自带：`texdoc short-math-guid`
- [Detexify](http://detexify.kirelabs.org/classify.html): 识别手绘数学符号
- [Mathpix](https://mathpix.com/)：公式 OCR，推荐，特别适用于文献中复杂公式的识别
- [beamer theme matrix](https://hartwork.org/beamer-theme-matrix/): beamer 自带样式展示

[^intro]: sdf
