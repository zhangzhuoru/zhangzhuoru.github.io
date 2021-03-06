# 第9章：构建并部署高性能JavaScript应用 #

## Apache AntP163 ##

Apache Ant是一个软件构建自动化工具。

## 合并多个JS文件 ##

一个简单的优化方法时把部分文件和代码合并成一个外链文件，从而大大降低页面渲染所需的HTTP请求数。

Apache Ant提供了合并多个文件的`concat`任务。JS文件通常需要按照特定的依赖顺序连接在一起。依赖关系一旦确定，使用`filelist`或`fileset`元素集合能保存文件顺序。

## 预处理JS文件P166 ##

## JS压缩P168 ##

将局部引用存储在对象/值中、用闭包封装代码、使用常量替代重复值、避免`eval`(`Function`)等、`with`关键字、JScript条件注释精简文件。

## 构建时处理与运行时处理的对比 ##

只要是能够在构建时完成的工作，就不要留到运行时去做。

## JS的HTTP压缩 ##

当Web浏览器请求一个资源时，它通常会发送一个`Accept-Encoding`的HTTP头来告诉Web服务器它支持哪种编码转换类型。

Accept-Encoding可用的值包括：`gzip`、`compress`、`deflate`和`identity`。

**gzip**是目前最流行的编码方式。Gzip压缩主要适用于文本，包括JS文件。

## 缓存JS文件P171 ##

## 处理缓存问题P172 ##

## 使用内容分发网络CDN ##

## 部署JS资源 ##

## 敏捷JS构建过程P174 ##

## 小结 ##

构建并部署Web应用的过程中最重要的步骤：

- 合并JS文件以减少HTTP请求数
- 压缩JS文件
- 在服务端压缩JS文件（Gzip编码）
- 通过正确设置HTTP响应头来缓存JS文件，通过向文件名增加时间戳来避免缓存问题
- 使用CDN提供JS文件；CDN不仅可以提升性能，还可以管理文件的压缩和缓存





