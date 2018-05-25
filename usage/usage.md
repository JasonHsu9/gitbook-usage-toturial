### 创建 mygitbook 工作目录
```bash
# 创建 mygitbook 文件夹，并切换到这个文件夹下面
~$ mkdir mygitbook && cd mygitbook
```
### 初始化 mygitbook 工作目录
```bash
~$ gitbook init
warn: no summary file in this book
info: create README.md
info: create SUMMARY.md
info: initialization is finished
```
这时你会得到这样一个目录结构,在[目录结构](../directory/directory.md)一文中会对目录结构详细解读。

**这两个文件可以预先手动创建，然后在执行`gitbook init`。此时手动创建的文件内容，会替代程序默认内容并一直存在，除非主动删除它，否则在执行gitbook相关命令时，它都会完整的保存，不用担心会被覆盖。**
```
|--README.md
|--SUMMARY.md
```

### mygitbook书籍预览
初始化后，就可以得到一本书籍的雏形，执行以下命令：
```bash
gitbook serve #两条命令就写一本书，有木有很爽
```


会生成_book静态网站,并在本地`http://localhost:4000`生成预览服务，此时可在浏览器预览GitBook书籍
`gitbook serve -p 5000` 当打开多本GitBook书籍时，可像这样自定义端口，以避免冲突。

### SUMMARY.md语法

* SUMARRY.md中的列表式超链接语法，渲染出来时，去掉了列表样式前面的黑点。

* 不要在列表格式链接外包含其他语法，会使当前行不被编译到目录中，亲测。

* 目录没有超链接时，直接在列表标记后写文字就行

* SUMMARY.md文件内容皆以星号开始(虽然不加也不会报错，不过统一加上)，后面可以是超链接，也可以是纯文本。

* 用缩进4个半角字符表示章和节层级关系，文件章节皆用超级连接表示
链接中不存在的文件或文件夹，编译时会被自动创建。

