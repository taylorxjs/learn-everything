# 一、基础篇

## 1.基础介绍

JUnit 是一个开放的资源框架，用于编写和运行测试。

- 提供注解来识别测试方法。
- 提供断言来测试预期结果。
- JUnit 测试允许你编写代码更快，并能提高质量。
- JUnit 优雅简洁。没那么复杂，花费时间较少。
- JUnit测试可以自动运行并且检查自身结果并提供即时反馈。所以也没有必要人工梳理测试结果的报告。
- JUnit测试可以被组织为测试套件，包含测试用例，甚至其他的测试套件。
- JUnit在一个条中显示进度。如果运行良好则是绿色；如果运行失败，则变成红色

官网地址：https://github.com/junit-team

> JUnit4：https://junit.org/junit4/，入门文档：https://github.com/junit-team/junit4/wiki/Assertions
>
> JUnit5：https://junit.org/junit5/，入门文档：https://junit.org/junit5/docs/current/user-guide/#overview
>
> 测试样例：https://github.com/junit-team/junit5-samples

## 2.常用注解

**@Test** 表示方法是一种测试方法。 与JUnit 4的@Test注解不同，此注释不会声明任何属性。

**@ParameterizedTest** 表示方法是参数化测试

**@RepeatedTest** 表示方法是重复测试模板

**@TestFactory** 表示方法是动态测试的测试工程

**@DisplayName** 为测试类或者测试方法自定义一个名称

**@BeforeEach** 表示方法在每个测试方法运行前都会运行 ，**@AfterEach** 表示方法在每个测试方法运行之后都会运行

**@BeforeAll** 表示方法在所有测试方法之前运行 ，**@AfterAll** 表示方法在所有测试方法之后运行

**@Nested** 表示带注解的类是嵌套的非静态测试类，**@BeforeAll**和 **@AfterAll**方法不能直接在@Nested测试类中使用，除非修改测试实例生命周期。

**@Tag** 用于在类或方法级别声明用于过滤测试的标记

**@Disabled** 用于禁用测试类或测试方法

**@ExtendWith** 用于注册自定义扩展，该注解可以继承

**@FixMethodOrder(MethodSorters.NAME_ASCENDING)**，控制测试类中方法执行的顺序，这种测试方式将按方法名称的进行排序，由于是按字符的字典顺序，所以以这种方式指定执行顺序会始终保持一致；不过这种方式需要对测试方法有一定的命名规则，如 测试方法均以testNNN开头（NNN表示测试方法序列号 001-999）

