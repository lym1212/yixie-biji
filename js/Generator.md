## Generator 函数

- ES6 提供的一种异步编程解决方案
- 封装了多个内部状态的的状态机 / 遍历器对象生成函数
- 执行 Generator 函数会**返回一个遍历器对象**，可以遍历 Generator 函数内部的每一个状态
- 两个特征：
  - `function` 关键字与函数名之间有一个星号 *
  - 使用 `yeild` 表达式，定义不同的内部状态

- 调用 遍历器对象的`next()` 方法，指针指向下一个状态，返回一个对象，有 value 和 done 两个属性
- 赋值时不会执行，调用 `next()` 才会执行

## yeild 表达式

- 暂停标志
- 遇到 yeild 表达式， 就暂停执行后面的操作，并返回跟在后面的值作为 value 的属性值
- 直到遇到 return 语句，如果没有 return 语句，返回的 value 值为 undefined
- yeild 后面的表达式，只有调用了 `next()` 才会执行
- 只能用在 Generator 函数中
- 如果用在另一个表达式之中，必须放在圆括号里

