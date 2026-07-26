# 2026 Summer Internship LaTeX Report

实习报告的 LaTeX 源文件仓库。

## 注意事项

本项目将在本人从同济大学毕业后公开，不一定具有时效性，仅供学习LaTeX使用。

## 文件结构

```text
.
├── report.tex                    # 主文档，组织各分文件输入顺序
├── report-header.tex             # 宏包、字体与通用排版设置
├── .gitignore                    # 文件忽略配置
├── .latexmkrc                    # PDF 1.7 输出配置
├── LICENSE                       # MIT License
├── includes/                     # 非正文主体的 LaTeX 分文件
│   ├── front-matter.tex          # 封面、说明、目录与正文页码初始化
│   ├── figures.tex               # 图片命令定义，提供 \reportFigure{...}
│   ├── table-01-schedule.tex     # 表1：实习日程安排
│   └── references.tex            # 参考文献
├── sections/                     # 正文各章节分文件
│   ├── 01-overview.tex           # 一、生产实习概况
│   ├── 02-manufacturing.tex      # 二、城轨车辆制造工艺概述
│   ├── 03-maintenance.tex        # 三、轨道车辆检修与运维管理认知
│   ├── 04-course-analysis.tex    # 四、课内知识联动分析
│   └── 05-summary.tex            # 五、总结与展望
├── assets/                       # 图片、矢量图及其源文件
└── out/                          # 编译输出目录（已忽略）
```

## 编译

使用 XeLaTeX 编译 `report.tex`。编译产物位于 `out/report.pdf`。

```powershell
xelatex -no-pdf -interaction=nonstopmode -halt-on-error -output-directory=out report.tex
xdvipdfmx -V 7 -E -o out/report.pdf out/report.xdv
```

## 开源许可

本项目采用 [MIT License](LICENSE)。
