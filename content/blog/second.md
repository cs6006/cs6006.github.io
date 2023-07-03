+++
title = "Explain It Like I'm Five"
date = 2023-07-02
description = "How I taught Ms Zdan's first-graders to empathize with a machine, and you can too!"
slug = "eli5"
[extra]
prettydate = "July 2, 2023"
+++

Little kids use computers all the time.
Increasingly early in their schooling, they also learn how to code.
However, is writing code on a computer the best way to teach computing? I think not.

A first attempt at writing code is often frustrating because the computer feels like an obtuse, unreasonable entity that just does things a certain way.
Because it wants to; because it can.
Memorize it and deal with it.
At worst, the computer becomes the adversary.
At best, it becomes an eccentric and unreliable teammate with whom we have somehow learned to collaborate.

I think kids need to understand, even empathize with, a computer before they begin to code.
Why does a computer do things the way it does?
What compels it, and what limits it?
Some of these ideas are captured by the term [computational thinking](https://www.cs.cmu.edu/~15110-s13/Wing06-ct.pdf), due to Jeannette Wing.
In a series of four lessons, I taught twenty first-graders at [Beverly J Martin Elementary](https://www.ithacacityschools.org/bjm) to think computationally.



### Lesson 1: a tale of two hungry cities

I went into class with eight cards, each colored red on one
side and blue on the other. I split the class into two groups, standing
in huddles on opposite ends of the room. Each group got one card
and I explained the game:

> _You are two cities on hills, and you have a zip line that carries food
between you. Occasionally you'd like to order something to eat from the
other city, but the cities are rather far apart and you can only
communicate using your cards. A card is either red or blue, and you can
order either a burger or spaghetti._

I allowed them one meeting to come up with a plan, and they quickly had
something: red would mean a burger, and blue spaghetti.

<center>

| Signal | Order |
| :---- | ---: |
| `R` | burger |
| `B` | <span style="color:white">they</span>spaghetti |

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
| :---- | ---: |
| `R` | burger |
| `B` | <span style="color:white">they</span>spaghetti |
| `RR`, `BB`, `RB`, `BR` | hot dog |

</center>

This made me a little nervous since it was not part of the plan, but I
moved us along: "Well this is great, but what if the other city
confuses the hot dog order with _two_ burgers or _two_ things of spaghetti?
Or a burger that is chopped up and mixed into spaghetti?"

They figured out a way to make me happy:

<center>

| Signal | Order |
| :---- | ---: |
| `RR` | burger |
| `BB` | <span style="color:white">they</span>spaghetti |
| `RB`, `BR` | hot dog |

</center>

and, on prodding, they realized they could order yet another thing:

<center>

| Signal | Order |
| :---- | ---: |
| `RR` | burger |
| `BB` | <span style="color:white">they</span>spaghetti |
| `RB` | hot dog |
| `BR` | bibimbap |

</center>


Finally I handed them a third card, asked them to make the longest list
they could, and left the room. I returned to a menu of eight items and
some rather hungry kids.

We were out of time, but the students had enough fun that Ms Zdan
requested that I leave the cards for them to play with.
I left her with all eight cards, and a hint:
_n_ cards can say _2<sup>n</sup>_ things.


### Lesson 2: computer as nation-state

I brought in a motherboard from the lab and showed it to the class.
There was a lot going on, but I made the key point: a chip has a bunch of things that are connected by wire to other things.

<center>

<img src="https://newscenter.lbl.gov/wp-content/uploads/2021/12/microelectronic-raigvi-shutterstock_1568488030-1200x800-1.jpg"
alt= "A computer chip showing two square components in gray. The squares are connected by eight wires. Other wires are leaving the components and leading off to other parts of the circuit, out of frame." width="60%" title="Image from raigvi/Shutterstock">

</center>

As in the image above, I pointed out two large components that were connected directly using wire (in the image, look for the gray squares, and notice that they are connected directly by four pairs of wire).
These components were like our cities on hills, and the wires like our cards.
Power flowing through a wire? That's a blue card.
No power? That's a red card.
A computer chip has way more than two components, and those components need to talk each other all the time.
All of the confusion that my students faced with the card game was also the computer's confusion,
and all their limitations also applied to the computer.

The kids were especially excited to see that the motherboard had a little fan, and this led to a discussion about how running electricity through a computer chip causes it to heat up.
My students were young enough to have never actually handled incandescent lightbulbs, so that example fell flat on its face.
However, they had almost all used their parents' phones and tablets for hours in a row and knew that those got hot.
I explained that we _could_ use less power to keep the temperature down, but that would make it harder to tell whether a wire was sending power or not.
The kids made a neat connection to the cities-on-hills game: this was like ordering food on a really foggy day, when it was hard for the other city to see the color of the card.

An aside that I did not bring up with the kids:
in the card game, we reserved the _no card_ signal for _no order_.
This is not actually available to a computer, since even the silence of a wire has a semantic meaning.
To get around this, a computer uses a special signal to mean _no signal_.

### Lesson 3: how a computer stores a number

Ms Zdan reported that the students had taken to playing the card game in their free time.
By the time I arrived for the third lesson, they were absolute pros at ordering food by zip line.
They had figured out that they could use four cards to say sixteen things, and had begun to write down their "codes" on little cheatsheets.

I made the point that all of this was only working because everyone had the same cheatsheets:
if I slipped a wonky cheatsheet into the mix, the whole system would break down.
We said, together, the biggest word of the day: _protocol_.
They had arrived at a protocol for ordering food, just as computers have protocols for
their electrical signals.

We went back to two cards and four items, and I explained that the real challenge was not making a long list, but making a long list that was still short enough to later pick out a unique item.
Indeed, they could make a list of _any_ four things and use two cards to pick out the right one.
For instance, they could use two cards to control their teacher around the room:

<center>

| Signal | Order |
| :---- | ---: |
| `RR` | Anshuman walks to the right |
| `BB` | Anshuman walks to the left |
| `RB` | Anshuman walks towards you |
| `BR` | <span style="color:white">they</span>Anshuman walks away from you |

</center>

and of course we spent a good five minutes having me bumble around the room like a robot.

I explained that a computer does the same thing, but with numbers.
We made a list of the kids' favorite numbers, and gave them card-based signals:


<center>

| Signal | Number |
| :---- | ----: |
| `RR` | a thousand! |
| `RB` | <span style="color:white">they</span>a thousand and one! |
| `BR` | a million! |
| `BB` | a quintajillion! |

</center>

Fun fact: little kids love big numbers.

We took a minute to write `0` on every card's red side and `1` on every card's blue side, and then I told them what a computer's favorite eight numbers are: `0`, `1`, `2`, `3`, `4`, `5`, `6`, and `7`.
Rather boring in comparison, yes, but could we signal them? Yes we could:

<center>

| Signal <br> (color) | Signal <br> (binary) <span style="color:white">they</span>| Number <br> (computer) |
| :--- | :--- | --: |
| `RRR`<span style="color:white">theythey</span> | `000` | `0` |
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

We started the day with a little arithmetic. How do we add 6 and 3?
My students were early enough in their education that they did this exactly the way I wanted them to:

> _We put up six fingers and say out loud, "one, two, three". As we say each number, we put up an additional finger. Then we stop and think. How many fingers do we have up? Nine!_

I then asked them to add 6 and 5.
They started off strong, but then, at ten, ran out of fingers.
Some of them counted a toe, but most just contented themselves with calling me a naughty man again.
I explained that a computer sometimes has a similar problem: it wants to keep going but it runs out of ways of holding on to information, just like running out of fingers to count or cards to signal with.

I requested a volunteer, and they and I stood up front facing the class.
We were on a number line, both currently at 0.
They were a person, and I was a computer.

<center>

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :---: | :---: |
| them | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> |
| me | | | | | | | | | |

</center>

"One more!" I said, and we both hopped over to stand on 1.

<center>

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :---: | :---: |
| <span style="color:white">they</span> | them | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> |
| | me | | | | | | | | |

</center>

The class took over. One more! One more! We eventually landed at:

<center>

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :---: | :---: |
| <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> |  <span style="color:white">they</span> | them |<span style="color:white">they</span> | <span style="color:white">they</span> |
| | | | | | | | me | | |

</center>

One more! I ran to the other end of the number line and stood on 0, while my volunteer jumped to eight:

<center>

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :---: | :---: |
| <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> | <span style="color:white">they</span> |  <span style="color:white">they</span> | <span style="color:white">they</span> | them | <span style="color:white">they</span> |
| me | | | | | | | | | |

</center>

There was a little riot. Once we had settled down, I asked them to look at their cheat sheets from the previous time:

<center>

| Signal <br> (color) | Signal <br> (binary) <span style="color:white">they</span>| Number <br> (computer) |
| :--- | :--- | --: |
| `RRR`<span style="color:white">theythey</span> | `000` | `0` |
| `RRB` | `001` | `1` |
| `RBR` | `010` | `2` |
| `RBB` | `011` | `3` |
| `BRR` | `100` | `4` |
| `BRB` | `101` | `5` |
| `BBR` | `110` | `6` |
| `BBB` | `111` | `7` |

</center>

What was a poor computer to do? I had simply run out of unique signals after 7, and I wanted to do something reasonable, so I had wrapped around to 0.

I explained that a computer does the same thing, and that it is called _overflow_.
By and large, the largest number that a computer can express, plus one, is the smallest number it can express.

So what's the big deal?

Well, let's say we're in a car with our mom.
The speedometer says we're doing seven miles per hour, and, yup, we are.
Then mom hits the gas a hair and the speedometer says we're doing zero.
Actually, we're doing eight.
Hmm, there's a bunch of stuff that we're allowed to do at zero miles an hour:
we're allowed to unbuckle our seatbelts, open the door, step out for ice-cream.
Doing this at eight miles per hour is a bad idea, and we know it.

With this (and an impromptu group hug), we wrapped up.
I like to think that my students left with a little more empathy for the computer, and all the little hoops it needs to jump through while it does our bidding.


### Further reading for the precocious student (or teacher)

I designed the lesson plan above with some care, trying to tell no untruths and yet not to overwhelm.
No doubt there will be further questions.
I'll answer some of them here.

1. _I'm pretty sure my computer can count way past seven. What's up with that?_

    In the example, a computer has three digits and each digit can be either 0 or 1, and so it can say 2<sup>3</sup> = 8 things.
    A modern computer actually has 64 digits, and so it can say 2<sup>64</sup> things.
    That's 1.84 x 10<sup>19</sup>: more than there are grains of sand on Earth.

    The average computer does not actually allow you to count that high:
    it wants to save a good chunk of its signals for stuff besides numbers.
    For instance, it needs a unique signal for each mathematical symbol, each mark of punctuation, each letter of the Roman alphabet,
    each letter of _every other_ human script, for each emoji, and so on.
    Even after allowing only a limited number of signals for numbers, we can still count pretty far:
    the largest number my machine will (easily) let me count to is 4611686018427387903.

2. _What about negative numbers?_

    In the example I simplified to positive numbers, so I was able to use my three digits to count from 0 to 7.
    When we know we'll need negative numbers, the standard practice is to use the same signals to instead mean:

<center>

| Signal <br> (color) | Signal <br> (binary) <span style="color:white">they</span>| Number <br> (computer) |
| :--- | :--- | --: |
| `RRR`<span style="color:white">theythey</span> | `000` | `-4` |
| `RRB` | `001` | `-3` |
| `RBR` | `010` | `-2` |
| `RBB` | `011` | `-1` |
| `BRR` | `100` | `0` |
| `BRB` | `101` | `1` |
| `BBR` | `110` | `2` |
| `BBB` | `111` | `3` |

</center>


3. _Is this overflow business real? What do we do about it?_

    Oh it's real.
    Consider the following code.
    My questions start with `#` and end with `;;`.  The computer's answers start with `- : int =`.

      ```
      # max_int;;
      - : int = 4611686018427387903
      # 4611686018427387903 + 1;;
      - : int = -4611686018427387904
      # min_int;;
      - : int = -4611686018427387904
      ```
    First I asked my machine to please tell me the biggest number it can handle.
    Then I added one to it.
    The answer was a rather small number; note that we've gone deeply negative.
    In fact, it was the smallest number my machine can handle.

    We have clever ways of checking for overflow, but here's the thing:
    addition accompanied by a check for overflow is meaningfully more expensive than a plain addition.
    We want to run these special checks judiciously.
    As an analogy, consider a person who gives their car a 75-minute inspection every morning before driving ten minutes to work.
    They'll be safe, but they'll also be late.
    Checking the car before each big family road trip is probably enough.

    Yet another instance where the computer must tread a tightrope!

    Sometimes, after analyzing a piece of code carefully, we're pretty sure that overflow _cannot possibly_ occur in that code, so we allow ourselves to skip the expensive checks.
    However, this analysis is tricky and we had better make sure we get them right.
    In 2021 I helped show that Dijkstra's algorithm, a classic algorithm that has been taught and used for over 60 years, can overflow in a way that was not previously known.
    I'll let you read all about that [here](https://link.springer.com/chapter/10.1007/978-3-030-81688-9_37).



### Acknowledgments

An enormous thank you to Ms Zdan, her teaching aide Ms Jenn, and
of course her delightful students.
My time at Beverly J Martin Elementary School was facilitated by Cornell
University's [<span style="font-variant: small-caps">grasshopr</span>](https://sites.google.com/view/grasshopratcornell/home) program, a volunteer organization
that pairs graduate students with K-12 teachers so we can share our
research with curious students. This is hard, important, rewarding work,
and you are superstars for making it happen every year.
