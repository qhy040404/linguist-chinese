# linguist-chinese

.gitattributes中linguist相关用法，相关文件类型的示例在对应文件夹中

## 合并计算

* 将某一种语言计算进其他语言的代码量中
> 示例：
```gitattributes
*.rb linguist-language=Java #将Ruby代码计算进Java代码量中
```

## 引用代码 / 他人供应代码

* 可以使用此属性排除不是自己编写的代码
> 示例1 （包含jQuery）
```gitattributes
js/jquery.js linguist-vendored=false
```
> 示例2 （将某个文件夹标记为此类代码）
```gitattributes
js/* linguist-vendored
```

## 文档

* 可以使用此属性来排除文档，或者将文档计入 （例如Markdown）
> 示例1 （将某个文件夹标记为文档）
```gitattributes
docs/* linguist-documentation
```
> 示例2 （将某个文件取消标记为文档）
```gitattributes
README.md linguist-documentation=false
```

## 编译生成的临时文件

* 可以使用此属性来排除编译临时文件
> 示例 （排除pyc文件）
```gitattributes
*.pyc linguist-generated=true
```

## 可检测的文件

* 可以使用此属性来决定此文件或者类型是否被检测
> 示例1 （检测Markdown）
```gitattributes
*.md linguist-detectable=true
```
> 示例2 （不检测example.py）
```gitattributes
example.py linguist-detectable=false
```
