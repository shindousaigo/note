#### sass提供了四个编译风格的选项
* nested：嵌套缩进的css代码，它是默认值。
* expanded：没有缩进的、扩展的css代码。
* compact：简洁格式的css代码。
* compressed：压缩后的css代码。

#### 基本用法
* 变量
    ```
    $blue: #1875e7;　
    div {
        color: $blue;
    }

    $side: left;
    .rounded {
        border-#{$side}-radius: 5px;    
    }
    ```
* 计算
    ```
    body {
        margin: (14px/2);
        top: 50px + 100px;
        right: $var * 10%;
    }
    ```
* 嵌套
    ```
    一般嵌套~
                                div {
    div (>)h1 {                        (>)h1 {
        color: #000;    --->            color: #000;
    }                               }
                                }

    伪类选择器~
    a {
        &:hover {
            color: #ffb3ff;
        }
    }
    ```
* 注释
    ```
    SASS共有两种注释风格。
    标准的CSS注释 /* comment */ ，会保留到编译后的文件。
    单行注释 // comment，只保留在SASS源文件中，编译后被省略。
    ```

#### 代码重用
* 继承
    ```
    .class_base {
        border: 1px solid #ddd;
    }
    .class_extend {
        @extend .class_base;    
        font-size:120%;
    }
    ```
* Mixin
    ```
    SASS共有两种注释风格。
    标准的CSS注释 /* comment */ ，会保留到编译后的文件。
    单行注释 // comment，只保留在SASS源文件中，编译后被省略。
    ```
