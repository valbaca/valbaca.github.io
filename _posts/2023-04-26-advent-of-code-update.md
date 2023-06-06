---
layout: post
title:  "Advent of Code Update"
date: 2023-04-26 19:04:52
category: advent
tags: advent kotlin python rust
---

## Advent of Code Update

First, consider reading my original post on Advent of Code [here](https://valbaca.com/advent/2022/09/05/advent-of-code-progress.html)

Assuming you've read that, here's my update:

**I finished year 2022 in *surprise!* Kotlin!** You can find the code here: [github.com/valbaca/advent-kt](https://github.com/valbaca/advent-kt)

Even though I didn't even mention Kotlin in my last post, it's the primary backend language that I use now for work. I ended up not staying at the startup that used Python, but I'm still a fan of Python. **In fact, I even went back and finished 2021 in Python.**

## Updated language thoughts

Kotlin

- Probably the best (most pragmatic) language I've used for Advent of Code.
- It's at least a Better Java, likely the best language on the JVM, and a strong contender for best static language.  Can use any Java libraries practically natively. I like [Guava](https://github.com/google/guava) and [Eclipse Collections](https://www.eclipse.org/collections/)
- Builds and runs very fast.
- Fantastic IDE support through IntelliJ. Great debugging, profiling, and gives suggestions
  - For example, if you do a `map` followed by `sum` it will suggest just doing `sumOf`. So much better than memorizing all of Clojure's sequence functions.
- Powerful/expressive features like:  [DeepRecursiveFunction](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-deep-recursive-function/), [extensions](https://kotlinlang.org/docs/extensions.html), [`when` expressions](https://kotlinlang.org/docs/control-flow.html#when-expression), and [data classes](https://kotlinlang.org/docs/data-classes.html)
- Cons/Missing: Python's tuples and dynamically growing `int`, Clojure's `assoc-in` and friends, and Rust's `match`

Python

- Same points as before: especially well-suited for Advent of Code
- Occasionally run into dynamic-language specific issues like this:
  - `return a, b if condition else None` I expected `(a,b) | None`, but got `(a, b|None)`

It's the classic Static vs Dynamic languages: dynamic languages require less up-front time but cost more in runtime and tracking down type issues at runtime; whereas, static languages have the opposite trade-off.

Now, there's a language that's further on the up-front spectrum: Rust.

Rust

- Blazing speed: it's just impressive seeing any code running in microseconds
- Powerful features: top-tier enums, match, map/reduce/etc
- Cons: Directly dealing with pointers Box/Arc/etc. Incredibly verbose.

I am more familiar with Rust now after reading and working through [The Book](https://doc.rust-lang.org/book/), [Rust by Example](https://doc.rust-lang.org/rust-by-example/), and [Rustlings](https://github.com/rust-lang/rustlings).

## Progress by Year and language (as of Apr 2023)

- Year 2015: 🎄 DONE! multiple times!
  - Fully solved in Python [valbaca/advent-py](https://github.com/valbaca/advent-py)
  - Fully solved in Go [valbaca/advent-go](https://github.com/valbaca/advent-go)
  - Fully solved in Clojure [valbaca/advent](https://github.com/valbaca/advent)
- Year 2016: ❄️ ON ICE @ Day 20
  - Days 1-7 & 19 in Python
  - 1-11 in Clojure and 11-18 in Java.
  - 1-12 in Go
- Year 2017: ❄️ ON ICE @ Day 7
  - Days 1-5 in [Crystal](https://crystal-lang.org/)
- Year 2018: ❄️ ON ICE @ Day 6
- Year 2019: ❄️ ON ICE @ Day 2
- Year 2020: 🎄 DONE!
  - Fully solved in Python [valbaca/advent-py](https://github.com/valbaca/advent-py)
- Year 2021: 🎄 DONE!
  - Fully solved in Python [valbaca/advent-py](https://github.com/valbaca/advent-py)
- Year 2022: 🎄 DONE!
  - Fully solved in Kotlin [valbaca/advent-kt](https://github.com/valbaca/advent-kt)
