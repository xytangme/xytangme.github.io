---
title: "Hell World"
date: 2022-10-18T18:38:04+08:00
draft: false
---

确实是Hell不是Hello，没有少写一个o。

还以为自己已经是个老司机了，没想到还是踩了好几个坑，其中两个值得特别记录一下：

- 为了避免部署时大头，`theme`最好以`submodule`的形式引用
- 由于`GitHub Actions`会生成一个`gh-pages`分支用于部署，所以需要将`settings → Pages → Build and deployment → Branch`由`main`改为`gh-pages`

以上。