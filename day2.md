<h1 align="center"> Day 2 (Flutter Excelr)</h1>

## Data Types

> Always prefer `var` to declare variables

### Built-in types

1. Numbers --> num (int, double)

   ```dart
       var x = 5;
       var y = 3.6;

       //num variables can hold both int and double values
       num x = 1;
       num y = 5.6;

       int a = 1.2; // error
       double b = 5;
   ```

2. Booleans --> bool (true, false)

3. Strings --> String

   ```dart
       String singleQuote = 'allowed';
       String doubleQuote = "also allowed";
       String multiLine = '''
           This is
           multi line
           string in dart''';
       String rawString = r"It is raw string \n will not work here";
   ```

### Collections / Iterables

1. Lists --> (List, array in other languages)

   > A List is an ordered group of items.

   ```dart
       var list = [1, 2, 3, 'Boat',];
       var constantList = const [1, 2, 3];
       var emptyList = [];

       // copy one list to another using spread operator [...]
       var list2 = [...list];

   ```

2. Sets --> (Set)

   > A Set is an unordered group of `unique` items

   ```dart
       var primeSet = {1, 3, 17};
       var emptySet = {}; // Creates an empty map, not a set
       var emptySet = <String>{};

       // copy one set to another using spread operator {...}
       var set2 = {2, ...primeSet};
   ```

3. Maps --> (Map)

   > A Map is an unordered collection of `key:value` pairs, similar to a dictionary in Python

   ```dart
       var map = {
           1: 'dart',
           2: 'flutter',
       };

       var emptyMap = {};

       // copy one map to another using spread operator {...}
       var map2 = {0: 'english', ...map};
   ```

### Control-flow operators(`if` and `for`) with Collections

```dart
    var list = [1, 2, 3, 4, 5];

    // Using if in a collection
    var evenList = [for (var i in list) if (i % 2 == 0) i];
    print(evenList); // prints: [2, 4]

    // Using for in a collection
    var incrementedList = [for (var i in list) i + 1];
    print(incrementedList); // prints: [2, 3, 4, 5, 6]
```

## Type Casting in Dart

```dart
    // implicit type casting or type inference (auromatically detect type of variable)
    var num = 5;

    // String -> int
    var one = int.parse('1'); // explicit type casting
    print(one); // 1

    // String -> double
    var onePointOne = double.parse('1.1'); // explicit type casting
    print(onePointOne); // 1.1

    // int -> String
    String oneAsString = 1.toString(); // explicit type casting
    print(oneAsString); // '1'

    // double -> int
    double myDouble = 123.45;
    int myInt = myDouble.toInt();
    print(myInt); // 123
```

## Operators

1. Arithmetic Operators (+, -, \*, /, %, ~/, -const)

   - `[~/ in dart ➡ // in Python]`

2. Relational Operators (<, >, <=, ==, !=, etc)

3. Type Test Operators (is, is !)

   ```dart
   String name = 'Ram';
   // prints true
   print(name is String);
   ```

4. Bitwise Operators (&, |, ~, ^, <<, >>)

5. Assignment Operators (=, ??=)

   ```dart
       // ??= [Assign value to x if it is null; otherwise, x stays the same]

       var x;
       x ??= 5; // Value is assigned as x is null
       x ??= 10; // Value is not assigned as x is not null
   ```

6. Logical Operators (&&, ||, !)

   > - Logical operators are only applicable to boolean expressions
   > - non-zero numbers are not considered as true and zero as false
   > - 0 and 1 are not boolean instead int

7. Conditional Operators / Ternary operators (?: and ??)

   - (condition ? expr1 : expr2)
     > If condition is true, evaluates expr1 (and returns its value); otherwise, evaluates and returns the value of expr2
   - (expr1 ?? expr2)
     > If expr1 is not-null, returns its value; otherwise, evaluates and returns the value of expr2

   ```dart
       int a = 5, b = 8;
       a > b ? print(a) : print(b);

       String? name; // made name nullable using ?
       String nameToUse = name ?? 'Guest'; // Null coalescing operator
   ```

8. Cascade Notation Operator (..)

   > used to perform multiple method calls or multiple operations on same object

   ```dart
   class MyClass {
       void methodA() {
           print('Method A');
       }

       void methodB() {
           print('Method B');
       }
   }

   void main() {
       MyClass myObject = MyClass();

       // without using cascade notation
       myObject.methodA();
       myObject.methodB();

       // Using cascade notation
       myObject
        ..methodA()
        ..methodB();
   }

   // output
       Method A
       Method B
   ```
<h1 align="center"> <a href="/day3.md">Day 3 notes</a></h1>