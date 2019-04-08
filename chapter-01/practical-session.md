# Practical session

## The Hogwarts problem

A first attempt to this problem may be the following FSA which has one initial node (1) and two final nodes (3) and (4).  

### FSA Graph

<img src='https://g.gravizo.com/svg?
%20%20digraph%20G%20%7B%0A%20%20%20%20size%20%3D%2210%2C10%22%3B%0A%20%20%20%20rankdir%3DLR%3B%0A%20%20%20%201%20%5Bshape%3Dcircle%5D%3B%0A%20%20%20%201%20-%3E%202%20%5Blabel%3D%22a%7Cthe%22%5D%3B%0A%20%20%20%202%20-%3E%202%20%5Blabel%3D%22brave%7Cfast%22%5D%3B%0A%20%20%20%202%20-%3E%203%20%5Blabel%3D%22witch%7Cwizard%7Cbroomstick%7Crat%22%5D%3B%0A%20%20%20%203%20%5Bperipheries%3D2%5D%3B%0A%20%20%20%203%20-%3E%201%20%5Blabel%3D%22with%22%5D%3B%0A%20%20%20%201%20-%3E%204%20%5Blabel%3D%22harry%7Chermione%7Cron%22%5D%3B%0A%20%20%20%204%20%5Bperipheries%3D2%5D%3B%0A%20%20%7D
'>

### The translation to prolog is straightforward

```prolog
initial(1).

final(3).
final(4).

arc(1,2,a).
arc(1,2,the).
arc(2,2,brave).
arc(2,2,fast).
arc(2,3,witch).
arc(2,3,wizard).
arc(2,3,broomstick).
arc(2,3,rat).
arc(3,1,with).
arc(1,4,harry).
arc(1,4,ron).
arc(1,4,hermione).
```