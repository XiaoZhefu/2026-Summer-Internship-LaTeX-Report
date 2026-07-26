# 2026 Summer Internship LaTeX Report

实习报告的 LaTeX 源文件仓库。

## 注意事项

本项目将在本人从同济大学毕业后公开，不一定具有时效性，仅供学习LaTeX使用。

## 文件结构

```text
.
├── report.tex          # 主文档
├── report-header.tex   # 宏包、字体与通用排版设置
├── .gitignore          # 文件忽略配置
├── .latexmkrc          # PDF 1.7 输出配置
├── LICENSE             # MIT License
├── includes/           # 前置页、图片、表格与参考文献分文件
├── sections/           # 正文各章节分文件
├── assets/             # 图片、矢量图及其源文件
├── references/         # 参考资料（已忽略）
└── out/                # 编译输出目录（已忽略）
```

## 编译

使用 XeLaTeX 编译 `report.tex`。编译产物位于 `out/report.pdf`。

```powershell
xelatex -no-pdf -interaction=nonstopmode -halt-on-error -output-directory=out report.tex
xdvipdfmx -V 7 -E -o out/report.pdf out/report.xdv
```

## 开源许可

本项目采用 [MIT License](LICENSE)。
