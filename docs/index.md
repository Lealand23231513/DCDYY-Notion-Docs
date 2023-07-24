# 使用说明

这里是大创大语言项目的文档仓库，使用[mkdocs](https://www.mkdocs.org/)构建，同时[read the docs](https://readthedocs.org/)提供基于github仓库的网页渲染，文档采用的是markdown格式。。Notion中已经完成的任务文件，可以导出并放到这里。

**注意：如果不会git，可以只编辑docs目录下自己名字的文件夹。** 如果对于push，pull，branch，merge等概念比较熟悉，就没有这个限制。

## 参与编辑的方法
1. 从[github仓库](https://github.com/Lealand23231513/DCDYY-Notion-Docs)clone到本地。
2. 编辑文档（/docs/name/xxx）
3. 编辑完成后push到仓库。

## mkdocs使用小技巧
### 1. 忽略文件（目录）
mkdocs会自动忽略以.开头的文件和目录，例如:.foo.md，.ignore/xxx等。因此，可以将不想被渲染的文件和目录改为以.开头。
### 2.本地渲染
在项目根目录打开终端，输入
```shell
mkdocs serve
```
打开url即可看到渲染好的网页。