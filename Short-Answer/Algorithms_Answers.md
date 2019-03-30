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

## Exercise II

In order to use the least amount of eggs to find out the value of floor _f_, I would propose the following algorithm:

```
def find_value_of_f(num_floors):
    if num_floors <= 1:
        return 0 # can't break an egg if it's on the ground!

    low_floor = 0
    high_floor = num_floors

    while low_floor <= high_floor:
        test_floor = (low_floor + high_floor) // 2

        if egg.thrown_off_of(test_floor) != 'broken':
            low_floor = test_floor + 1

        elif egg.thrown_off_of(test_floor) == 'broken':
            if egg.thrown_off_of(test_floor - 1) != 'broken':
                return test_floor - 1
            else:
                high_floor = test_floor - 1

    return 0 # assuming we went through the whole building and broke every egg
```

By doing this, you would not need to go through each floor and test to see if the egg will break when dropped,minimizing the amount of eggs you have to drop. The time complexity of this algorithm would be **O(log n)**, as the number of eggs you'll have to use would not increase by that much as the number of floors gets larger.
