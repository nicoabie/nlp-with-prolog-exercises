# Practical session

## The Hogwarts problem

A first attempt to this problem may be the following FSA which has one initial node (1) and two final nodes (3) and (4).  

### FSA Graph

![Alt text](https://g.gravizo.com/source/custom_mark01?https%3A%2F%2Fgithub.com%2Fnicoabie%2Fnlp-with-prolog-exercises%2Fblob%2Fmaster%2Fchapter-01%2Fpractical-session.md)
<details> 
<summary></summary>
custom_mark01
  digraph G {
    rankdir=LR;
    1 [shape=circle];
    1 -> 2 [label="a|the"];
    2 -> 2 [label="brave|fast"];
    2 -> 3 [label="witch|wizard|broomstick|rat"];
    3 [peripheries=2];
    3 -> 1 [label="with"];
    1 -> 4 [label="harry|hermione|ron"];
    4 [peripheries=2];
  }
custom_mark01
</details>

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