# omi虚拟dom格式

```
var vnode = html`
<div>
    <button onClick=${clickHandler}>hello, world</button>
</div>
`;

{
    "nodeName": "div",
    "children": [
        {
            "nodeName": "button",
            "children": [
                "hello, world"
            ],
            "attributes": {
                "onClick": "clickHandler"
            }
        }
    ]
}

```

# omi如何处理attributes

- class：将值设置为node.className
- style: 值为字符串，设置为node.style.cssText。值为object，设置为node.style['csskey']
- on***：添加或者删除事件监听器，和html绑定事件的行为相同
- value：node的nodeName为input时，设置为node.value
- name in node: node里存在该属性，设置为该属性
- 其他：通过node.setAttribute和node.removeAttribute，设置到node.attributes上


# omi中的自定义DOM

继承自HTMLElement类，