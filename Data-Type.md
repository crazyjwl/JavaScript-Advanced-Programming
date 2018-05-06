- Five simple data types(also calle *primitive types*)
  5种简单数据类型（基本数据类型）
  1. Undefined
  2. Null
  3. Boolean
  4. Number
  5. String
&nbsp;
- One complex data type
  1种复杂数据类型
  - Object
&nbsp;
- 对一个值使用 **typeof** 操作符将会返回以下某个字符串：
 "undefined" / "string" / "number" / "object" / "function"
  Usage/示例：
  ```javascript
    var message = "welcome";
    alert(typeof message);    //"string"
    alert(typeof(message));   //"string"
    alert(typeof 100);        //"number"

  ```
- 在使用 *var* 声明变量但未初始化时，变量值为undefined

- null值表示一个空对象**指针** （`typeof null == object`）

- 任何数值除以非数值会返回*NaN*，*NaN* 与任何值不相等，包括它自身。

- 数值的转换（非数值转化为数值）：
    - `Number（）`：
    ```javascript
    var num1 = Number("Hello World");   //NaN
    var num2 = Number("");              //0
    var num3 = Number("66666");         //66666
    var num4 = Number(true);            //1
    ```
    - `parseInt()`:
    ```javascript
    var num1 = parseInt("1234Hi");      //1234
    var num2 = parseInt("");            //NaN
    var num3 = parseInt("0xA");         //10 (十六进制)
    var num4 = parseInt(22.5);          //22
    var num2 = parseInt("070");         //56 (八进制)
    var num2 = parseInt("70");          //70 (十进制)
    var num2 = parseInt("0xf");         //15 (十六进制)
    var num2 = parseInt("AF",16);       //175 十六进制
    var num2 = parseInt("AF");          //NaN
    ```
    - `parseFloat()`:

    ```javascript
    var num1 = parseFloat("1234Hi");      //1234
    var num2 = parseFloat("0xA");         //0
    var num3 = parseFloat("66.0");        //66
    var num4 = parseFloat("66.6");        //66.6
    var num5 = parseFloat("66.6.6");      //66.6
    var num6 = parseFloat("0606.6");      //606.6
    var num7 = parseFloat("3.124e5");     //312400
    ```
- String类型（值转换为字符串）
    - `toString()`方法
    *null* 和 *undefined* 没有这个方法
    ```javascript
    var age = 11;
    alert(age.toString());      //"11" 字符串

    var found = true;
    alert(found.toString());    //"true" 字符串

    var num = 10;
    alert(num.toString());      //"10"
    alert(num.toString(2));     //"1010"
    alert(num.toString(8));     //"12"
    alert(num.toString(16));    //"a"
    ```
    -  `String()`方法
        - 适用于不知道要转换的值是否为*null*或*undefined*的情境
        - 如果值有`toString()`方法，则调用（无参）方法并返回结果
        - 如果值为*null*，则返回 "null"
        - 如果值为*undefined*，则返回 "undefined"
&nbsp;
- Object类型：对象是一组“数据”和“功能”的组合
   - 创建自定义对象:
    ``` javascript
    var o = new Object();
    ```
   - Oject的每个实例都有下列属性和方法：
        - `constructor:  Object()` 保存着用于创建当前对象的函数
        - `hasOwnProperty(propertyName)` 用于检查给定的属性在当前对象实例中（非其原型中）是否存在
        - `isPrototypeOf(object)` 用于检查传入的对象是否是当前对象的原型
        - `propertyIsEnumerable(propertyName)` 用于检查给定的属性是否能够使用 `for-in` 语句来枚举
        - `toLocalString()` 返回对象的字符串表示，与执行环境的地区对应
        - `toString()` 返回对象的字符串表示
        - `valueOf()` 返回对象的字符串、数值或布尔值表示
