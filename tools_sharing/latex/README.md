
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
  - 其它文本编辑器：VS Code、Sublime Text、Atom，配合相应插件也可实现丰富功能，扩展性更强
  
## 基本语法

### LaTeX命令与环境

- 以 \ 开头
- 大小写敏感
- `%` 注释
- 命令参数，用 `{}` 表示
  - 可选参数 `[]` 表示
- 环境：局部生效，`\begin` 与 `\end` 包裹，环境名成对出现

```latex
\begin{env name}{args}[optional args]
...
\end{env name}
```

### 文档结构

- **导言区**：对文档的全局设置命令、宏包调用
  - `\documentclass{}` 文档类型
    - 自带 article、report、book、beamer
    - 选用期刊、学校提供的样式文件
    - 例如：`\documentclass[11pt,twoside,a4paper]{article}`
  - `\usepackage{}` 调用宏包
- 正文内容放在 `\begin{document}` 与`\end{document}` 之间

- [英文文档案例](./example/example.tex)
- [中文文档案例](./example/example_zh.tex)：借助 `ctex` 宏包，不是**CTeX**发行版
  - 建议先阅读 ctex 文档
- [幻灯片制作](./example/example_beamer.tex)：beamer
  - beamer 文档有详细教程

## Tips

- 投稿时根据相应要求，一般会有样式文件、配套手册
- 文档查看：`texdoc` 命令查看
- 数学公式
  - 借助编辑器选择符号
  - Mathpix 在线识别
  - Detexify 在线绘制
  - Short Math Guide
- 绘图
  - TikZ，需要学习特殊绘图语言
  ![tikz](./example/tikz_example.png)
- 表格可以借助[在线工具](http://www.tablesgenerator.com/latex_tables)
- 书籍、毕业论文等，可将源代码分割成不同文件，使用 `\include{filename}` 组合
- `latexdiff` 可生成[文档修订](./example/diff/example_diff.pdf)
  - `latexdiff origin.tex modify.tex >diff.tex`
- 多人协同可以用在线的 `Overleaf`
- 遇到问题怎么办
  - 除错：lshort-zh-cn 中附录B
  - 搜索引擎

## 资源

- 一份不太简短的LATEX2ε介绍，系统自带：`texdoc lshort-zh-cn`
- 数学公式参考文档 `texdoc short-math-guid`
- [Detexify](http://detexify.kirelabs.org/classify.html): 识别手绘数学符号
- [Mathpix](https://mathpix.com/)：公式 OCR，推荐，特别适用于文献中复杂公式的识别
- [beamer theme matrix](https://hartwork.org/beamer-theme-matrix/): beamer 自带样式展示
