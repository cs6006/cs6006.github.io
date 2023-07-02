+++
title = "ELI5 (because I am, in fact, five)"
date = 2023-06-30
description = "How I taught Ms Zdan's first-graders to empathize with a machine, and you can too!"
slug = "eli5-i"
[extra]
prettydate = "June 30, 2023"
+++

Little kids use computers all the time.
Increasingly early in their schooling, they also learn how to code.
However, is writing code on a computer the best way to teach computing, or more generally, [computational thinking](https://www.cs.cmu.edu/~15110-s13/Wing06-ct.pdf)? I think not.

A first attempt at writing code is often frustrating because the computer feels like an obtuse, unreasonable thing that just... does things a certain way.
Because it wants to; because it can.
Memorize it and deal with it.
At worst, the computer becomes the adversary.
At best, it becomes an eccentric and unreliable teammate whom we have somehow learned to collaborate with.

I think kids need to understand, even _empathize with_, a computer before they begin to code.
Why does a computer do things the way it does?
What compels it, and what limits it?
In a series of four lessons, I took this step with twenty first-graders at [Beverly J Martin Elementary](https://www.ithacacityschools.org/bjm) in Ithaca, NY.



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
| :----: | :---: |
| `R` | burger |
| `B` | spaghetti |

</center>

I sneaked up to one city and whispered, "Can you order me a burger,
please?", and the students delivered. I ran to the other city and got
them to order me some spaghetti. Then I went to the
first city and requested that they order me a hot dog.

Pandemonium. I was accused of being a naughty man.

A student proposed that flashing *no card* could mean a hot dog, but I steered
them away from that: "Well some days you may want to order nothing at
all; reserve no card for that."

Someone proposed balancing the card between red and blue, or swapping
quickly between red and blue; I steered them clear of these too. After a
minute I offered each city a second card, and they had an answer right
away. The old rules would remain, and *any* two cards would mean hot
dog.

<center>

| Signal | Order |
| :----: | :---: |
| `R` | burger |
| `B` | spaghetti |
| `RR`, `BB`, `RB`, `BR` | hot dog |

</center>

This made me a little nervous since it was not part of the plan, but I
steered things along: "Well this is great, but what if the other city
confuses the hot dog order with _two_ burgers or _two_ things of spaghetti?
Or a burger that is chopped up and mixed into spaghetti?"

They figured out a way to make me happy:

<center>

| Signal | Order |
| :----: | :---: |
| `RR` | burger |
| `BB` | spaghetti |
| `RB`, `BR` | hot dog |

</center>

and, on prodding, they realized they could order yet another thing:

<center>

| Signal | Order |
| :----: | :---: |
| `RR` | burger |
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


### Lesson 2: computer as nation-state

I brought in a motherboard from the lab and showed it to the class.
There was a lot going on, of course, but I made the key point: a chip has a bunch of things that are connected by wire to other things.

<center>

<img src="https://newscenter.lbl.gov/wp-content/uploads/2021/12/microelectronic-raigvi-shutterstock_1568488030-1200x800-1.jpg"
alt= "A computer chip showing two square components in gray. The squares are connected by eight wires. Other wires are leaving the components and leading off to other parts of the circuit, out of frame." width="60%" title="Image from raigvi/Shutterstock">

</center>

As in the image above, I point out two large components that were connected directly using wires (in the image, look for the gray squares, and notice that they are connected directly by four pairs of wire).
These components were like our cities on hills, and the wires like our cards.
Power flowing through a wire? That's a blue card.
No power? That's a red card.
All their confusion from the previous week was also the computer's confusion,
and all their limitations also applied to the computer.

As an aside, the kids were especially excited to see that the motherboard had a little fan, and this led to a discussion about how running electricity through a computer chip causes it to heat up.
My students were young enough to have never actually handled incandescent lightbulbs, so that example fell flat on its face.
However, they had almost all used their parents' phones and tablets for hours in a row and knew that those got hot.
I explained that we _could_ use less power to keep the temperature down, but that would make it harder to tell whether a wire was sending power or not.
The kids made a neat connection to the cities-on-hills game: this was like ordering food on a really foggy day, when it was hard for the other city to see the color of the card.

### Lesson 3: how a computer stores a number

Ms Zdan reported that the students had taken to playing the card game in their free time.
By the time I arrived for the third lesson, they were absolute pros at zipline-based food-ordering.
They had figured out that they could use four cards to say sixteen things, and had begun to write down their "codes" on little cheatsheets.

This was easy money.
I made the point that all of this was only working because everyone had the same cheatsheets:
if I slipped a wonky cheatsheet into the mix, the whole system would break down.
We said, together, the the biggest word of the day: _protocol_.
They had arrived at a protocol for ordering food, just as computers have protocols for
their electrical signals.

We went back to two cards and four items, and I explained that the real challenge was not making a list, but making a list from which they could then _pick out_ a single item without confusing anyone else.
Indeed, they could make a list of _any_ four things and use two cards to pick out the right one.
For instance, they could use two cards to control their teacher around the room:

<center>

| Signal | Order |
| :----: | :---: |
| `RR` | Anshuman walks to the right |
| `BB` | Anshuman walks to the left |
| `RB` | Anshuman walks towards you |
| `BR` | Anshuman walks away from you |

</center>

and of course we spent a good five minutes having me bumble around the room like a robot.

I explained that a computer does the same thing, but with numbers.
We made a list of the kids' favorite numbers, and gave them card-based signals:


<center>

| Signal | Number |
| :----: | :----: |
| `RR` | a thousand! |
| `RB` | a thousand and one! |
| `BR` | a million! |
| `BB` | a quintajillion! |

</center>

Fun fact: little kids love big numbers.

We took a minute to write `0` on every card's red side and `1` on every card's blue side, and then I told them what a computer's favorite eight numbers are: `0`, `1`, `2`, `3`, `4`, `5`, `6`, and `7`.
Rather boring in comparison, yes, but could we signal them? Yes we could:

<center>

| Signal <br> (color) | Signal <br> (binary) | Number <br> (computer) |
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

We wrote this down on our little protocol cheatsheets and called it a day.

### Lesson 4: counting too far

TK.

Overflow.


### Acknowledgments

An enormous thank you to Ms Zdan, her teaching aide Ms Jenn, and
of course her delightful students.
My time at Beverly J Martin Elementary School was facilitated by Cornell
University's [<span style="font-variant: small-caps">grasshopr</span>](https://sites.google.com/view/grasshopratcornell/home) program, a volunteer organization
that pairs graduate students with K-12 teachers so we can share our
research with curious students. This is hard, important, rewarding work,
and you are superstars for making it happen every year.

