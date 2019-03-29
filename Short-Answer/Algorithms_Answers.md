# Algorithms Answers

## Exercise I

a) O(n), because the number of operations in the while loop grows in accordance to the input n.

Examples:

```
n = 1
(while a < 1)
a = 0 + 1 = 1
(1 loop)
```

```
n = 3
(while a < 27)
a = 0 + 9 = 9
a = 9 + 9 = 18
a = 18 + 9 = 27
(3 loops)
```

```
n = 10
(while a < 1000)
a = 0 + 100 = 100
a = 100 + 100 = 200
a = 200 + 100 = 300
a = 300 + 100 = 400
a = 400 + 100 = 500
a = 500 + 100 = 600
a = 600 + 100 = 700
a = 700 + 100 = 800
a = 800 + 100 = 900
a = 900 + 100 = 1000
(10 loops)
```

b) O(n^4), as there are four nested loops written in this function.

c) O(n), because it is preforming the same number of operations (adding 2 ears per bunny) no matter how big the integer passed in gets
