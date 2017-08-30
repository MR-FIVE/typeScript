##TypeScript 是微软2012年推出的一种编程语言，属于 JavaScript 的超集，可以编译为 JavaScript 执行。 它的最大特点

##首先，安装TypeScript。

##$ npm install -g typescript(注意一定是全局安装，局部安装本人亲测 > -bash: tsc: command not found)
##然后，为变量指定类型。

`// greet.ts
function greet(person: string) {
  console.log("Hello, " + person);
}

greet([0, 1, 2]);`
##上面是文件 greet.ts 的代码，后缀名 ts 表明这是 TypeScript 的代码。函数 greet 的参数，声明类型为字符串，但在调用时，传入了一个数组。
##使用 tsc 命令将 ts 文件编译为 js 文件，就会抛出类型不匹配的错误。

`$ tsc greeter.ts
greet.ts(5,9): error TS2345: Argument of type 'number[]'   
is not assignable to parameter of type 'string'.`
