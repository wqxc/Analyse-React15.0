## map 方法。

### 概念

Map 方法是 Children 属性的属性之一。
主要用来遍历组件的子节点。

### 用法

```
React.Children.map(this.props.children, function (child) {
    return <li>{child}</li>;
)}

```

### 位置 

Map方法是定义在 ReactChildren.js文件内的。名字叫做 mapChildren

简单的来说是 Map==> mapChildren


```

function mapChildren(children, func, context) {
  if (children == null) {
    return children;
  }
  var result = [];
  mapIntoWithKeyPrefixInternal(children, result, null, func, context);
  return result;
}

```

如上所示。

参数 children  表示要遍历的所有子元素。
 children的类型是不确定。

 null,数字，布尔值,Object，undefined，Array