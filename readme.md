# 使用说明
该文档是为了向外包公司说明项目的需求、模块接口、测试案例、简单页面设计、数据库架构的文档，此文档为公开文档，故关于算法的细节部分不要在此文档内阐述。但需求和功能模块接口需要写很详细，需求可以多提，将能想到的都放上去，不需要考虑版本的问题，然后我们再备注哪些是7月份版本需要公司完成的。
如果希望在本地编译查看效果，可以按以下章节进行学习，如果不需要，请直接编写并查看无误后直接提交github。
在编写阶段，建议只在本地 `make html` 查看效果，使用git进行版本控制，不要push到github。

## 安装环境
pip install sphinx sphinx-autobuild sphinx_rtd_theme sphinx_markdown_tables

[学习链接](https://www.xncoding.com/2017/01/22/fullstack/readthedoc.html)

- 查看效果：make html，可在build/html中打开index.html查看效果

## github
- commit时请按照以下规范提交：hanfeng-add readme(提交人-提交内容)
- username：ZGF0YWdyb3VwdXN0Yw==
- password：TGlua2VVU1RDKzFz

## read the docs
- https://readthedocs.org
- name和pass同github

## 编写说明
- source/platform下有以下文件
   - requirement：需求说明
   - page：页面需求说明
   - function：功能模块接口
   - database：数据库设计
   - storage：数据存储相关的设计
   - timeline：时间规划
   - questions：将现有的问题分类写在此处，如有解决方案可以在问题下进行填充
   - figure文件夹：存放相关图片资料，命名规范：groupname-XXX
- 编写规范说明
   - 需求说明文档：待增
   - page：待增
   - function：见该页面开头
   - database：待增
   - timeline：待增
- 如有其他问题，大家多沟通下哈
