# 常考的关键字

## ✏ 1、`auto`

在早期C/C++中`auto`的含义是：使用auto修饰的变量，是具有自动存储器的局部变量。C++11中，`auto`有了全新的含义即：`auto`不再是一个存储类型指示符，而是作为一个新的类型指示符来指示编译器，`auto`声明的变量必须由编译器在编译时期推导而得。通俗地讲，`auto`关键字是可以自动推导变量类型的。

> auto不是一个类型的“声明”，而是一个“占位符”，编译器在编译期会将`auto`替换为变量实际的类型。使用`auto`定义变量时必须对其进行初始化，在编译阶段编译器需要根据初始化表达式来推导`auto`的实际类型。它自动推导变量类型是根据`“=”`右侧的变量类型决定的。

### 使用规则

**1. auto与指针和引用结合起来使用**

用`auto`声明指针类型时，用`auto`和`auto*`没有任何区别，但用`auto`声明引用类型时则必须加`&`。

**2. 在同一行定义多个变量**

当在同一行声明多个变量时，这些变量**必须是相同的类型，**否则编译器将会报错，因为编译器实际只对  
第一个类型进行推导，然后用推导出来的类型定义其他变量。 

**3. auto不能作为函数的参数**

参数要被编译成指令，但是开辟空间时候需要知道空间大小，`auto`做参数不知道多大，那么栈帧也不知道开多大。

**4. auto不能直接用来声明数组**

因为数组也涉及大小，在下面的例子中，a的类型严格来说是 int \[3\]，所以b的大小也不确定。

```cpp
int a[] = {1,2,3};
auto b[3] = a;
```

**5. auto在实际中最常见的优势用法是C++11提供的新式for循环，还有lambda表达式等进行配合使用。**

**6. auto不能定义类的非静态成员变量。**

**7. 实例化模板时不能使用auto作为模板参数。**

## ✏ **2、mutable**

\*\*\*\*

## ✏ **3、static**

\*\*\*\*

## ✏ **4、volatile**

\*\*\*\*

## ✏ **5、extern**
