# 关于全文标题不能换行的问题
在由`v5.02`向`v5.03`升级的过程中，因代码编辑过程中的疏忽造成新版本出现了大标题不能换行的问题。目前美赛已临近尾声，再修改仓库里的源代码没有实际意义，
因此仅将可行的解决方案在此贴出：

目前，标题被默认为一行（由于`\centerline`命令）而不能换行了。请到`easymcm.sty`文件中修改，约在`160`行左右：

```latex
%=======摘要生成命令=========
\def\make@abstract{
    \vskip -10pt\par
    \centerline{\bf\abstractname}\vskip 10pt\par    %摘要标题
    \centerline{\Large\bf\@title}\vskip 5pt\par    % 插入论文标题，字号可自己修改
    \noindent\usebox\@abstract\par  %摘要正文
    \vskip 10pt %底部留空，若不需要可删去
}
```

改为：

```latex
%=======摘要生成命令=========
\def\make@abstract{
    \vskip -10pt\par
    \centerline{\bf\abstractname}\vskip 10pt\par    %摘要标题
    \begin{center}\Large\bf\@title\end{center}\vskip 5pt\par    % *****
    \noindent\usebox\@abstract\par  %摘要正文
    \vskip 10pt %底部留空，若不需要可删去
}
```

仅有标注了`*****`的那一行做了改动，先将其改为一个`center`环境了事（其实这样做是不好的……）。再编译一次就可以了。
