+++
title = "ELI5: Binary"
date = 2023-01-02
description = "How I taught Ms Zdan's first-graders binary, and you can too!"
slug = "eli5-ii"
draft = true
+++

# Lesson 3: A look at a circuit, and the end of Moore's law {#lesson-3-a-look-at-a-circuit-and-the-end-of-moores-law .unnumbered}

This was a digression. I brought in an FPGA and showed them the wires
running between components. I drew the analogy to the game. The students
were super interested in the fan, however, and we entered into an
unplanned discussion about Moore's law.

Fuller description TK.

# Lesson 4: Why $8$ looks like $0$ {#lesson-4-why-8-looks-like-0 .unnumbered}

TK, but here's a sketch.

I asked for a volunteer and we stood together in front of the class. We
were at $0$ on a number line, and moving to our right meant adding $1$.
She was a human, and I a computer. We counted from $0$ through $7$ no
problem, but on adding $1$ to $7$ she took a step to her right and I ran
all the way back to $0$.

I mapped this back to regular math, where performing $9 + 1 = 10$
requires an additional digit. What do you do when you are not allowed
that additional digit? There isn't a clean answer, but you're going to
have to do *something*. We went over the table that we had already drawn
up and explored some of the binary addition that was implicit.

-   Adding one to $1_{dec}$ is the same as adding one to $001_{bin}$.
    How do we do it? We carry the $1$, just like we do in regular math,
    and arrive at $010_{bin} = 2_{dec}$.

-   Adding one to $3_{dec}$ is the same as adding one to $011_{bin}$.
    It's a little more complicated than last time---a little like
    $99+1 = 100$ in regular math---but we figure it out and arrive at
    $100_{bin} = 4_{dec}$.

-   Adding one to $7_{dec}$ is the same as adding one to $111_{bin}$,
    and *we* know how to do that and arrive at $1000_{bin} = 8_{dec}$.
    However, a computer that has just three cards is in trouble: it does
    the math, gets to an answer, and then realizes that it doesn't have
    enough cards to write down the answer. It drops the leftmost digit.
    We know that
    $$7_{dec} + 1_{dec} = 111_{bin} + 1_{bin} = 1000_{bin} = 8_{dec},$$
    but a computer performs
    $$7_{dec} + 1_{dec} = 111_{bin} + 1_{bin} = {\color{red}1}000_{bin} = 0_{dec}.$$
    Uh oh.

I mapped this back to overflow, and why it is such a big issue. If
you're in your car with your mom and you *think* you're doing $0$ miles
per hour, but you're actually doing $8$, you may be in trouble. Eight
miles an hour is not very fast, but there's a whole bunch of stuff that
we're allowed to do at $0$ miles an hour that we're not allowed to do at
$8$ miles an hour. At $0$ miles an hour, you can unfasened your
seatbelt, lean over the seat, and even get out of the car and walk
around.

This is what happened with the Ariane 5 rocket. It was in fact flying
super fast away from the earth, but the on-board computer thought it was
going backwards towards the earth. The computer triggered a
self-destruct sequence because it thought it was going to crash into the
earth.

# Reflections {#reflections .unnumbered}

TK