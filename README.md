# mianshi

面试题

一．HTML5 中的语义化标签有哪些？

包括header、nav、article、section、aside、footer等

二．HTML5 中的多媒体支持哪些？

HTML5 提供了内置的多媒体支持，包括audio和video标签，用于在网页上嵌入音频和视频内容。

三．HTML5 中的本地存储有哪些机制？

HTML5 的本地存储机制：Web 存储和 indexedDB

Web 存储包括长期保存（LocalStorage）和会话期间保存（SessionStorage），用于浏览器中存储键值对数据。

四．CSS 选择器有哪些类型？

CSS 选择器用于选择需要应用的 html 元素。

常见的选择器类型：标签选择器，类选择器，ID 选择器，属性选择器，伪类选择器等

五．CSS 中的浮动（float）属性是用来做什么的？

浮动属性用于控制元素在文档流中的位置。通过设置 float 属性为 left 或 right，元素可以脱离文档流并向左或

向右浮动。这通常用于实现多列布局或图文混排效果。

六．CSS 中的伪类和伪元素有什么区别？

伪类用于选择元素的特定状态或行为，伪元素则用于创建并操作元素的特定部分。

语法上的区别是伪类使用单冒号（：），而伪元素使用使用双冒号（：：）。

七．CSS 中的响应式设计是什么？如何实现响应式布局？

响应式设计是根据设备屏幕大小和特性，使网页能够自适应地调整布局和样式。实现响应式布局可以使用媒体查询

，根据不同的屏幕宽度应用不同的 css 样式，或使用弹性布局和网格布局等技术。

八．CSS 中的选择器优先级是如何确定的？

九．选择器优先级是通过计算选择器的特定权重值来确定的。

ID 选择器 > 类选择器 > 属性选择器 > 标签选择器

可以通过使用 ！Important 声明和提高选择器的特定性来增加优先级

十．解释闭包是什么，以及它的工作原理

闭包是指函数能够访问并操作其词法作用域之外的变量的能力。当内部函数引用了外部函数的变量时，就创建了一

个闭包。闭包通过保留对外部函数作用域的引用，使得内部函数在外部函数执行结束后仍然可以访问外部函数的

变量。这种机制使得 JavaScript 中的函数具有了更强大的灵活性和功能。

map 和 forEach 的区别

forEach 方法，是最基本的方法，遍历和循环。默认有 3 个参数：分别是遍历的每一个元素 item，遍历的索引

index，遍历的数组 array

map 方法，和 foreach 一致，不同的是会返回一个新的数组，所以 callback 需要有 return 返回值，如果没

有会返回 undefined

箭头函数和普通函数的区别？

函数体内的 this 对象，就是定义时所在的对象，而不是使用时所在的对象

不可以当作构造函数，也就是说不可以使用 new 命令，否则会报错

不可以使用 arguments 对象，该对象在函数体内不存在，如果要用可以使用 Rest 参数代替

不可以使用 yield 命令，因此箭头函数不能用作 Generator 函数

es6 新增

新增模版字符串

箭头函数

增加 let、const 来声明变量

for-of 用来遍历数据-例如数组中的值

解构赋值

新增简单数据类型 Symbol，独一无二的，不会与其他属性名冲突

将 Promise 对象纳入规范，提供了原生的 Promise 对象

数组方法汇总

map 循环遍历数组、返回一个新的数组

forEach 循环遍历数组，不改变原数组

push/pop 在数组的末尾添加/删除元素 改变原数组

unshift/ shift 在数组的头部添加/删除元素，改变原数组

join 把数组转化为字符串

some 有一项返回为 true，则整体为 true

every 有一项返回为 true，则整体为 false

filter 数组过滤

slice(start, end) 数组截取，包括开头，不包括截取，返回一个新的数组

splice(start, number, value) 删除数组元素，改变原数组

indexof/lastindexof： 查找数组项，返回对应的下标

concat：数组的拼接，不影响原数组，浅拷贝

sort：数组排序 改变原数组

reverse： 数组反转，改变原数组

项目性能优化方案

动态加载组件 component :is="componA" 

