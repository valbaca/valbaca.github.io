---
layout: post
title:  "My Personal Journey through Programming Languages"
date: -0700 2022-07-20 09:56:39 -0700
categories: programming languages ruby java
---

I originally meant to talk about Kotlin and Rust, but then this turned into a personal history of languages I've used...so that's what this post is.

# Early Years

I love learning new programming languages. It's almost an obsession. I think it came from the fact that I learned so many clunky languages at the very beginning of my programming life. My very first programming book was ["C++ for dummies" (5th edition)](https://www.amazon.com/C-Dummies-Stephen-R-Davis/dp/0764568523). In 2006 (high school for me) C++ was synonymous with programming, at least in the sense of "how do I learn to program." Before that, I technically did a tiny bit of web-development in middle school, around 2002. It was just the absolute basics of creating a website. These skills would be really handy in the era of MySpace and being able to copy in CSS and JS and know what was actually going on!

Moving on...in college, I majored in electrical engineering and computers science. On the CS side, we mostly worked in C++ or Java or Scheme. On the EE side, it was mostly Matlab but also some C for microcontroller programming. I never really found a language I liked, but we also use a different language each semester so you didn't really get any expertise in any of it. It was also rough because to be honest, none of these languages were very "friendly" to new programmers and some of the professors were just downright hostile to change. I remember our computer architecture professor refused to touch any machine that wasn't running SunOS (in 2010!). But the languages we did use were geared toward the machine, not the programmer. 

