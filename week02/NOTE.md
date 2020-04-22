# 总结
## 第一次课
> 学习了`乔姆斯基谱系`，`BNF`，`图灵完备性`，`动态语言与静态语言`，`类型系统`
### 乔姆斯基谱系
#### 定义
乔姆斯基体系是由诺·乔姆斯基于1956年提出的，是刻画形式文法表达能力的一个分类谱系。
#### 分类
+ 0-型文法（无限制文法或短语结构文法）包括所有的文法。
+ 1-型文法（上下文相关文法）生成上下文相关语言。
+ 2-型文法生成上下文无关语言。
+ 3-型文法（正规文法）生成正规语言。


### BNF
#### 定义
巴科斯范式 以美国人巴科斯(Backus)和丹麦人诺尔(Naur)的名字命名的一种形式化的语法表示方法，用来描述语法的一种形式体系，是一种典型的元语言。又称巴科斯-诺尔形式(Backus-Naur form)。
#### 规则
非终结符用尖括号括起。每条规则的左部是一个非终结符，右部是由非终结符和终结符组成的一个符号串，中间一般以“：：=”分开。具有相同左部的规则可以共用一个左部，各右部之间以直竖“|”隔开。

### 图灵完备性
+ [什么是图灵完备？](https://www.zhihu.com/question/20115374)
图灵完备性（Turing Completeness）是针对一套数据操作规则而言的概念。数据操作规则可以是一门编程语言，也可以是计算机里具体实现了的指令集。当这套规则可以实现图灵机模型里的全部功能时，就称它具有图灵完备性。直白一点说，图灵完备性包括无限内存、if/else 控制流、while 循环……

### 动态语言与静态语言
### 类型系统

## 第二次课
> 学习了`Unicode`，`WhiteSpace`，`LineTerminator`，`Comment`，`Token`，`IdentifierStart`，`IdentifierPart`，`Types`
- Literal
- Variable
- Keywords
- Unicode
    ```javascript
      for(let i = 0; i < 128; i++) {
        console.log(i + ": " + String.fromCharCode(i));
      }
      
      
      console.log("厉害".codePointAt(0).toString(16)); // "5398"
      
      console.log("\u5389"); "厉"
    ```
- WhiteSpace
  - \<TAB> 
  - \<VT>
  - \<FF>
  - \<SP>
  - \<NBSP>
  - \<BOM>
  - \<USP> 
- LineTerminator
  - \<LF>
  - \<CR>
  - \<LS>
  - \<PS> 
- Comment
  - MultiLineComment
  - SingleLineComment
- Token
  - IdentifierName
  - Punctuator
  - NumericLiteral
  - StringLiteral 
- IdentifierStart
  - UnicodeLetter
  - $
  - _
  - \ UnicodeEscapeSequence 
- IdentifierPart
  - IdentifierStart
  - UnicodeCombiningMark
  - UnicodeDigit
  - UnicodeConnectorPunctuation
  - \<ZWNJ>
  - \<ZWJ> 
- Types
  + Number
    IEEE754 双精度浮点64位数
     + 常见进制
        + 十进制
        + 二进制
        + 八进制
        + 十六进制 
    + 安全整数
    + 浮点数比较
  + String
    + 字符
    + code point
    + 字符编码
      + ASCII
      + Unicode
      + UTF-8
      + UTF-16
  + Boolean
  + Null
  + Undefined