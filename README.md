[//]: # (source: https://github.com/ema-mil/style_guide)

# Style Guide

## Contents
 
 - [Formatting](#formatting)
    - [Alignment](#alignment)
    - [Brackets](#brackets)
    - [Characters Per Line](#characters-per-line)
    - [Const](#const)
    - [Empty Lines](#empty-lines)
    - [Indentation](#indentation)
    - [Namespaces](#namespaces)
    - [Single Line Rules](#single-line-rules)
    - [Spaces](#spaces)
    - [Templates](#templates)
 - [Naming](#naming)
    - [Case](#case)
    - [Prefix](#prefix)
    - [Suffix](#suffix)
 - [Best Practices](#best-practices)

## Formating

### Alignment

Don't align anything except the following:

 - If arguments/parameters doesn't fit in a line:
   - Break after open brackets and place the closing bracket to a new line.
   - Place each arugment/parameter in a separated line.
 ```cpp
 void int foo(
     unsigned int value_one,
     unsigned int value_two,
     unsigned int value_three
 )
 {
    // Code...
 }
 
 foo(
     value_one,
     value_two,
     value_three
 );
 ```

 - Align array of structures to the left:

 ```cpp
 std::array<my_struct, 3> list =
 {
     {56, 23,    "hello"},
     {-1, 93463, "world"},
     {7,  5,     "!!"   }
 };
 ```

 - Align operands:

 ```cpp
 int aaa = bbbbbbbbbbbbbbb
         + ccccccccccccccc;
 ```

 - Align lambdas scope relative to the indentation of the outer scope:

 ```cpp
 someMethod([]()
 {
   return;
 });
 ```

 - Align pointers and references to the left:

 ```cpp
 // Good
 int* ptr_one;
 int& ref_one;

 // Bad: Aligned to the right
 int *ptr_two;
 int &ref_two;
 ```

 - Align initializer list comma to the left:

 ```cpp
 constructor()
    : initializer1()
    , initializer2()
 ```

 - Align inheritence list comma to the left:

 ```cpp
 class foo
    : base1
    , base2
 {

 }
 ```

### Brackets

Always use brackets, even for short statements.

Always break before brackets.

Example:

```cpp
// Good
for (std::size_t i = 0; i < 100; ++i)
{
    std::cout << i << '\n';
}

// Bad: No break before brackets
for (std::size_t i = 0; i < 100; ++i) {
    std::cout << i << '\n';
}

// Bad: No brackets used
for (std::size_t i = 0; i < 100; ++i)
    std::cout << i << '\n';
```

### Characters Per Line

Each line must have a maximum of `80` characters.

### Const

Put const when you can except for member variables and copy parameters.

### Empty lines

Max empty line to keep: `1`

### Indentation

Use `4` spaces for indenting your code.

Don't use tabs.

Don't indent pre processor directives.

Don't indent `public`, `protected` and `private` keywords.

Don't indent `case` keyword.

### Namespaces

Don't indent namespaces.

If a namespaces have more then one line:

Place a comment with the name of namespace at the end of its brackets.

### Single Lines Rules

Never put everything into a single line except:

 - Short compound requirement
 - Short lambdas

### Spaces 

Put a space between `for`, `if`, `else if`, `while` keywords and open brackets.

Put a space after C style casts.

### Templates

Always use concepts in templates when you can.

## Naming

### Case

Use `underscore_style` everywhere except for macros.

For macros use `UPPER_CASE`.

### Prefix

Put `m_` as prefix in all non public member variables.

### Suffix 

Put `_t` as suffix for all defined types.

Defines types are types defined with:
 - `typename` keyword.
 - `using` keyword.
 - `typedef` keyword.
 
## Best practices:

Raccomented best practices:

[Jason Turner Best Practices](https://github.com/cpp-best-practices/cppbestpractices)

[C++ Core Guidelines](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines)

