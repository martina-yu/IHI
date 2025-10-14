# **Intro Health Informatics**

## August 28 Overview

AMIA



## Sep 2 What is data, where they from

#### Health Data

homework

Metadate: meta meaning beyond

modality: a mode

Creatinine 肌苷酸, Fuzzy 不确定的

#### Data acquisition/Clinical data

Data 获取方式有哪些：比如observation,，lab results，clinical test等

#### Data Forms

data的形式有哪些。

structured、unstructured

#### Data quality（important）

completeness：censor

plausibility 合理性；

correctness 正确性：OB/GYN妇科；intubation （气管）插管；

concordance 一致性：metformin 二甲双呱；PMH（past medical history）多方实验一致

Currency 实效性？

#### Other aspects of health data

Big data difinition

#### Clinical data & Administrative data

Administrative data: information collected and maintained by government agencies and other organizations during their routine operations for administrative purposes, rather  than for research.

## Sep 4

## Sep 9



### **Sep 11 Database**



#### Database problems & correct structures

1. schema：数据store和related
2. Fields/columns/attributes：abstruct identity
3. types：data的format
4. Record, row, tuple
5. constraints: missingness, uniqueness
6. relationships：atom的connection

#### **Types of primary database**

![Screenshot 2025-09-14 at 15.28.16](/Users/yuzimeng/Library/Application Support/typora-user-images/Screenshot 2025-09-14 at 15.28.16.png)

1. hierarchical![Screenshot 2025-09-11 at 13.37.39](/Users/yuzimeng/Library/Application Support/typora-user-images/Screenshot 2025-09-11 at 13.37.39.png)
2. relational![Screenshot 2025-09-11 at 13.37.47](/Users/yuzimeng/Library/Application Support/typora-user-images/Screenshot 2025-09-11 at 13.37.47.png)

- Tuple 元組；Attribute 属性
- Primary key: 唯一的
- Foreign key：可以关联其他表的（比如两个表有相同的key）

#### **Relation Algebra**

- *并集union、交集intersect*、差集except（Difference）
- selection 行；projection 列
- cartesian product：笛卡尔乘积？
- Joins：inner join, left join, right join, full join

#### **Structured query language (SQL)**

- definition: is a programming language for storing and processing information in a relational database.

````sql
select p.patient_id
From Patients as p
Where p.test_name = 'Glucose'
````

grammar：核心查询语法（CRUD），SQL 的最常用功能可以概括为 **CRUD**：

- **Create (创建)**：`INSERT` 插入数据
- **Read (读取)**：`SELECT` 查询数据
- **Update (更新)**：`UPDATE` 更新数据
- **Delete (删除)**：`DELETE` 删除数据

其中，**`SELECT` 查询**是最复杂也最常用的部分。一个完整的 `SELECT` 查询通常包含以下几个关键子句：

```sql
select * -- 查询所有列
select 列1,列2 -- 查询列

where 条件 -- 返回条件的特定值
where age > 18

from 表名 -- 指定特定的表为数据来源
from 表1 join 表2 -- 联合两个表

group by 列名
-- 常常和聚合函数一起使用：sum, min, max, avg, count

order by 列名 -- 按照特定的顺序排序
order by 列名 desc
```

例子：![Screenshot 2025-09-14 at 16.12.43](/Users/yuzimeng/Library/Application Support/typora-user-images/Screenshot 2025-09-14 at 16.12.43.png)

```sql
-- 从patients表和labresults表中计算超过40岁的每种gender的平均WBC值

-- Logic：
-- 查询test results
-- 查询gender
-- 计算average（test results）
select
	p.gender
	avg(l.test_results) as avg_wbc

-- 列选择 patients
from patients p

-- 根据病人id列合并 patients join lab tests
join labresults l on p.patient_id = l.patient_id

-- 条件 age > 40且测试名称是WBC
-- DATE_PART('要提取的部分', 来源日期/时间)
-- '要提取的部分'：这是一个字符串，用来指定你想要提取什么。常见的选项有：'year', 'month', 'day', 'hour', 'minute', 'second'.
-- 来源日期/时间：你想要处理的日期或时间数据。
where l.test_name = 'WBC' and date_part('year', age(p.date_of_birth))>40

-- 分组 group by gender
group by p.gender

-- 顺序 order by test results
order by avg_wbc desc;

```

#### out of class scope part

超出本课程的部分

ACID gurantees：数据库事务的 **ACID 特性**，确保数据库可靠性的四个基本原则。

- Atomicity，transaction元素完整性，一个事务是不可分割的最小工作单元。这意味着它要么**完全成功**执行，要么**完全失败**回滚。不存在“部分完成”的事务。
- Consistency， 事务执行前后，数据库从一个**有效状态**转移到另一个**有效状态**。它确保了数据库中的数据总是符合所有预设的规则和约束
- Isolation，多个事务并发执行时，它们之间应该互不影响。一个事务的中间结果对其他事务是不可见的，就像它们是**按顺序一个接一个地执行**一样。
- Durability，一旦一个事务被**提交（Commit）**，它对数据库的改变就是**永久性的**。即使系统发生故障（如断电或崩溃），这个改变也不会丢失。

#### Terminology

- OLTP: online transaction processing
- OLAP: online analytics processing

#### NoSQL Database system

- Key-Value Stores
- Object Oriented Database
- Document Store
- Graph Database
