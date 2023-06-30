+++
title = "ELI5: Binary"
date = 2023-01-02
description = "How I taught Ms Zdan's first-graders binary, and you can too!"
slug = "eli5-i"
+++

Little kids use computers all the time.
Increasingly early in their schooling, they also learn how to code.
Is writing code on a computer the best way to teach computing, or more generally, [computational thinking](https://www.cs.cmu.edu/~15110-s13/Wing06-ct.pdf)? I think not.

A first attempt at writing code is often frustrating because the computer feels like a totally obtuse, totally unreasonable thing that just... does things a certain way.
Because it wants to; because it can.
Memorize it and deal with it.
At worst, the computer becomes the adversary.
At best, it becomes an eccentric and unreliable teammate whom we have somehow learned to collaborate with.

I think kids need to understand, even _empathize with_, a computer before they begin to code.
In a series of lessons, I took this step with twenty first-graders at [Beverly J Martin Elementary](https://www.ithacacityschools.org/bjm).



### Lesson 1: a tale of two hungry cities

I went into class with eight pieces of card, each colored red on one
side and blue on the other. I split the class into two groups, standing
in huddles on opposite ends of the room. I handed each group one card
and explained the game:

> _You are two cities on hills, and you have a zipline that carries food
between you. Occasionally you'd like to order something to eat from the
other city, but the cities are rather far apart and you can only
communicate using your cards. A card is either red or blue, and you can
order either a burger or spaghetti._

I allowed them one meeting to come up with a plan, and they quickly had
something: red would mean a burger, and blue spaghetti.

<center>

| Signal | Order |
| :--: | :--: |
| `R` | burger |
| `B` | spaghetti |

</center>

I sneaked up to one city and whispered, "Can you order me a burger,
please?", and the students delivered. I ran to the other city and got
them to order me another burger and some spaghetti. Then I went to the
first city and requested that they order me a hot dog.

Pandemonium. I was accused of being a naughty man.

A student proposed that flashing *no card* could mean a hot dog, but I steered
them away from that: "Well some days you may want to order nothing at
all; reserve no card for that."

Another proposed balancing the card between red and blue, or swapping
quickly between red and blue; I steered them clear of these too. After a
minute I offered each city a second card, and they had an answer right
away. The old rules would remain, and *any* two cards would mean hot
dog.

<center>

| Signal | Order |
| :--: | :--: |
| `R` |     burger |
| `B` | spaghetti |
| `RR`, `BB`, `RB`, `BR` | hot dog |

</center>

This made me a little nervous, since it was not part of the plan, but I
steered things along: "Well this is great, but what if the other city
confuses the hot dog order with just a double order, or a burger that is
chopped up and mixed into spaghetti?"

They figured out the way to make me happy:

<center>

| Signal | Order |
| :--: | :--: |
| `RR` |     burger |
| `BB` | spaghetti |
| `RB`, `BR` | hot dog |

</center>

and on prodding, they realized they could order yet another thing:

<center>

| Signal | Order |
| :--: | :--: |
| `RR` |     burger |
| `BB` | spaghetti |
| `RB` | hot dog |
| `BR` | bibimbap |

</center>


Finally I handed them a third card, asked them to make the longest list
they could, and left the room. I returned to a menu of eight items and
some rather hungry kids.

We were out of time, but the students had enough fun that Ms Zdan
requested that I leave the cards for them to play with until next week's
lesson. I left her with all eight cards, and a hint:
_n_ cards can
say _2<sup>n</sup>_ things.


### Lesson 2: how a computer stores a number

TK, but here's the punchline:

<center>

| Signal <br> (cards) | Signal <br> (binary) | Number <br> (decimal) |
| :---: | :---: | :--: |
| `RRR` | `000` | `0` |
| `RRB` | `001` | `1` |
| `RBR` | `010` | `2` |
| `RBB` | `011` | `3` |
| `BRR` | `100` | `4` |
| `BRB` | `101` | `5` |
| `BBR` | `110` | `6` |
| `BBB` | `111` | `7` |

</center>


### Acknowledgments

My time at Beverly J Martin Elementary School was facilitated by Cornell
University's [<span style="font-variant: small-caps">grasshopr</span>](https://sites.google.com/view/grasshopratcornell/home) program, a volunteer organization
that pairs graduate students with K-12 teachers so we can share our
research with curious students. This is hard, important, rewarding work,
and you are superstars for making it happen every year.

An enormous thank you to Ms Zdan, her teaching aide Ms Jenn, and
of course her delightful students.