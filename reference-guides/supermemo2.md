---
description: About our Spaced Repetition algorithm
---

# SuperMemo2

### What is SuperMemo2 \(SM2\)?

From [Wikipedia](https://en.wikipedia.org/wiki/SuperMemo):

> SuperMemo \(from "Super Memory"\) is a learning method and software package developed by SuperMemo World and SuperMemo R&D with Piotr Woźniak in Poland from 1985 to the present.
>
> It is based on research into long-term memory, and is a practical application of the spaced repetition learning method that has been proposed for efficient instruction by a number of psychologists as early as in the 1930s.

SM2 is the most popular version of SuperMemo, refers to the original computer-based algorithm released in the 1987.

### Memoet is a port of Anki SM2 algorithm

Anki’s algorithm differs from SM-2 in some respects. Notably:

* SM-2 defines an initial interval of 1 day then 6 days. With Anki, you have full control over the length of the initial learning steps. Anki understands that it can be necessary to see a new card a number of times before you’re able to memorize it, and those initial "failures" don’t mean you need to be punished by being shown the failed card many times over the course of a few days. Performance during the learning stage does not reflect performance in the retaining stage.
* Anki uses 4 choices for answering review cards, not 6. There is only one 'fail' choice, not 3. The reason for this is that failure comprises a small amount of total reviews, and thus adjusting a card’s ease can be sufficiently done by simply varying the positive answers.
* Answering cards later than scheduled will be factored into the next interval calculation, so you receive a boost to cards that you were late in answering but still remembered.
* Like SM-2, Anki’s failure button resets the card interval by default. But the user can choose to have the card’s interval reduced instead of being reset completely. Also, you can elect to review failed mature cards on a different day, instead of the same day.
* 'Remembered easily' not only increments the ease factor, but adds an extra bonus to the current interval calculation. Thus, answering 'remembered easily' is a little more aggressive than the standard SM-2 algorithm.
* Successive failures while cards are in learning do not result in further decreases to the card’s ease. A common complaint with the standard SM-2 algorithm is that repeated failings of a card cause the card to get stuck in "low interval hell". In Anki, the initial acquisition process does not influence a card’s ease.

### What happens if I press...

#### Again

The card is placed into relearning mode, the ease is decreased by 20 percentage points \(that is, 20 is subtracted from the 'ease' value, which is in units of percentage points\), and the current interval is multiplied by the value of 'new interval' \(this interval will be used when the card exits relearning mode\).

#### Hard

The card’s ease is decreased by 15 percentage points and the current interval is multiplied by 1.2.

#### Good

The current interval is multiplied by the current ease. The ease is unchanged.

#### Easy

The current interval is multiplied by the current ease times the 'easy bonus' and the ease is increased by 15 percentage points.

{% hint style="info" %}
Read more about SRS in Anki FAQ: [https://faqs.ankiweb.net/what-spaced-repetition-algorithm.html](https://faqs.ankiweb.net/what-spaced-repetition-algorithm.html)
{% endhint %}

