# Javascript

## DOMContentLoaded这个事件是在什么情况下触发的

文档解析完成: 当 HTML 文档被完全加载和解析时，DOMContentLoaded 事件会被触发。这意味着 DOM 树已经构建完成，所有的元素都可以被访问和操作。
不等待外部资源: 该事件不会等待样式表、图像或其他外部资源（如 iframe）加载完成。因此，它通常会比 load 事件更早触发。
事件触发时机: DOMContentLoaded 事件在 HTML 文档完全解析后触发，但不等待图像、样式表和其他外部资源的加载。这使得它非常适合在 DOM 准备好后立即运行 JavaScript 代码。
与 defer 脚本的关系: 当使用 defer 属性时，这些脚本会在文档解析完成后、DOMContentLoaded 事件触发之前执行。换句话说，所有的延迟脚本会在 DOM 完全构建好后立即执行，因此可以安全地操作 DOM。
因此，是的，DOMContentLoaded 事件会等待带有 defer 属性的 JavaScript 脚本加载和执行。这使得开发者能够在 DOM 准备好后安全地进行操作，而不必担心外部资源是否已经完全加载。

## 事件绑定 this 指向相关问题

``` javascript
let a = document.querySelectorById('app');
a.addEventListener('change', () => {});

this 的含义: 在箭头函数中，this 的值是从外部上下文继承而来的。换句话说，this 将指向定义箭头函数时的上下文，而不是事件目标（即触发事件的元素）。因此，如果在这个箭头函数内部使用 this，它将指向包含该代码的作用域（例如，可能是全局对象或包含该代码的其他对象）。
```

``` javascript
a.addEventListener('change', function(e) {});

this 的含义: 在常规函数中，this 的值指向调用该函数的上下文。在事件处理程序中，this 通常指向触发事件的元素，即在这个例子中是 a（即 #app 元素）。因此，在这个函数内部使用 this 时，它将引用触发 change 事件的元素。
```

总结
箭头函数: this 的值由外部作用域决定，不指向事件目标。
常规函数: this 的值指向触发事件的元素（即 a）。

## 面试被问到如何一次性渲染十万条数据，我该怎么答？

[渲染页面的优化](https://juejin.cn/post/7420248650607902757)

## 面试被问到跨域还不会答？来看看这篇文章

[跨域](https://juejin.cn/post/7418085899719294976)

