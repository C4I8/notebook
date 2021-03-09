# ES6
## Array
### 管道函数    
#### Array.prototype.filter()    
##### filter() 方法创建一个新数组, 其包含通过所提供函数实现的测试的所有元素。
                console.log([1, 2, , 3].filter(value => value > 1))
                //excepted output: [2,3]
#### Array.prototype.map()
##### map() 方法创建一个新数组，新数组元素结果是原数组中的每个元素传入提供的函数并调用后的返回值。    
                console.log([1, 2, 3].map(value => value * 2))
                //excepted output: [2,4,6]
#### Array.prototype.reduce()      
##### reduce() 方法对数组中的每个元素执行一个由您提供的reducer函数(升序执行)，将其结果汇总为单个返回值。
                let initialValue = 0;
                console.log([1, 2, 3, 4].reduce((accumulator, value, index, arr) => { return accumulator + value }, 0));
                // 0 + 1 + 2 + 3 + 4
                // excepted output: 10
第一次执行*reducer*时,accumulator为数组的第一个元素或者传入的参数initialValue