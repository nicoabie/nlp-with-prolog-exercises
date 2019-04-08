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

<img src='https://g.gravizo.com/svg?
  digraph G {
    rankdir=LR;
    1 [shape=circle];
    1 -> 2 [label="a|the"];
    2 -> 2 [label="brave|fast"];
    2 -> 3 [label="witch|wizard|broomstick|rat"];
    3 [peripheries=2];
    3 -> 1 [label="with"];
    1 -> 3 [label="harry|hermione|ron"];
  }
'>

Test1 is able to parse now [ron, with, harry] however test3 only sees that 1 is an initial node and 3 is a final node and it stops there, unable to go back to the node 1 as test1 does.

## Ex 3.

<img src='https://g.gravizo.com/svg?
  digraph G {
    rankdir=LR;
    1 [shape=circle];
    1 -> 2 [label="aaaa"];
    2 -> 2 [label="a"];
    2 -> 3 [label="bbb"];
    3 -> 3 [label="b"];
    3 -> 4 [label="b"];
    4 [peripheries=2];
  }
'>

<img src='https://g.gravizo.com/svg?
  digraph G {
    rankdir=LR;
    1 [shape=circle];
    1 -> 2 [label="aa"];
    2 -> 2 [label="a"];
    2 -> 3 [label="cc"];
    3 -> 4 [label="bb"];
    4 -> 4 [label="b"];
    4 -> 5 [label="b"];
    5 [peripheries=2];
  }
'>