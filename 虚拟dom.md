分解工作
1. 网上找教程，关于虚拟dom，自定义元素，标准文档
2. propertity/attributes的关系
3. 总结多个框架对虚拟dom的实现，虚拟dom的结构，虚拟dom到真实dom的处理过程


# html解析后是什么

# DOM是什么

# 虚拟DOM是什么

# propertity/attributes的关系, 虚拟DOM如何处理

- propertity是DOM实例上属性集合
- attributes是DOM实例的一个叫attributes的属性，是元素所有属性节点的一个实时集合。内容是key-value形式，值都是字符串
- html解析生成dom树时，会给每个dom生成attributes
- dom会根据attributes，初始化同名propertity，初始化规则多样
- 脚本修改attributes时，浏览器会同步修改propertity
- 脚本修改propertity时，浏览器会同步修改同名的attributes

## 是否所有同名propertity/attributes都会同步初始化和同步修改？

## 列举和虚拟DOM相关的propertity/attributes