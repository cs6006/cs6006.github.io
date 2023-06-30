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
_n_ cards can say _2<sup>n</sup>_ things.


### Lesson 2: how a computer stores a number

When I went in the next week, the students were zipline-based food-ordering pros.
They had figured out that they could use four cards to say sixteen things, and had begun to write down their "codes" on little cheatsheets.

This was easy money.
I made the point that all of this was only working because everyone had the same cheatsheets:
if I slipped a wonky cheatsheet into the mix, the whole system would break down.
We said, together, the the biggest word of the day: _protocol_.

Next, painful as it was, we had to abandon our food metaphor.
We went back to two cards and four items, and I explained that the real trick was _picking out_ the right item from the list.
Indeed, they could make a list of _any_ four things and use two cards to pick out the right one.
For instance, they could use two cards to control their teacher around the room:

<center>

| Signal | Order |
| :--: | :--: |
| `RR` | Anshuman walks to the right |
| `BB` | Anshuman walks to the left |
| `RB` | Anshuman walks towards you |
| `BR` | Anshuman walks away from you |

</center>

and of course we spent a good five minutes having me walk around the room like a robot.

I explained that a computer does the same thing, but with numbers.
We took a minute to write `0` on every card's red side and `1` on every card's blue side, and then we put on the whiteboard the numbers that we could make with two cards:

<center>

| Signal <br> (cards) | Signal <br> (binary) | Number <br> (decimal) |
| :---: | :---: | :--: |
| `RR` | `00` | `1` |
| `RB` | `01` | `2` |
| `BR` | `10` | `3` |
| `BB` | `11` | `4` |

</center>

What, then, could we do with three cards?
We took it in two steps.
1. We could use two cards, as above, to get `1`, `2`, `3`, or `4`, and then use the third card to say
"red `1`" or "blue `1`", "red `2`" or "blue `2`", and so on.
2. We decided to start calling "red `1`" by the name `1`, "blue `1`" by the name `5`, and so on:

<center>

| Signal <br> (cards) | Signal <br> (binary) | Color-Number <br> (??) | Number <br> (decimal) |
| :---: | :---: | :--: | :--: |
| `RRR` | `000` | red `1` | `1` |
| `RRB` | `001` | red `2` | `2` |
| `RBR` | `010` | red `3` | `3` |
| `RBB` | `011` | red `4` | `4` |
| `BRR` | `100` | blue `1` | `5` |
| `BRB` | `101` | blue `2` | `6` |
| `BBR` | `110` | blue `3` | `7` |
| `BBB` | `111` | blue `4` | `8` |

</center>

Interestingly, the biggest challenge was the last one.
In order to set myself up for the next lesson, I really needed for them to get to:

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

That is, I wanted them to shift the numbers down by one: having `0` is way more useful than having `8`.
I must admit that this was a bit of a stretch, and basically ended with me pleading with them to just try it out.
Ms Zdan assured me that they would get it in the next lesson, and on that note we wrapped up.


### Acknowledgments

An enormous thank you to Ms Zdan, her teaching aide Ms Jenn, and
of course her delightful students.
My time at Beverly J Martin Elementary School was facilitated by Cornell
University's [<span style="font-variant: small-caps">grasshopr</span>](https://sites.google.com/view/grasshopratcornell/home) program, a volunteer organization
that pairs graduate students with K-12 teachers so we can share our
research with curious students. This is hard, important, rewarding work,
and you are superstars for making it happen every year.

