# Score 课程给分数据

*Author: [NagisaCo](https://github.com/NagisaCo)*

## 简介

本文件夹存储，在 2021 年 9 月选课期间使用项目 [NagisaCo/WHU-CourseGrade](https://github.com/NagisaCo/WHU-CourseGrade) 对梦想珈“查给分”的爬虫数据汇总。

由于因不可抗力，梦想珈“查给分”功能已下线，上述项目暂无可用数据源，现停止维护，并将结果上传以供其他人使用。

> 所有数据均来自于网上，本项目对数据真实性不做保证
> 
> 如有侵权，请联系我删除
> 
> 禁止用于非法用途，违者后果自负

## 内容说明

目前在该文件夹下仅有 course_grade_202109.xlsx 一个汇总文件，由 mysql 数据库直接导出。

请合理使用 Excel 中的筛选与排序功能。

### 表说明

excel 文件内部一共有 8 张表，表名由 *前缀*_*后缀* 构成：

|前缀|含义|
|:-:|:-:|
|sport|体育课|
|specialized|专业课|
|optional|选修课|
|eng|英语课|

|后缀|含义|
|:-:|:-:|
|course|课程|
|class|课程下不同老师开的课|

### 字段说明

#### course 表

|字段|含义|
|:-:|:-:|
|id|主键（与 class 中的 class_id 关联）|
|code|课程号（与学校选课系统一致）|
|name|课程名|
|credit|学分|
|category|分类|
|subcategory|子分类|
|academy|开课学院|
|time|创建时间|

#### class 表

|字段|含义|
|:-:|:-:|
|id|主键|
|course_id|所属课程|
|name|课程名|
|teacher|任课老师|
|score|平均分|
|number|统计人数|
|section_n|[10(n+1), 10n) 分数段的人数|
|time|创建时间|
