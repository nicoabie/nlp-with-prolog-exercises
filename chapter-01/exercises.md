# Exercises

## Ex 1.

No, it does not make a difference changing the order of the facts.

## Ex 2.
The effect produced by this change is that once we reach a final node there is no possibility of backtracking.
Suppouse we change the following arcs:

```prolog
arc(1,3,harry).
arc(1,3,ron).
arc(1,3,hermione).
```
The graph will now look as this:

<img src='https://g.gravizo.com/svg?digraph%20G%20%7B%0A%20%20%20%20rankdir%3DLR%3B%0A%20%20%20%201%20%5Bshape%3Dcircle%5D%3B%0A%20%20%20%201%20-%3E%202%20%5Blabel%3D%22a%7Cthe%22%5D%3B%0A%20%20%20%202%20-%3E%202%20%5Blabel%3D%22brave%7Cfast%22%5D%3B%0A%20%20%20%202%20-%3E%203%20%5Blabel%3D%22witch%7Cwizard%7Cbroomstick%7Crat%22%5D%3B%0A%20%20%20%203%20%5Bperipheries%3D2%5D%3B%0A%20%20%20%203%20-%3E%201%20%5Blabel%3D%22with%22%5D%3B%0A%20%20%20%201%20-%3E%203%20%5Blabel%3D%22harry%7Chermione%7Cron%22%5D%3B%0A%20%20%7D'>

Test1 is able to parse now [ron, with, harry] however test3 only sees that 1 is an initial node and 3 is a final node and it stops there, unable to go back to the node 1 as test1 does.

## Ex 3.

<img src='https://g.gravizo.com/svg?digraph%20G%20%7B%0A%20%20%20%20rankdir%3DLR%3B%0A%20%20%20%201%20%5Bshape%3Dcircle%5D%3B%0A%20%20%20%201%20-%3E%202%20%5Blabel%3D%22aaaa%22%5D%3B%0A%20%20%20%202%20-%3E%202%20%5Blabel%3D%22a%22%5D%3B%0A%20%20%20%202%20-%3E%203%20%5Blabel%3D%22bbb%22%5D%3B%0A%20%20%20%203%20-%3E%203%20%5Blabel%3D%22b%22%5D%3B%0A%20%20%20%203%20-%3E%204%20%5Blabel%3D%22b%22%5D%3B%0A%20%20%20%204%20%5Bperipheries%3D2%5D%3B%0A%20%20%7D'>

<img src='https://g.gravizo.com/svg?digraph%20G%20%7B%0A%20%20%20%20rankdir%3DLR%3B%0A%20%20%20%201%20%5Bshape%3Dcircle%5D%3B%0A%20%20%20%201%20-%3E%202%20%5Blabel%3D%22aa%22%5D%3B%0A%20%20%20%202%20-%3E%202%20%5Blabel%3D%22a%22%5D%3B%0A%20%20%20%202%20-%3E%203%20%5Blabel%3D%22cc%22%5D%3B%0A%20%20%20%203%20-%3E%204%20%5Blabel%3D%22bb%22%5D%3B%0A%20%20%20%204%20-%3E%204%20%5Blabel%3D%22b%22%5D%3B%0A%20%20%20%204%20-%3E%205%20%5Blabel%3D%22b%22%5D%3B%0A%20%20%20%205%20%5Bperipheries%3D2%5D%3B%0A%20%20%7D'>