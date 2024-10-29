## Interviews

### 海石-2024-08-百世集团

1. 说说你对js闭包的理解
2. 说说你对浏览器事件循环的理解 [juejin](https://ulj5gfpntt.feishu.cn/drive/folder/B7Z5f622jliRsfdtvRucB6mUnBc?from=from_copylink)
3. 宏任务和微任务有哪些  **注意判断RAF是宏任务还是微任务**
4. 密集型计算任务该怎么办，如何让他不阻塞页面渲染 [webworker](https://ulj5gfpntt.feishu.cn/drive/folder/B7Z5f622jliRsfdtvRucB6mUnBc?from=from_copylink)
5. webWorker的使用
6. 如果现在后端返回了十万条数据，期望你渲染，你该怎么做，都有哪些方式？  [juejin](https://juejin.cn/post/7407763018471948325)
7. 阻止iframe中的点击事件，都有哪些方式 [juejin](https://juejin.cn/post/7411799494415941666)
8. Promise中存在多个resolve，会执行哪一个，还是都不执行 [juejin](https://juejin.cn/post/7411799494415941666)
9. 打开页面a, 存在一个定时器，比如倒计时5秒，之后切换页面，访问页面b,停留3秒，之后又切换页面，访问页面a,请问此时页面a的定时器的倒计时是否还准确？如果不准确，如何让他准确？
10. 项目中Console.log 比较多怎么办？[juejin](https://juejin.cn/post/7417710863711649832)  不用正则你会怎么做？
11. 说说你项目中的难点和亮点

### 海石-2024-08-SSW

1. 全英文自我介绍
2. 说说为什么在项目中使用graphQL

### 海石-2024-08-浙江大华

1. 说一说js中的变量提升 [juejin1](https://juejin.cn/post/7375152719483650082) [juejin2](https://juejin.cn/post/7405260565679603721)
2. 谈一谈如何实现一个深拷贝 [juejin1](https://juejin.cn/post/7402922513888362548) [juejin2](https://juejin.cn/post/7405536151288053769)
3. 既然聊到了关于递归内存泄漏的问题，请介绍下垃圾回收机制，说出你知道的几种机制，并讲讲优劣 [juejin](https://juejin.cn/post/7405536151288053769#heading-10)
4. 如何创建一个真正空的对象
   1. Object.create(null)
   2. let a = {}; a.\_\_proto\_\_ = null
5. 如何让一个对象无法被修改？ [juejin](https://juejin.cn/post/7405260565679603721#heading-9)
6. 你做过登录功能，请你讲一讲怎么对用户密码做加密的
   1. MD5
   2. sha-2
   3. sha-3
7. http和https的区别
   1. S代表ssl/tls, 分别对应着对称加密和非对称加密，为什么对称加密不安全，中间人劫持，非对称加密一定安全吗？中间人可以伪造公钥和私钥，进行双端欺骗，由此引入CA证书，CA的公钥是嵌在操作系统中的，以此确保不会伪造
   2. 但是这样也有问题，那就是操作系统漏洞，被人植入了一些有害的CA公钥，这就又能让中间人进行欺骗了。
8. 讲一讲css中display: none和visible: hidden的区别
9. 讲一讲position,他有几个值？ sticky使用过吗？

### 海石-2024-09-酷家乐

1. 说说你最有难点的项目，如何克服的？ bpmn-js项目
2. 说一说你是如何理解bpmn的，能解释一下这个名词吗？
3. 如何完成组件封装，从那些层面考虑
4. 我不希望创建的实例对象后续在被修改，如何去做？
5. 聊一聊桌面端应用electron,工作原理，如何发布版本，部署
6. 请讲一讲你是如何实现水印组件的
7. 请讲一讲你实现的令你印象深刻的hook组件

### 海石-2024-09-探迹科技

#### 一面

1. 说说你知道的性能优化，尽可能多地去说 [wendnag](https://ulj5gfpntt.feishu.cn/docx/Is8gdqeuGofi1Hx96kEcVCYOnKc)
2. 为什么不能在useEffect的第一个参数中的函数体内部使用await?
   1. 因为此时就得给函数声明async,那么函数返回的就是一个Promise对象
   2. useEffect期望第一个参数返回一个函数，这样方便在卸载阶段完成一些清理工作，比如变量的释放等等，但是假如第一个参数返回的不是函数，而是Promise，就会影响useEffect在卸载阶段的工作了
3. 如果我给useEffect的第二个参数不传任何值，注意区分，不是传个空数组，而是不传如何值，会怎么样
   1. 会在首次渲染即挂载阶段调用，之后每一次re-render都会调用
4. 说一下fiber架构吧，diff算法全过程
5. 说一下useState是如何生效的
6. 你对useCallback的使用心得

#### 二面

1. 说一说你实际在项目中应用的性能优化方法
2. 说一说webpack，他做了什么？
3. loader和plugin的区别
4. 如何优化webpack的构建过程
5. tree-shaking原理
6. react的lazy import的原理
7. 聊一聊对你来说有难点的项目

### 海石-2024-10-合合信息

1. 请你说说你对于html语义化的理解
   1. 有利于seo,搜索引擎将其内容是为影响页面搜索排名的重要关键字
      1. 搜索引擎爬取网页，跟随页面之间的链接，并索引找的内容，搜索时，搜索引擎会显示索引内容，爬行者遵守规则，如果你在为网站进行搜索引擎优化时密切关注这些规则，则会为网站提供最好的机会，以便在首批结果中显示，增加流量和可能的收入（用于电子商务和广告）
2. 请你说说strong和b 那个更具备语义化
   1. Strong,还代表加强语气
3. DOMContendLoaded和window.onload区别
   1. DOMContentLoaded事件在DOM树构建完成时触发，不包括样式表，图片和子框架的加载。
   2. window.onload 事件在整个页面包括所有依赖资源如样式表，图片等都加载完成后触发
4. DomContentloaded和onLoad事件的区别和对async，defer关键字的处理的异同
   1. **async**： 当脚本使用 async 属性时，脚本会在下载完成后立即执行，不会阻塞 HTML 的解析。此时，脚本执行的顺序不一定与它们在文档中的位置相同。对事件的影响：
如果使用 async 加载的脚本在 DOMContentLoaded 事件触发之前执行，可能会导致在 DOM 完成解析之前就尝试访问 DOM 元素，从而引发错误
   2. **defer**使用 defer 属性时，脚本会在文档解析完成后按顺序执行。即使多个脚本使用了 defer，它们仍然会保持原有的顺序。对事件的影响：所有使用 defer 的脚本会在 DOMContentLoaded 事件之后执行，因此可以安全地访问和操作 DOM。
5. 对于dom来说，element和node的区别
   1. element是node的一种，指的是HTML或XML文档中的元素节点，而node是更广泛的概念，包括元素节点、文本节点、注释节点等
6. less 和 sass那个可以客户端编译
   1. less可以sass不行
7. js事件循环
8. js事件流、事件委托、实现事件委托的特性是什么？
   1. target和currenTarget
9. 往html中插入节点的方法
10. html,input标签的onChange和input事件的区别
11. input标签的name属性是什么？
12. html, dom的props和attribute的区别
13. 标准盒模型和怪异盒模型，margin会计算宽度吗？
    1. 怪异： border + padding + 内容
14. css动画，说说如何实现平移，并在完成平移后触发回调 [juejin](https://code.juejin.cn/pen/7425549072540368937)
15. css变量有用过吗？

``` css
:root {
  --primary-color: red;
  --padding-large: 20px;
  --font-stack: 'UI'
}
body {
  font-family: var(--font-stack);
  color: var(--primary-color);
  padding: var(--padding-large);
}
.button {
  background-color: var(--primary-color);
  color: white;
  padding: var(--padding-large);
}
```

16. css使用grid布局绘制一个九宫格
17. css使用flex如何实现左边固定，右边自适应
18. css的position属性有哪些
    1. static
    2. relative
    3. absolute
    4. fixed
    5. sticky
19. css如何开启gpu加速

```css
可以通过使用css的transform、opacity等属性来开启gpu加速、
.element {
  transform: translate(0,0,0);
}
```

20. RAF用过吗？ 说说他的执行时机？
    1. requestAnimationFrame
    2. 在浏览器绘制之前执行
21. meta标签中的viewport设置有什么用？
    1. 用于缩放
22. 在typescript中，any,unknown,never的区别
    1. 在typescript中，any,unknown,never是三种不同的类型，他们在类型系统中扮演着不同的角色
    2. **any**: 类型关闭了类型检查，允许赋值和接受任何类型的值
    3. **unknown**: 类型提供了类型安全性，要求在使用前进行类型检查
    4. **never**: 类型表示那些永不存在的值，通常用于不可能有返回值的函数

### 海石-2024-10-京东

#### 一面jd

1. 说下let, const的区别，能说多少说多少，能有多个角度就说多个角度，说到说不出来为止
2. CORS是什么，怎么用，原理是什么，原理很复杂，没有我说的这么简单
3. For和ForEach的区别，能说多少说多少，能有多少个角度就说多个角度，说到说不出来为止，性能上，等等
4. Promise.all和Promise.race区别，能说多少说多少，能有多个角度就说多个角度，如果Promise.all有任务失败了怎么解决
5. 生成器和迭代器，如果在for语句中使用生成器，会有什么不同呢？
6. 闭包的好处和坏处？使用场景，说到说不出来为止
7. async和await和Promise的区别，为什么要用async和await,实现原理是什么？
8. 生成器，yield,ok，那你说一说为什么能够中断一个函数的执行，不是它的作用，我知道他能中断函数的执行，那么为什么呢？
9. Promise捕获错误的方法，await后面能接上catch方法吗？除了 try catch之外，还有什么能够捕获错误的方法？
10. 类组件和函数组件的区别？能说多少说多少，能有多个角度就说多个角度，说到说不出来为止
11. 类组件的this我们经常用，我们却从不在函数式组件中使用，为什么？围绕类组件的this,说到说不出来为止
12. 函数式组件真的没有生命周期吗?
13. useEffect的第二个参数，什么都不传，会怎么样？
14. css中的flex布局，在什么情况下默认的轴会变，flex:1的彻底吊打，要求很细节
15. es5之前如何实现一个私有变量？
16. 手写题，写一个监听屏幕宽度和高度变化的hook，要考虑性能

``` jsx
import {useState, useEffect, useRef} from 'react';

function useSubWindowChange(element) {
  const [dimensions, setDimensions] = useState({
    width: element ? element.offsetWidth : window.innerWidth;
    height: element ? element.offsetHeihgt : window.innerHeihgt;
  });

  const timer = useRef(null);

  const handleResize = () => {
    if (element) {
      setDimensions({
        width: element.offsetWidth,
        height: element.offsetHeight
      })
    } else {
      setDimensions({
        width: window.innerWidth,
        height: window.innerHeight
      })
    }
  }

  useEffect(() => {
    const resizeListener = () => {
      if (timer.current) {
        clearTimeout(timer.current)
      }
      timer.current = setTimeout(handleResize, 1000)
    };

    window.addEventListener('resize', resizeListener)

    return () => {
      window.removeEventListener('resize', resizeListener);
      if (timer.current) {
        clearTimeout(timer.current)
      }
    }
  }, [element]);

  return dimensions
}

```

#### 二面jd

1. 说说你从0到1负责的项目
2. 说说什么时候适合使用websocket
   1. 全双工通信，双向同时互传数据的角度，和持久性链接的角度，数据的实时性，和性能的角度去回答
3. 实现需求的前期工作你会做哪些？
4. 性能优化
5. 平常写代码的时候，你都会注意哪些方面
6. 组件封装，组件封装的原则，说一个你亲手封装的组件，你都做了那些工作
7. 如果我期望这个组件更加通用，你该怎么改造
8. 分享一下你的简历中提到的，你认为最亮眼的项目
9. 分享一下你最近遇到的一个最难解决的bug，以及你是如何去解决的

### 海石-2024-10-食享

1. 说一说垃圾回收机制
2. 说说你理解的React Fiber
3. 简历汇总提到的某个量化数据是怎么计算得出的
4. [笔试题](https://code.juejin.cn/pen/7426274777028886538)
5. 针对项目，说说你这个项目的难点都有哪些，你是怎么去做的
6. webpack HMR原理
7. 说说js的基本数据类型有哪些，原始值和引用类型的区别是什么？
8. [笔试题](https://code.juejin.cn/pen/7426650890453483560)

```jsx
// 代码题1
function fn() {
  console.log(this);
}
const obj1 = { a: 1 }
const obj2 = { a: 2 }
const obj3 = { a: 3 }
const obj4 = { a: 4 }
const obj5 = { a: 5 }
fn.bind(obj1).bind(obj2).bind(obj3).bind(obj4).call(obj5)
// 判断输出的this
// output {a: 1}
// 因为只有第一次bind会对 fn生效，后续的bind都是bind给了return的新函数，不会影响到fn
// call和apply回调用，bind不会会优先返回一个函数
```

``` jsx
// 提供一个公共函数 myAdd, 要求能够解决小数精度问题

function myAdd(num1, num2) {
  const [, decimals1] = num1.toString().split('.')
  const [, decimals2] = num2.toString().split('.')

  if (decimals1 && decimals2) {
    const factor = Math.max(decimals1.length, decimals2.length) * 10;

    return (num1 * factor + num2 * factor) / factor
  } else {
    return num1 + num2;
  }
}
```

**场景题3**

现在要实现一个定时开启抽奖的功能，你会怎么做，说说你的方案？不要让用户早点进来，也不要让用户晚点进来，还有人一直在刷页面，考虑时区，考虑准确性，考虑各种层面，服务端，客户端
**solve** 不仅可以通过技术手段，实在不行，还可以通过产品手段

1. setTimeout和setInterval的准时性 [juejin](https://juejin.cn/post/6844904022051127310?searchId=2024102322382855E03C88D02AD7AB4D9F)
   1. 其实都不准，会受到事件循环的影响。当定时器到期之后，回调函数被添加进宏任务队列中，假如出队的回调函数执行时间较长,那么就会影响后续回调函数的执行，这就导致本该同时在100毫秒内到期执行的定时器任务，会出现任务A执行，任务B可能等到180毫秒才执行的现象

``` jsx
// 使用RAF模拟setTimeout
function rafTimeout(func, delay) {
  let start = Date.now();
  const handleRaf = () => {
    if (Date.now() - start >= delay) {
      func()
    } else {
      requestAnimationFrame(handleRaf)
    }
  };
  requestAnimationFrame(handleRaf)
}

rafTimeout(() => {
  console.log('延迟1秒后执行')
}, 1000)


// 使用RAF模拟setInterval

function rafInterval(func, delay) {
  let start = Date.now();
  const handleRaf = () => {
    if (Date.now() - start >= delay) {
      func();
      start = Date.now()
    }
    requestAnimationFrame(handleRaf)
  }
  requestAnimationFrame(handleRaf)
}

rafInterval(() => {
  console.log('每秒执行一次')
}, 1000)

```

9. 性能优化, 如何做到fcp的优化，不说具体的实现细节，而是聊一聊做性能优化的步骤。除了lighthouse, performance会使用吗？判断自己做的优化行为，在渲染时间，比如4秒钟的占比？你会如何判断？fcp的4秒渲染那些是必要的开销，那些是非必要的，可以优化的开销？你可以告诉这个项目打开之后，时间消耗在什么地方？[优化1](https://juejin.cn/post/7382768099252715520) [优化2](https://juejin.cn/post/7222642085405048890)

### 海石-2024-10-腾讯音乐

1. 说说你这个Electron项目
2. Electron是什么，为什么选择他？
3. 说说你是怎么做H5的？
4. 为什么选择使用react native去做呢？实现的方式还有很多
5. 原生和其他方式的区别是什么？
6. 你觉的react native和react的区别是什么
7. react native的实现原理你知道吗？
8. 项目中使用到了bit.dev,为什么选择使用它？
9. 项目的国际化怎么实现的？
10. 你知道i18next加载词条资源的原理吗
11. i18next的按需加载是如何实现的？
12. 看到你的项目里也是用到了websocket,使用的时候有没有遇到一些问题，如何解决问题？
13. 看到你的难点里写了优化Fullcalendar的渲染，你是怎么优化的？
14. 为什么选择Fullcalendar，技术选型的时候有调研过其他第三方库吗？
15. 前端埋点有做过吗？sentry的原理是什么？
16. 水印组件你是怎么实现的？
17. 如何实现水印组件的点击传递
18. 还有什么你简历上的难点和亮点，是我没有问到的，你可以主动聊一聊
19. 说说你了解的性能优化都有哪些措施？
20. 说说你为什么选择加入上家公司

### 海石-2024-10-字节跳动

1. 自我介绍，
2. 看你有在博客进行知识分享，你认为哪些知识点是亮点，比如你刚提到的组件封装
3. 聊聊组件库的按需加载，他们是如何实现的，比如实现样式上的按需加载，组件层面的按需加载等等
4. react组件中的key值的作用？
5. 为什么不能用index作用key值？
6. 你认为什么场景下适合用inde作为key值，什么场景下不适合？
7. 详细说说index作为key值后，可能会产生的影响
8. **必问题**：性能优化的具体实践，比如你是怎么做首屏优化的？ 怎么完成性能指标的计算、然后定位问题、然后去解决问题、实现优化的？
9. 抛开其他的封装、改造、请你说说js原生如何发起接口请求？
10. 你们公司平常是怎么去实现接口请求的，怎么封装的？
11. 看到你实现过水印组件，那你说说z-index,他是什么，使用它要注意什么？
12. 说说你为什么自研一个水印组件，以及你是怎么实现的？
13. 你知道什么是暗水印吗？
14. React事件机制 [react查漏](https://ulj5gfpntt.feishu.cn/docx/Y6n7dcyC6oypuNxU2sZcV17Xnqc)
15. 写出ts的enum类型被编译后的js产物
16. 手写题：输入一个root和number，返回查找到number的完整路径

``` jsx
const root = [{id: 1, children: [{ id: 2, children: [{ id: 4, children: []}]}, {
  id: 3,
  children: [{ id: 6, children: []}]
}]}]

// findPaths(root, 6)
// Output: [1, 3, 6]
```