减少 http 请求

减少 DNS 查询

使用 CDN

避免重定向

图片懒加载

路由懒加载

减少 DOM 元素操作

使用外部 js 和 css

压缩 js、css、字体、图片等

使用 iconfont 字体图标、雪碧图等

避免图片的 src 为空

把样式表放在 link 中

把 js 放在页面的底部

forEach 和 for 循环的区别

for 循环是通过索引循环遍历每一个元素；而 forEach 是通过 JS 底层程序来实现循环遍历数组元素

for 循环可以通过 break 终止循环；而 forEach 不可以，会报错

for 循环可以通过控制循环变量的数值来控制循环次数；而 forEach 不行

for 循环可以在循环体外调用循环变量；而 forEach 不行

for 循环的执行效率比 forEach 高

==补充：==既然 for 比 forEach 效率高，为何不用 for

原因： for 循环只能通过索引下标数值来操作数组元素，而 forEach 可以设置参数，操作上更加遍历。

实际工作中，可自行根据需要选择

解释 let、var 和 const 之间的区别

et 和 const 具有块作用域，这意味着它们仅限于声明它们的块（例如，在大括号内）。var 具有函数作用域，这

意味着它可以在声明它的整个函数中访问。

const 与 let 类似，但用于在初始分配后不应重新分配的变量。

什么是事件循环？调用堆栈和任务队列有什么区别？

事件循环负责利用单个线程执行 JavaScript 中的操作。它使用调用堆栈来跟踪当前正在执行的操作，并使用任务队

列来管理异步任务。调用堆栈按照后进先出的顺序处理函数，而任务队列则按照先进先出的顺序处理。

块元素和行内元素有什么区别？

块元素被格式化为块并从新行开始，占据可用的整个宽度。它们可以应用宽度、高度、边距和填充属性。

内联元素在文本流中格式化，并且不从新行开始。它们仅根据其内容占用必要的空间，并且不能应用宽度、高度或边

距。

CSS 预处理器 SASS/LESS 有何用途？

SASS 和 LESS 等 CSS 预处理器用于通过添加变量、mixins、嵌套和函数等功能来增强 CSS 的功能。它们允许更高效和模块化的 CSS 开发，从而实现代码重用、改进的组织和更轻松的维护。

事件循环如何处理微观和宏观任务？

事件循环负责处理 JavaScript 中的微任务和宏任务。在事件循环的每次迭代期间，它首先处理所有微任务（例如 Promise 和排队回调），然后再继续处理下一个宏任务。

HTTP GET 和 POST 请求有什么区别？

HTTP GET 和 POST 请求都用于将数据从客户端传输到服务器。但是，GET 请求包括附加到 URL
的请求参数，而 POST 请求包括消息正文中的请求参数。POST 请求对于传输敏感数据更加安全，因为参数在 URL 中不直接可见。
使用回调、promise、await 和 async 处理异步调用。使用每种方法来处理异步调用有何优缺点？

回调提供了处理异步调用的传统方法，但可能导致回调地狱并使代码难以阅读。Promise 提供了更简洁的语法，并允许通过链接和 catch 块等功能更好地处理错误。Async/await 是最近添加的功能，它通过使用异步函数和等待

Promise 来简化异步代码，使代码看起来更加同步且更易于理解。

您能解释一下标签属性，例如“disabled”、“async”、“defer”以及何时使用“data-\_”吗？

“disabled”属性用于禁用元素，防止用户交互。`async` 和 `defer` 属性与脚本标签一起使用来控制外部脚本的执行时间。

`async` 属性允许脚本异步执行，而 `defer` 属性则推迟执行，直到文档解析完成。“data-\_”属性用于存储与元素关联的自定义数据属性，提供了一种无需使用非标准属性或类即可存储附加信息的方法。

您能描述一下渐进增强和优雅降级之间的区别吗？

渐进增强从所有浏览器都可以提供的基本用户体验开始，并针对现代浏览器进行增强。

另一方面，优雅降级从丰富的体验开始，并为旧浏览器优雅降级。

[面试题](1.png)
