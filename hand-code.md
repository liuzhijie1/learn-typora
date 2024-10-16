# Hand-Code

![hand-code](/images/hand-code.png "hand-code")

## 树

### 二叉树的最大深度

```javascript
function TreeNode(val, left, right) {
  this.val = (val === undefined ? 0 : val)
  this.left = (left === undefined ? null : left)
  this.right = (right === undefined ? null : right)
}

var maxDepth = function(root) {
  if (!root) return null;
  let ret = 1;
  function dfs(root, depth) {
    if (!root.left && !root.right) ret = Math.max(ret, depth);
    if (root.left) dfs(root.left, depth + 1)
    if (root.right) dfs(root.right, depth + 1)
  }
  dfs(root, 1)
  return ret;
}
```

## Javascript 基础

### 手写Object.create

``` javascript
function create(obj) {
  function F();
  F.prototype = obj
  return new F();
}
```  

### 手写 instanceOf 方法

``` javascript
function myInstanceof(left, right) {
  let proto = Object.getPrototypeOf(left),
      prototype = right.prototype;
  while(true) {
    if (!proto) return false;
    if (proto == prototype) return true;

    proto = Object.getPrototypeOf(proto);
  }
}
```  

### 手写 new 操作符

**在调用 new 的过程中会发生以上四件事情**

* 首先创建一个空对象
* 设置原型，将对象的原型设置为函数的 protottype 对象
* 让函数的 this 指向这个对象，执行构造函数的代码（为这个新对象添加属性）
* 判断函数的返回值类型，如果是值类型，返回创建的对象。如果是引用类型，就返回这个引用类型的对象

``` javascript
function objectFactory() {
  let newObject = null
  let constructor = Array.prototype.shift.call(arguments);
  let result = null
  // 判断参数是否是一个函数
  if (typeof constructor !== 'function') {
    console.error('type error');
    return;
  }

  // 新建一个空对象，将对象的原型为构造函数的 prototype 对象
  newObject = Object.create(constructor.prototype);
  // 将 this 指向新建对象，并执行函数
  result = constructor.apply(newObject, arguments);
  // 判断返回对象
  let flag = result && (typeof result === 'object' || typeof result == 'function');

  return flag ? result : newObject;

}
```

### 手写 Promise

``` javascript
const PENDING = 'pending'
const RESOLVED = 'resolved'
const REJECTED = 'rejected'

function MyPromise(fn) {
  var self = this;
  this.state = PENDING;
  this.value = null;
  this.resolvedCallbacks = [];
  this.rejectedCallbacks = [];
  function resolve(value) {
    if (value instanceof MyPromise) {
      return value.then(resolve, reject)
    }
    setTimeout(() => {
      if (self.state === PENDING) {
        self.state = RESOLVED;
        self.value = value;
        self.resolvedCallbacks.forEach(callback => {
          callback(value);
        })
      }
    }, 0)
  }

  function reject(value) {
    setTimeout(() => {
      if (self.state === PENDING) {
        self.state = REJECTED;
        self.value = vlaue;
        self.rejectedCallbacks.forEach(callback => {
          callback(value);
        })
      }
    }, 0)
  }

  try {
    fn(resolve, reject);
  } catch (e) {
    reject(e)
  }
}

MyPromise.prototype.then = function(onResolved, onRejected) {
  onResolved = typeof onResolved === 'function' ? onResolved : function(value) {
    return value;
    }

  onRejected = typeof onRejected === 'function' ? onRejected : function(error) {
    return error;
  }

  if (this.state === PENDING) {
    this.resolvedCallbacks.push(onResolve)
    this.rejectedCallbacks.push(onRejected)
  }

  if (this.state === RESOLVED) {
    onResolved(this.value)
  }
  if (this.state === REJECTED) {
    onRejected(this.value)
  }
}

```

### 手写防抖函数

``` javascript
function debounce(fn, wait) {
  let timer = null;

  return function() {
    let context = this, args = arguments;

    if (timer) {
      clearTimeout(timer)
      timer = null
    }

    timer = setTimeout(() => {
      fn.apply(context, args);
    }, wait)
  }
}
```  

### 手写节流函数

``` javascript
function throttle(fn, delay) {
  let curTime = Date.now();

  return function() {
    let context = this, args = arguments, nowTime = Date.now();

    if (nowTime - curTime >= delay) {
      curTime = Date.now();
      return fn.apply(context, args)
    }
  }
}
```

### 手写类型判断函数

``` javascript
function getType(value) {
  // 判断数据是 null 的情况
  if (value === null) {
    return value + '';
  }
  if (typeof value === 'object') {
    let valueClass = Object.prototype.toString.call(value),
        type = valueClass.split(" ")[1].split("");
    type.pop();
    return type.join("").toLowerCase();
  } else {
    return typeof value;
  }
}
```  

## 排序算法

### 冒泡排序

``` javascript
function bubbleSort(arr) {
  let len = arr.length;
  for (let i = 0; i < len; i++) {
    for (let j = 0; j < len - 1 - i; j++) {
      if (arr[j] > arr[j + 1]) {
        let temp = arr[j + 1];
        arr[j + 1] = arr[j];
        arr[j] = temp;
      }
    }
  }
}
```

### 二分排序 (快速排序)

``` javascript
function quickSort(arr) {
    if (arr.length <= 1) {
        return arr; // 如果数组长度小于等于1，直接返回
    }

    const pivotIndex = Math.floor(arr.length / 2); // 选择基准值的索引
    const pivot = arr[pivotIndex]; // 基准值
    const left = []; // 存放小于基准值的元素
    const right = []; // 存放大于基准值的元素

    for (let i = 0; i < arr.length; i++) {
        if (i === pivotIndex) continue; // 跳过基准值本身
        if (arr[i] < pivot) {
            left.push(arr[i]); // 小于基准值的放左边
        } else {
            right.push(arr[i]); // 大于基准值的放右边
        }
    }

    // 递归调用并合并结果
    return [...quickSort(left), pivot, ...quickSort(right)];
}

// 测试代码
const array = [7, -2, 4, 1, 6, 5, 0, -4, 2];
console.log(quickSort(array)); // 输出排序后的数组
```

### javascript 原生排序法

``` javascript
let arr = [3,2,1,5,4]
arr.sort((a, b) => a - b);
```
