# SEO

## MicroData

Itemscope:  itemscope is a boolean global attribute that defines the scope of associated metadata. This ususlly goes with itemtype attribute

Itemtype: itemtype specifies the URL of the vocabulary that will be used to define itemprop's (item properties) in the data structure, for Example: [http://schema.org/Thing](http://schema.org/Thing)   Thing is the type

### MetaData 和 MicroData 的区别

#### MetaData

定义： metadata 是描述数据的数据，通常用于提供关于网页的信息，如标题、描述、关键字等。

```markdown
作用：

+ SEO优化： 元数据帮助搜索引擎理解网页内容，从而提高搜索排名，常见的元数据包括`<meta>` 标签，如`description`、`keyword`, `viewport`等
+ **社交媒体分享**：元数据可以定义网页在社交媒体上分享时的显示内容，例如Open Graph 和 Twitter Card元数据
+ **文档信息**：提供关于文档的其他信息，如作者，版权信息等。
```

#### Microdata

定义：Microdata 是一种在HTML 中嵌入结构化数据的方式，允许开发者为页面内容添加额外的语义信息，使其更易于被搜索引擎和其他应用程序理解。

```markdown
+ **结构化数据**：Microdata 通过使用`itemscope`、`itemtype` 和 `itemprop` 等属性来描述内容，例如，可以使用microdata标记一个产品的信息，包括名称、价格和描述
+ 最强搜索结果： 使用microdata 可以使搜索引擎在结果中显示丰富的摘要（如星级评分、价格等），从而提高点击率
+ 支持语义网： Microdata 有助于实现语义网的目标，使机器更好的理解和处理网页内容
```
