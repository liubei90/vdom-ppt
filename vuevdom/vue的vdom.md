# VUE中有Component和VNode两种类型

## Component是组件

- Vue
- 通过Vue.component('name', { /*options*/ })注册
- .vue文件导出

## VNode是虚拟DOM

- 通过render函数返回

## Component和VNode的关系

- Component挂载时，通过render函数生成一个VNode树，根节点是vm._vnode
- vnode节点有多种类型， 通过tag属性区分
    1. 浏览器默认的元素（'div', 'span'）
    2. Component（'keep-alive', 'el-button'）
- Component更新时，会根据VNode树生成真实DOM树
    1. 默认元素生成的是其对应的DOM元素
    2. Component生成的是组件实例，该实例会继续调用挂载函数，直到生成真实的DOM元素

## VNode的结构

- tag
    + 节点类型
- data
    + 节点属性（on, nativeOn, attr, props, domProps, staticClass, class, staticStyle, style, normalizedStyle, scopedSlots, slot, key, ref, is）
- children
    + 子节点， 和slot有点区别
- text
    + 文本节点的内容
- elm
    + 节点的真实DOM
- context
    + VNode所属的Component
- componentOptions
    + Component的信息（构造函数，data, listeners ...）
- componentInstance
    + Component的实例
- parent
    + 父节点

## VNode生成真实DOM时的操作

- 生成真实DOM
- 设置真实DOM的attributes和propertieys

### 需要处理的数据有

- ref
- directives
- attrs
    - 具体有什么attrs？
    - 怎么处理的，为什么这么处理
- class
    - 怎么处理的，为什么这么处理
- events
- domProps
    - 怎么处理的，为什么这么处理
    - 和attr的关系
- style
    - 怎么处理的，为什么这么处理
- transition

### 通过hook钩子完成解耦

- 每种属性的处理逻辑都写成模块
- 支持在data.hook上写自己的功能