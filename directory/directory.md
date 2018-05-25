## 整书目录结构
<hr />
这里的目录是gitbook程序的工作目录 `mygitbook` 而不是生成的静态站点 `_book` 目录
```
|--README.md   
|--SUMMARY.md
|--book.json
|--_book
|--otherfile...
```

* README.md  项目介绍写在这里，会被编译到 `_book` 文件夹的 `index.html` 文件
* SUMMARY.md 项目目录，整个项目目录结构由此文件决定
* book.json  配置文件，必须放项目根目录
* _book      `gitbook serve` 或者 `gitbook build` 生成的静态站点文件夹
* otherfile...


### SUMMARY.md文件
整个`mygitbook` 项目的目录除了上述基本不变的目录结构，还有一些目录完全是由 `SUMMARY.md` 文件的内容决定的。

> 可以说`SUMMARY.md` 是整个书籍源码的核心，是它的骨架。我们只需要编写好目录文件代码，繁琐的**创建各种文件和文件夹**就交给 gitbook 程序自己吧。

**通用 `SUMMARY.md` **

为了节省时间，一般的项目我们可以用通用的 `SUMMARY.md` 文件。然后做适当的修改，即可瞬间创建一本 gitbook 电子书的原型
```
# Summary

* [bookName](README.md)
* [前言](PREFACE.md)
* [第1章 入门](chapter1/README.md)
    * [1-1 前端的发展](chapter1/quarter1-1.md)
    * [1-2 常见的构建工具及对比](chapter1/quarter1-2.md)
    * [1-3 安装与使用](chapter1/quarter1-3.md)
    * [1-4 使用 Loader](chapter1/quarter1-4.md)
    * [1-5 使用 Plugin](chapter1/quarter1-5.md)
    * [1-6 使用 DevServer](chapter1/quarter1-6.md)
    * [1-7 核心概念](chapter1/quarter1-7.md)
* [第2章 实战](chapter2/README.md)
    * [2-1 Entry](chapter2/quarter2-1.md)
    * [2-2 Output](chapter2/quarter2-2.md)
    * [2-3 Module](chapter2/quarter2-3.md)
    * [2-4 Resolve](chapter2/quarter2-4.md)
    * [2-5 Plugins](chapter2/quarter2-5.md)
    * [2-6 DevServer](chapter2/quarter2-6.md)
    * [2-7 其它配置项](chapter2/quarter2-7.md)
    * [2-8 整体配置结构](chapter2/quarter2-8.md)
    * [2-9 多种配置类型](chapter2/quarter2-9.md)
    * [2-10 配置总结](chapter2/quarter2-10.md)
* [第3章 实战](chapter3/README.md)
    * [3-1 使用 ES6](chapter3/quarter3-1.md)
    * [3-2 使用 TypScript 语言](chapter3/quarter3-2.md)
    * [3-3 使用 Flow 检查器](chapter3/quarter3-3.md)
    * [3-4 使用 Scss](chapter3/quarter3-4.md)
    * [3-5 使用 PostCSS](chapter3/quarter3-5.md)
    * [3-6 使用 React 框架](chapter3/quarter3-6.md)
    * [3-7 使用 Vue 框架](chapter3/quarter3-7.md)
    * [3-8 使用 Angular2 框架](chapter3/quarter3-8.md)
    * [3-9 为单页应用生成HTML](chapter3/quarter3-9.md)
    * [3-10 管理多个单页应用](chapter3/quarter3-10.md)
    * [3-11 构建同构应用](chapter3/quarter3-11.md)
    * [3-12 构建 Electron 应用](chapter3/quarter3-12.md)
    * [3-13 构建Npm模块](chapter3/quarter3-13.md)
    * [3-14 构建离线应用](chapter3/quarter3-14.md)
    * [3-15 搭配 Npm Script](chapter3/quarter3-15.md)
    * [3-16 检查代码](chapter3/quarter3-16.md)
    * [3-17 通过 Node.js API 启动 Webpack](chapter3/quarter3-17.md)
    * [3-18 使用 Webpack Dev Middleware](chapter3/quarter3-18.md)
    * [3-19 加载图片](chapter3/quarter3-19.md)
    * [3-20 加载 SVG](chapter3/quarter3-20.md)
    * [3-21 加载 Source Map](chapter3/quarter3-21.md)
    * [3-22 实战总结](chapter3/quarter3-22.md)
* [第4章 优化](chapter4/README.md)
    * [4-1 缩小文件搜索范围](chapter4/quarter4-1.md)
    * [4-2 使用 DllPlugin](chapter4/quarter4-2.md)
    * [4-3 使用 HappyPack](chapter4/quarter4-3.md)
    * [4-4 使用 ParalleUglifyPlugin](chapter4/quarter4-4.md)
    * [4-5 使用自动刷新](chapter4/quarter4-5.md)
    * [4-6 开启模块热替换](chapter4/quarter4-6.md)
    * [4-7 区分环境](chapter4/quarter4-7.md)
    * [4-8 压缩代码](chapter4/quarter4-8.md)
    * [4-9 CDN加速](chapter4/quarter4-9.md)
    * [4-10 使用 Tree Shaking](chapter4/quarter4-10.md)
    * [4-11 提取公共代码](chapter4/quarter4-11.md)
    * [4-12 按需加载](chapter4/quarter4-12.md)
    * [4-13 使用 Prepack](chapter4/quarter4-13.md)
    * [4-14 开启 Scope Hoistin](chapter4/quarter4-14.md)
    * [4-15 输出分析](chapter4/quarter4-15.md)
    * [4-16 优化总结](chapter4/quarter4-16.md)
* [第5章 原理](chapter5/README.md)
    * [5-1 工作原理概括](chapter5/quarter5-1.md)
    * [5-2 输出文件分析](chapter5/quarter5-2.md)
    * [5-3 编写 Loader](chapter5/quarter5-3.md)
    * [5-4 编写 Plugin](chapter5/quarter5-4.md)
    * [5-5 调试 Webpack](chapter5/quarter5-5.md)
    * [5-6 原理总结](chapter5/quarter5-6.md)
* [附录](appendix/README.md)
    * [常用 Loaders](appendix/usual-loaders.md)
    * [常用 Plugins](appendix/usual-plugin.md)
    * [其它 Webpack 学习资源](appendix/other-webpack-learning-resource.md)
```
>创建这样的目录结构最好的思路是在 `Chrome` 控制台用 `JavaScript` 的嵌套 for 循环来完成章和节的输出，由 `\n` 控制换行 由于时间关系，我先把此方法 JavaScr`ipt 的位置留在这里，往后一定不上

```js
for(let i=1; i<10; i++)
{
    //some code...
}
```

