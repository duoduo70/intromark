它支持将内嵌的 dot 语言渲染到 markdown 。
```python
compile(filename)                   # 这用于编译某一个文件
compile_all_subprojects_intromark() # 这用于编译所有文件
```
关于内嵌流程图的语法：
```markdown
在 markdown 中使用代码块：
```[graph]
digraph G {
        A -> B
}
```
由 IntroMark 编译后会用一个 SVG 代替这个代码块，任何基于翻译到 HTML 到 markdown 渲染器应该都可以渲染这种内嵌流程图

同时，在使用 `compile_all_subprojects_intromark()` 编译后，会生成一个 `Subproject.md` 文件，用以列出项目的子项目列表，以及它们的简短描述。