For me, the big enlightening experience was around 2011, at the peak of the Ruby on Rails hype. My last semester of college was one where I finally had some free time after four and a half years of dual majoring. I mostly spent time with my girlfriend (now wife!) and played lots Call of Duty (I was great!) and Starcraft (I was terrible!). I also messed around with learning Linux deeply and the [Ruby](https://www.amazon.com/Ruby-Programming-Language-Everything-Need/dp/0596516177) programming language. It was *beautiful*. You can print with just one work `puts` or hell, even one character `p`. You could fit entire programs on a single screen. Your numbers are just numbers and the number type just automatically gets bigger when they need to. With Ruby on Rails, I built my own Rails website on Heroku. With a credit card mean for emergencies...I bought like four books on Ruby and RoR immediately. 

(A short aside on books vs online learning): This would also kick off my love of programming books, especially the O'Reilly programming books. I'm going to date myself, but I still love learning the fundamentals of a language from a book. I think a major reason was that screen sizes were quite limited back then. You only had a single monitor or laptop screen, so having a book laid open was like a second screen. The editing quality of books is also higher than most written documentation and there's no link rot. Books also tend to give more commentary on the *why* and best practices and is more conversational, whereas a website is just listing facts. All that said, it all depends on the language; some just don't have a good book (Crystal) and/or have superior resources online (Clojure, Go, Rust).

Granted, there was so much at that time I didn't remotely understand (ActiveRecords, metaprogramming), but it felt okay because it was because that was **Advanced Knowledge** and not just **complicated knowledge** (as opposed to needing to understand OOP for Java or Pointers and memory management for C & C++).

Of course, as the saying goes, beauty doesn't last. I'll never forget the moment of disillusionment as I worked through [Project Euler](TK) problems in Ruby. Sometimes, it would be execute in a second and solutions would consist of a single-line of code...and other times, it would take *hours* to finish executing, meanwhile my poor Thinkpad X200s turned into a hot plate. I felt firsthand what people meant when they said Ruby was slow and inefficient. Obviously my Project Euler solutions were just toy programs, poorly written by a novice and I was only a math major, but we would soon hear similar stories in the large, like with Twitter moving away from Ruby as well.

# Career Years

With that last semester of college over, it was finally time to get to work. I went to work at Raytheon because they were literally the ones hiring. [The Great Recession](https://en.wikipedia.org/wiki/Great_Recession) was officially over but it was still very rough to get a job straight out of college. Being a military contractor, they obviously weren't on the cutting edge of web tech, but there were people really trying to bring Raytheon into the 21st century with Agile and Ruby. All I worked with was Java 4, J2EE, and some old-school IE6-compatible JavaScript. I actually did quite a bit of JavaScript because the "real" programmers were not willing to learn a "new and terrible" language. I hadn't touched JS since building my Yahoo! GeoCities website in middle school, but saw that I could fulfill a role that the team needed. It was also the time that JS was getting more attention with Node. I still have my ebook ["What is Node?"](https://www.oreilly.com/library/view/what-is-node/9781449315016/) floating in my Kindle library from that time. Even at the time, it wasn't clear whether Node was to be taken seriously or if it's an elaborate practical joke on programmers. *Somehow we were wrong and right on both accounts.* 

*I actually cut quite a bit here...* suffice it to say that I was happy to leave Raytheon and work at the quickly growing more-than-just-a-bookstore Amazon.com in 2013. However, in terms of programming languages, not much changed. Java and JavaScript still made up 90% of the code I would write for the next decade.

That was until I worked on AmazonSmile for iOS where I worked with ~~Swift~~ Objective-C. Since we *had* to write in ObjC, I took up the role of becoming an ObjC master and teacher for the team. Despite the crazy syntax and obscure nature of the language, the team grew a soft spot for the language. Stepping away from the absurdly [complected](https://www.youtube.com/watch?v=SxdOUGdseq4) world of Java, with Spring's AbstractProxyFactories, Dependency Injection, and terrible build times (made 10-100x worse due to internal tools). ObjC built fast in Xcode wayyy faster Android Studio and the debugger actually worked, every single time. You could do neat stuff with "reflection" with hardly any runtime hit. Obj-C's directness, speed, and reliability made Android's Java look like a joke...but square brackets are too weird I guess.

That said, I completely understand why these companies choose Java. It was built scratch to be for enterprise use, not just because of things like Spring and Hibernate, but by the very nature of the language. Everything *must* be in a class and nearly every class corresponds 1:1 with a file. So everyone's work is separated, reducing the # of files anyone works on at a time. This is all following the Single-Responsibility principle. But at the same time it reduces the ability to make changes that have cross-cutting concerns (like security and logging). So then we tack on things like AspectJ and Interceptors. 

This may be my tin-foil hat, but I legitimately believe that part of the success of Java is the nature of the cult around "Best Practices" (of which I've been a part of!). Java was designed to be easy and familiar for C++ programmers to pick up and C++ itself was similarly designed to be easy and familiar for C programmers to pick up. So there are design decisions that trace all the way back to C and also new ones thrown in as well. While C & C++ have foot-guns, Java has foot-tazers? You can find them in [Java Puzzlers](http://www.javapuzzlers.com/) . So before you can be effective Java developer, you have to first learn the basics of programming (variables, loops) and OOP (classes, methods, inheritance). Then, just when you think you're ready, you also need to read [Effective Java](TK). At each step of the way, there's some more senior developer eager to slap you on the wrist in your code review and remind you to use `final` everywhere. But the whole thing is that these things don't make you a better developer, they just make you a better Java developer. What's the difference? Certainly a whole 'nother post.

There are complexities inherent to some domains and many problems in software engineering that are Just Very Hard, period; like CAP theorem and distributed computing. Then there are things in *coding* that are also Just Hard; like naming and commenting appropriately. Finally, there are things **made hard** in programming by the language. Again, [Rich Hickey put it best](https://www.youtube.com/watch?v=2V1FtfBDsLU&t=1640s&ab_channel=ClojureTV). **Please, if you take nothing else from this post, check out that video clip.**

At this point in my career, I think I'm approaching a new level-up moment. I've dabbled in a lot of languages at work and many more at home. A glance at my bookshelves and bookmarks shows: C, C++, Objective-C, Rust, Go, Java, Perl, JavaScript, TypeScript, Python, Ruby, Scala, Kotlin, and Clojure. My brain is saturated with syntax and idioms and paradigms. At this point I'm mostly frustrated with languages with too many gotchas. But I suppose any language that actually sticks is one that sticks around long enough for those "gotchas" to actually be found.

I'm also frustrated by modern execution times. Java's cold starts on AWS Lambda have been the bane of my existence for the past several years. The GraalVM is supposed to help in this regard, but with serverless, we really have to rethink our execution model. The idea that "it doesn't matter how long it takes to serve the first request as long as the rest are fast" is old-fashioned; oh, and the "fast" second requests still aren't even that fast. Why does every request to a Java server come with a 100ms minimum latency? It's all just a tradeoff that we accepted to not have to deal with memory and pointers. And to be fair, Java held the crown for fastest enterprise language for a long time. Only recently did Go begin to usurp the  king. And again, to be fair to Java, it practically allowed Amazon and other companies to be able to build out what they needed by  tossing more developers at the problems. A mediocre junior Java developer can actually get a decent amount done. So I see why it's still on top. I mean, look at me!

# Present Day

I'll make this section its own post, but there are a handful of languages I'd love to work with at some point:

1. Rust - A stringent, but caring compiler. A **fantastic** toolset. Blazing fast!! Monadic returns
2. Crystal - A nascent language, but as beautiful as Ruby...and fast!
3. Clojure - A Lisp that targets JVM & JS. It could be my "uber-language"

I look forward to writing about each of them.

In the meantime, my world is still very much mostly Java and JavaScript. Both are getting rock-solid upgrades with Kotlin and TypeScript respectively. I don't mind any of them nearly that much anymore.

![[bookshelf.jpeg]]

## So what's the point?

So what's the point of learning so many programming languages if you only use really two languages? Because each language teaches a lesson, gives a different viewpoint via its paradigm, and shows what is **possible** in computing, but may just be tough in your language.

So to wrap this up, I've compiled a list of things I've learned, loved, and hated about different languages I've worked or played with, approximately in order of low-level to high-level programming languages.

- C
	- Context: I mostly wrote C in college for EE projects. Currently a "read-only" language for me.
	- C shows how much you can do with *so* little. It was necessary to program microcontrollers, learn how system calls work in my Computer Architecture class, and it's valuable to develop an "intuition" of what's going on in those core tools like compilers and drivers.
	- Cons: C has no shortage of cons...so let's just say lack of namespaces and wild function pointer syntax. 
- C++
	- Context: I wrote some C++ in college and my college internship. None since.
	- I wouldn't recommend it, but C++ being my first language helped me move "upward" to Java and "downward" to C with relative ease.
	- Cons: C++ virtual methods, deconstructors, and multiple inheritance
- Objective-C
	- Context: wrote some for a major project working with a large iOS app
	- ObjC's *blazing* speed, message passing style of methods, and featherlight reflection
	- Cons: a syntax only a mother could love...and if you ever work with Objective-C++ you have my deepest sympathies
- Rust
	- Context: novice, just worked through "the Rust book" a few weeks ago.
	- I'm very much a beginner with Rust. "Programming Rust" is the only book on my shelf I haven't read yet. So far though I can see the compiler really is there working with you, not against you. And I love `Result<T, E>` style returns with the `?` shorthand for easy error-handling.
	- Cons: not yet sure if Rust is a good fit for "after-hours" programming.
- Go
	- Context: novice, worked through practices online and some Advent of Code
	- Simple, like, stupidly simple and straightforward. The **first** chapter of [The Go Programming Language](https://www.gopl.io/) has you generating gifs, concurrently pulling from the web, and running a web server. Goroutines are powerful (see [Java's Loom Project](https://www.infoworld.com/article/3652596/project-loom-understand-the-new-java-concurrency-model.html)). 
	- Cons: unbearably tedious and fights abstraction at the language level. I stopped doing Advent of Code in Go because it was just *so* much typing. My hands were the bottleneck for the first time. Just no support for overloading or map/reduce/filter. The use of capitalization for public/private visibility is a pet peeve.
- Java
	- Context: primary programming language for 11+ years
	- Listen, Java's basically cut me a nice paycheck for the past decade, so let's just say "it pays the bills." For most projects, Java is good enough and mature enough to bank on. It's low/no risk. There are *so many* libraries out there for anything you want to do. The language doesn't update at breakneck speed, but it's kind of nice because you can rest assured features are fully tested and vetted. I do really like everything included in `java.util` and Java's interfaces like `Iterator/Iterable/Runnable`  adapted very well to single-method-lambda functions
	- Cons: Java Server startup and Thread model. "Java is slow" was the old joke in Java 1.1 but now it's surfaced in a new way: Java isn't good for AWS Lambda style on-demand execution (unless you go with GraalVM AOT compilation) and Java's Thread-per-request model on services also isn't keeping up with modern scaling requirements. To be fair, the first has a workaround (via AOT native compilation with GraalVM) and the latter is either addressed by using Reactive libraries or by holding out for Project Loom to launch. Java has shown it can respond to problems, but it's also shown to struggle with keeping up with "leaner" languages. Java's cold-start and large memory footprint matter more when we're no longer just running dedicated Ec2 hosts whose sole purpose is to host a web service. Note: my frustrations with Java have been a major source of looking at other languages, especially Rust.
	- Cons pt2: Not to mention the over-engineered and the [overly-enterprisified](https://projects.haykranen.nl/java/) nature of everything in Java. Every class needs getters and setters (because a "struct" is too brittle) and needs to be called via Proxy (because I gotta have enough Design Patterns in my code to get promoted to SDE 2). Oh god and annotations. Between Spring, Lombok, and friends I see that you either build a macro system (Ruby, Rust, or Clojure) or you'll have N written for you.
- Kotlin
	- Context: used some in Android years back and began using server-side professionally this year
	- Kotlin makes writing on the JVM a joy again. I especially like Kotlin's method extensions and type aliases. Obviously, I love the `val` keyword.
	- Cons: Kotlin's handling of static fields via companion objects seems like it could've been much simpler IMO. Overall, Kotlin still suffers from the JVM startup and memory issues.
- JavaScript
	- Context: secondary language for 11+ years
	- JS's resilience is impressive. It's grown a lot in the past decade. I like its object syntax and prototype-based inheritance. Prototypes just make sense to me.
	-  *remainder omitted for brevity*
- TypeScript
	- Context: began using a few year ago, primarily for CDK and React.
	- TypeScript is a solid A in my book. I'm glad that a JavaScript-replacer finally became mainstream and got the popularity and support it needed to bring some sanity to the world of JS/Node/etc
	- Cons: There *a lot* to the type system. This is a very weak con because it's just in comparison of how JS fits on an index card and I've just not had extensive experience with TS to fully work with all of its features
- Perl
	- Context: tertiary language, worked with legacy code for past 9+ years
	- aaahahhahaha...I guess some credit is due to one of the first mainstream dynamic scripting languages. Without it, people wouldn't have been incentivized to write Python or Ruby.
	- Cons: bwahahahahaha...but in seriousness I'll never touch perl again
- Python
	- Context: adept, used at work for glue scripts and jobs
	- I don't need to say anything here, we all know why Python is great
	- Cons: environment and packaging is a [nightmare](https://xkcd.com/1987/) and every python has a different value for X when they say "Well, **JUST** use X". Examples of X include:venv, virutalenv, poetry, pipenv, pyflow, and conda. This makes me appreciate good tooling even more. Hell, even `npm` is better than all of this nonsense. Also, I cannot stand the `__dunder__` methods.
- Ruby
	- Context: learned in college and used in some scripts
	- I've already waxed poetic, but I thank Ruby for first teaching me `fold/map/reduce` and what metaprogramming looks like.
	- Cons: too much emphasis on "elegance" and mixins. First, I love mixins, but every codebase I've worked with in Ruby abuses them when simple composition would've worked
- Clojure
	- Context: novice, learned on my own and used in some Advent of Code
	- Fantastic literals, decomposition, real immutability, real functional programming, and **honest-to-god Lisp macros**, using vectors instead of lists, using collections as functions. REPL reloading is fantastic.
	- Cons: Literally the worst stacktraces ever. REPL tooling and connectivity is flaky, same old slow JVM issues but 10x slower because of Clojure's highly dynamic nature, namespaces and imports are confusing and have bad tooling. No job demand. Not going to lie, learning Clojure was mind-bending (even mind-breaking). A large part of it was due to the many layers going on but also no debugging made things rough. Yes, you have the REPL, but you're needing to master the REPL at the same time you're trying to learn this whole other paradigm. The first few times I also made the mistake of also trying to use Emacs...way too much all at once. Learning Clojure is hard...but I'd still say it's worth it.

Thank you so much for reading. If you have thoughts, questions, or articulated feelings, please tweet at [@val_baca](https://twitter.com/val_baca).  