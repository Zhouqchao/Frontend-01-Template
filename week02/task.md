+ 写一个正则表达式 匹配所有 Number 直接量
  ```js
    var reg = /((((0|[1-9]([0-9]+)?)\.([0-9]+)?([eE][+-]?[0-9]+)?|\.[0-9]+([eE][+-]?[0-9]+)?|(0|[1-9]([0-9]+)?)([eE][+-]?[0-9]+)?)|0[bB][01]+|0[oO][0-7]+|0[xX][0-9a-fA-F]+))/g
  ```
+ 写一个 UTF-8 Encoding 的函数
  ```js
    functionUTF8_Encoding(string){
      //return new Buffer();
    }
  ```

+ 写一个正则表达式，匹配所有的字符串直接量，单引号和双引号
  ```js
    var reg = /"(?:[^"\n\\\r\u2028\u2029]|\\(?:['"\\bfnrtv\n\r\u2028\u2029]|\r\n)|\\x[0-9a-fA-F]{2}|\\u[0-9a-fA-F]{4}|\\[^0-9ux'"\\bfnrtv\n\\\r\u2028\u2029])*"/g
  ```