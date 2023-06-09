---
title:Linux系统的基础命令
# Link this post with a project
projects: []

# Date published
date: '2020-12-13T00:00:00Z'

# Date updated
lastmod: '2020-12-13T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

authors:
  - admin
  - Love Astro

tags:
  - Linux
  - command

categories:
  - Linux
  - command
---

1.echo(说明，如果你想看变量，但是又不想进入".bashrc"，那么可以使用此命令让它在屏幕上只打印你需要的变量内容.)

作用：

用于在终端输出字符串；

变量提取后的值.

格式：echo [字符串]，echo 变量

若字符串中出现以下字符，则特别加以处理，而不会将它当成一般文字输出：
```latex
\a 发出警告声；

\b 删除前一个字符；

\c 最后不加上换行符号；

\f 换行但光标仍旧停留在原来的位置；

\n 换行且光标移至行首；

\r 光标移至行首，但不换行；

\t 插入tab；

\v 与\f相同；

\\ 插入\字符；

\nnn 插入nnn（八进制）所代表的ASCII字符；
```

