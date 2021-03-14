## 学习笔记

- 四则运算：产出四则运算的词法定义和语法定义。
- 语法分析：把输入的字符串流变成 token
- 语法分析：把 token 变成抽象语法树 AST。
- 解释执行：后序遍历 AST，执行得出结果。

AST定义
- 抽象语法树 AST:是源代码的抽象语法结构的树状表示，树上的每个节点都表示源代码中的一种结构，这所以说是抽象的，是因为抽象语法树并不会表示出真实语法出现的每一个细节，比如说，嵌套括号被隐含在树的结构中，并没有以节点的形式呈现。

四则运算
- Token
    - Number：1 2 3 4 5 6 7 8 9 0 的组合
    - Operator：+、-、*、/ 之一
- Whitespace ：<sp>
- LineTerminator： <LE> <CR>

语法分析：LL
- 一种自上而下分析的方法，第一个 L 表示从左向右扫描，第二个 L 表示分析过程是最左推导。
- 递归的用法。
- MultiplicativeExpression，AdditiveExpression和 Expression的函数处理。