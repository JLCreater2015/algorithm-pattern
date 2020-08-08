# c语言到c++

## 1、Class与Struct

 C++中的 struct 和 class 基本是通用的，唯有几个细节不同：

* 使用 class 时，类中的成员默认都是 private 属性的；而使用 struct 时，结构体中的成员默认都是 public 属性的。
* class 继承默认是 private 继承，而 struct 继承默认是 public 继承。
* class 可以使用模板，而 struct 不能。

## 2、函数重载

函数重载就是指： 在同一作用域类，一组函数的函数名相同，参数列表不同（个数不同或类型不同），返回值可同可不同。C 语言不存在函数重载， C++支持函数重载，属于静多态。

比如一个函数声明如下： `void function(int x, int y);` 

在 C 语言中，编译器进行编译之后，在库中的名字为： `_function` ，在 C++中，编译器在进行编译之后，在库中的名字为： `_function _int_int` 。

编译器在链接的阶段，都是找到相应的函数名，进行链接。 在 C 语言中，两个函数的名字一样，就会在链接时报错。 在 C++中，两个函数饿名字不相同，就不会报错。

 函数的重载的规则：

* 函数名称必须相同。
* 参数列表必须不同（个数不同、类型不同、参数排列顺序不同等）。
* 函数的返回类型可以相同也可以不相同。
* 仅仅返回类型不同不足以成为函数的重载。
