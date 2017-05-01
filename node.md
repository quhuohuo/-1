## 为什么要用node?
### 优点
#### 1.采用事件驱动、异步编程，为网络服务而设计。其实Javascript的匿名函数和闭包特性非常适合事件驱动、异步编程。而且JavaScript也简单易学，  
很多前端设计人员可以很快上手做后端设计。
#### 2.Node.js非阻塞模式的IO处理给Node.js带来在相对低系统资源耗用下的高性能与出众的负载能力，非常适合用作依赖其它IO资源的中间层服务。
#### 3.Node.js轻量高效，可以认为是数据密集型分布式部署环境下的实时应用系统的完美解决方案。Node非常适合如下情况：在响应客户端之前，  
您预计可能有很高的流量，但所需的服务器端逻辑和处理不一定很多。
### 缺点
#### 可靠性低
#### 单进程，单线程，只支持单核CPU，不能充分的利用多核CPU服务器。一旦这个进程崩掉，那么整个web服务就崩掉了

## node的构架是什么样子的?
#### 主要分为三层，应用app >> V8及node内置架构 >> 操作系统. V8是node运行的环境，可以理解为node虚拟机．node内置架构又可分为三层: 核心模块(javascript实现) >> c++绑定 >> libuv + CAes + http.


## node有哪些核心模块?
#### http,console,fs,events,buffer,assert,global,process,EventEmitter, Stream, Net



## node有哪些全局对象?
#### 1.global: 最根本的作用是为全局变量的宿主. 表示Node所在的全局环境.
#### 2.process：该对象表示Node所处的当前进程，允许开发者与该进程互动。
#### 3.console：指向Node内置的console模块，提供命令行环境中的标准输入、标准输出功能。
#### 4.exports: 
#### 全局变量有两个
#### __filename：指向当前运行的脚本文件名。
#### __dirname：指向当前运行的脚本所在的目录。

## process有哪些常用方法?
#### process.stdin, process.stdout, process.stderr, process.on, process.env, process.argv,   
process.arch, process.platform, process.exit
#### process.stdout是标准输出流，通常我们使用的 console.log() 向标准输出打印字符，而 process.stdout.write() 函数提供了更底层的接口。
#### process.stdin是标准输入流，初始时它是被暂停的，要想从标准输入读取数据，你必须恢复流，并手动编写流的事件响应函数。
#### process.stderr：指向标准错误
#### process.pid：当前进程的进程号。
#### process.argv：当前进程的命令行参数数组。
#### process.exit()：退出当前进程。
#### process.cwd()：返回运行当前脚本的工作目录的路径。_
#### process.chdir()：改变工作目录。
#### process.nextTick()：将一个回调函数放在下次事件循环的顶部。

## console有哪些常用方法?
#### console.log/console.info, console.error/console.warning, console.time/console.timeEnd, console.trace, console.table

## node有哪些定时功能?
#### setTimeout/clearTimeout, setInterval/clearInterval, setImmediate/clearImmediate, process.nextTick


## Promise 中 .then 的第二参数与 .catch 有什么区别?
#### 

## Eventemitter 的 emit 是同步还是异步?
#### 是同步的
