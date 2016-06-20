Web 前端开发技能栈

## 初衷

待补充

## 维护团队

本项目由![伯乐在线](http://www.jobbole.com)团队策划，![@Kenshin](https://github.com/Kenshin) 撰写第一版。如果您感兴趣加入维护团队，请![从这里提交申请](http://group.jobbole.com/category/feedback/skill-set-team/)。谢谢！ 

## 概览

> 阅读提示：本篇文章并没有单纯的罗列出前端开发涉及到的技术栈，而是探寻这些技术栈背后的『秘密』，适合初学者以及想要了解这些『秘密』的阅读者。如仅想了解前端开发技术栈的话，请关注后续的更新

### 开篇：
> 工欲善其事，必先利其器。
> ​                          *出自：《论语·卫灵公》*

### 前言：
由于 JavaScript 的语法很简单，所以上手容易，基本上少则数周就可以开发项目了，但这就是 JavaScript 的全部吗？显然不是！
很多刚接触 JavaScript 开发的程序员，或多或少的都要再继续学习其它的技术栈，如：`grunt / gulp, npm, requre.js / seajs` 等辅助性技术；学习 `prototype / __proto__` 等较晦涩的语法知识；掌握 `MVC / MVP / MVVM` 等设计模式；`Backbone.js / Vue.js / React  / AngularJS` 等框架；`jQuery / Protorype / lodash` 等库。

### 疑惑：
> 一些初学者大多都有这样的想法：我现在可以用 JavaScript 编写程序了，并且也正常上线了，而且运行的也不错，为什么我要再花额外的时间学习这些技术栈呢？

### 答案：
> 上述这些技术栈是为了弥补 JavaScript 在开发大型项目时的短板。

### 疑问：
> JavaScript 作为前端开发领域中最重要的语言，难道无法胜任现在的大型项目开发吗？如果要寻求这个答案，需要我们重新认识 JavaScript 的前世今生。

### 前世：
JavaScript 在创造初期用来（ 脚本形式 ）弥补网页开发的不足。在那个时代，JavaScript 作为诸如： `ASP / JSP` 等开发语言的辅助功能存在，经常使用的场景（ 之一 ） 就是 『表单验证』。
虽然 JavaScript 的缔造者 Brendan Eich 大神早已 『洞悉』了未来，但也无法阻挡 JavaScript 只花 `10天` 创造出来的事实。（ 第一版 ）
那个时代，还没有一个专门从事 JavaScript 开发的职位，前端开发先驱们将更多的精力放在了 『浏览器大战』 之后的兼容性问题上。

### 发展：
浏览器大战之后的另外一个影响，就是推动了 JavaScript 成为国际化标准，即：`ECMAScript` （欧洲标准化组织ECMA（European Computer Manufacturers Association）），后者用来描述 JavaScript 的语法结构，并推动它的发展，前者只是后者的实现方案。（备注：另外一个 ECMAScript 实现方案是 `ActionScript 3.0` ）

### 今生：
随着 `Chrome` 这种现代浏览器的出现，其背后的 JavaScript 解析器（V8）大大增强了 JavaScript 的执行速度/效率。（在 `V8` 的基础上，另外一位大神 Ryan Dahl 发明了 `Node.js`，将本来仅仅运行在浏览器端的语言，发展到了后端开发。）
`jQuery` 的诞生，使前端开发先驱们抽离出『浏览器兼容性问题的泥沼』，有更多的精力来思考 JavaScript 的未来。
网络带宽的增大以及 `Ajax` 技术的出现，使网页具有异步更新的方式，大大的加快了由传统 `B/S` 架构向 `C/S` 架构的探索，`Google Gmail` 的成功进一步推动此项技术成为大型项目的可能性。
最终出现了 `SPA`（ Single Page Application：单页面应用程序 ），至此使用  JavaScript 开发大型项目成为一种趋势和标准。

### 短板：
由于 ECMAScript 推动着 JavaScript 的发展，即便 JavaScript 是上世纪的产物，但使用它开发一个小型的前端项目，其实并不困难。
但是，一个大型的 SPA 项目往往具有 `n个外部引用类库`，`数十个（甚至更多） js/html/css/图片` 等资源组成；多人参与/长时间维护，成千上万行的代码的特点。
显然，这些都是 JavaScript 在最初时所没有考虑过的情况。

### 前端项目的特点：
正如前文描述，技术栈弥补了 JavaScript 在开发大型项目上的短板，所以为了更加清晰的分析技术栈的特点，先从问题入手：
> 一个大型的 JavaScript 项目通常需要解决哪些问题？

- 外部引用包的管理；
- 过多的代码导致的项目更新，迭代，重构难题；
- 多人参与，开发职责区分困难；
- 虽然网络带宽得到了很大的提高，但页面的加载速度仍是问题；
- 静态资源（  html/js/css/图片资源等 ）过多导致上线时的重复性工作量增大；

#### 外部引用包的管理：
JavaScript 先天不具有其它语言的包管理功能，但这并没有阻碍我们伟大的前端开发先驱们的探索，`npm`，`bower` 这类技术栈为我们解决了包管理问题。

#### 过多的代码导致的项目更新，迭代，重构难题：
既然代码过多，就需要使用诸如：`封装`，`继承` 等现代化编程语言的面向对象编程方式。虽然 JavaScript 缔造初期并不是解决这些问题的，但 Brendan Eich 大神显然预见了未来，即在初版的 JavaScript 语言中，就包含了 OO 思想。换言之，JavaScript 是基于对象的开发语言。
虽然都是面向对象，但 JavaScript 与传统的面向对象不太一样，它使用了 `更加高级但晦涩` 的 `继承链` 方式，这就是我们需要理解 `prototype / __proto__`  这些技术栈的原因。

#### 多人参与，开发的职责区分困难：
由于大型 SPA 项目的出现，页面不仅承载了用户行为，更多的是将后端主导的逻辑开发也带到了前端。原本 MVC 中的 『M』比任何以往都要『重』，以至于在 『M』层，又形成了新的框架理论。因此了解并掌握 `MVC / MVP / MVVM` 等设计模式就变成了必要手段，进而 `前端框架` 开始流行。
与其它语言一样，选用现成的前端框架自然变成了趋势，这些现代化框架的『设计思想』包含了前端开发新颖的理念， 如：操作虚拟 DOM（ Virtual DOM ）的 `React`；单纯的践行 MVC 理论的 `Backbone.js`；MVM 风格的 `AngularJS` 等。
学习并掌握前端框架可以更好的区分职责，而框架统一的 `API` 实现了长时间多人开发/维护的可能性。

#### 虽然网络带宽得到了很大的提高，但页面的加载速度仍是问题：
由于`SPA` 是单页面应用，因此页面在加载的时候几乎包含了全部功能，但用户往往却只使用其中的一部分，所以网速的限制，带宽的浪费，用户的等待则是另一个难题。
 『模块化开发』 是解决这类难题的银弹，而 `AMD  / CMD` 的理论自然成为前端开发者们掌握的必要知识，而 `requre.js / seajs` 则是这些理论的具体实现方式。
由于 Http 的特性所致 ( `分散的，小的静态资源在加载的时候更慢` )，因此 `合并/压缩` 则是另外一个解决方案，因此也产生了一个新的问题，即第四个问题。

#### 静态资源（  html/js/css/图片等资源 ）过多导致上线时的重复性工作量增大：
当这类静态资源很少的时候，手动 `合并/压缩` 并没有问题，反之这些资源呈指数上升的时候，手动方案显示不是一个好办法。
`自动化方案` 的引入势在必行，而其中践行者：`grunt / gulp / webpack` 就需要掌握了。

### 思考：
上述大多是『 非官方机构 / 开发者社区 』创造出来的技术栈，推动 JavaScript 发展的 ECMAScript 官方组织在做什么？难道当前 『最in』 JavaScript ，其实是个过时的产物？
> 答案当然是错的，ECMAScript 早已公布了 它的第六个版本：ECMAScript 6（ 2015年6月正式发布 ）

### ECMAScript 6：
它最重要的特性（之一）就是包含了：Class（ `原生 OOP` ） 和 Module（ `原生模块化` ）方案。

### 结论：
不掌握这些技术也可以实现 JavaScript 开发，但掌握了这些技术栈可以使我们从 『繁重 / 繁琐』的事务中抽离出来，更加 『专注于业务逻辑』。
>  上述技术的掌握能使我们更好的融入现代化的前端开发中来。

### 结语：
如果你看到这里的话，那么恭喜你，**欢迎来到新世界！！！**
> ![新世界](http://ksria.qiniudn.com/jobbole/%E6%96%B0%E4%B8%96%E7%95%8C.jpg)

### 彩蛋1：
上述列举的知识点仅仅属于前端技术栈的一部分，除此以外还包括了：`调试/测试`，`性能优化`，`CSS预编译方式`，`编码规则`，`SEO`，`移动 Web 开发` 等。

### 彩蛋2：
掌握这些技术后就万事无忧了吗？当然不，随着前端开发的发展，总有一天，这些技术仍无法满足开发。所以要了解这些技术栈背后的理论逻辑，以不变应万变，方为制胜之道！

### 彩蛋3：
- 相似的技术栈，如何取舍？
- 只要是大型项目就都需要这些技术栈吗？
- 为什么使用了框架后，还是觉得开发慢？
- 使用了 xxx 后，并没有实际解决我的问题？

想弄懂它们？请关注后续的更新。

### 参考文献：
- ECMAScript is an object-oriented [出处](http://www.ecma-international.org/ecma-262/5.1/index.html#sec-4)
- ECMAScript 6 语言描述 [出处](http://www.ecma-international.org/ecma-262/6.0/index.html)
- ECMAScript 6 浏览器兼容表 [链接](http://kangax.github.io/compat-table/es6/)
- 浏览器兼容性问题 [链接](https://zh.wikipedia.org/wiki/%E6%B5%8F%E8%A7%88%E5%99%A8%E5%85%BC%E5%AE%B9%E6%80%A7) 及 浏览器大战 [链接](https://zh.wikipedia.org/zh/%E6%B5%8F%E8%A7%88%E5%99%A8%E5%A4%A7%E6%88%98)
- Chrome V8 解析器 [链接](https://en.wikipedia.org/wiki/V8_(JavaScript_engine))


