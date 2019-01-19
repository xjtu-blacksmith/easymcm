七位控制号**居中不齐**的问题，我会在之后发布的新版本里统一解决。为解燃眉之急，可先这样做：在`easymcm.sty`文件中**第200行**左右，注释标明为“*中间的控制号环境*”处，有这样一些代码：

```latex
% 中间的控制号环境
\begin{minipage}{0.33\textwidth}
    \centering
    Team Control Number\\[10pt]
    {\fontsize{38pt}{25pt}\selectfont  \textbf{\MCM@control} }\normalsize\\[10pt]
    Problem Chosen\\[10pt]
    {\fontsize{18pt}{\baselineskip}\selectfont \textbf{\@problem}}\normalsize\\
\end{minipage}\hspace{\fill}
```

将以上第5行中的`\fontsize{38pt}{25pt}`之`38`改小为`30`左右，缩小字号，数字就能正确居中了（*比例也更合适一些*）。美赛官方对这个数的尺寸**没有要求**。
