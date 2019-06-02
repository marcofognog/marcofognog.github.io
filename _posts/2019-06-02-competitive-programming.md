---
layout: post
title: This is not Ruby.
date: 2019-06-02
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Ruby
tags: []
author:
  login: marcofognog
  email: marcofognog@gmail.com
  display_name: marcofognog
---

A friend and I solved a challange from [code wars](https://www.codewars.com/) in Ruby. The program worked, but something bothered me.

We understood the problem, than thought about the steps the algorithm would take.

We thought **really hard** about it.

We wrote the code.

It failed here and there because of silly mistakes, and eventually worked. (the tests passed)

It ended up something like 15 or 20 lines of code that was hard to read and had some duplications.

Anyway, later he showed me this solution from another user for the same problem:

```ruby
def mix(s1, s2)
 hist=('a'..'z').map{|c| [c, s1.count(c), s2.count(c)]}.select{|v| v[1]>1||v[2]>1}
 hist2=hist.map{|v| [v[1]>v[2]?-v[1]:-v[2], v[1]>v[2]?'1':v[1]<v[2]?'2':'=', v[0]]}
 hist2.sort.map{|v| v[1]+':'+v[2]*-v[0]}.join('/')
end
```


At that point I knew what was going on: this is not Ruby.

**"Of course it is, it has even the sweet syntax sugar for range of strings!"**

Simply put, you could write very similar code in most of the other languages (Phyton, Javascript, or even C) with no difference about the way you think about the problem.

To better understand this, let's digress just a bit (I promise), and think about what is a *programming language*.

**Language and approach**

In the course [programming languages](), in coursera, the professor suggests a langague is:

**1.** syntax, **2.** evaluation rules, and **3.** type checking rules

Great, we could be really objective in defining languages using those three aspects, right?

Well, there's actually more to it. Each language builds their set of behaviours (syntax, the eval rules and the type checking) around some core ideas, or approach.
You could even call it **ideology**.

We can say Ruby, for example, was built for [programmer happines](https://learn.co/lessons/matz-readme).
Java, on the other hand, implements very stiff object orientation (IMO), because their creators had other things in mind ([such as the write once run anywhere](https://en.wikipedia.org/wiki/Write_once,_run_anywhere)).
Yes, Ruby also claims to be very object oriented, but one can see it achieves that in a differente way than Java.
My point here is, all the design decisions in the language favor or hinders **ways of thinking**.

Because of the differences in the **world view**, a language could also be described by the high level practices and approaches it takes to solve problems.

The idioms can highlight this phenomena very well. For example, you could loop using `for` in Ruby, but using enumerables (like the method `#each`) feels much better.

Deriving from the language design choices, we get to the libraries and the ecosystem itself.
Which in turn may include the discussions about *presenters*, *Domain Driven Design*, TDD, SOLID, DRY, etc...
There's a whole community around the language that have a 'style' of thinking and approaching problems.
Rails has even a [doctrine manifest](https://rubyonrails.org/doctrine/), to name only one example.

**Back to the task at hand**

One could argue that, in that particular case, none of that matters because the problem is a very short and simple challange.

And that's the whole point.

We just wrote a program that:

* will never change
* will never go to production
* will never get exposed to different kinds of failures
* nobody else will have to read it in a year...

Tackling those issues is what got Ruby so popular in the first place in the software industry.

Now, let's check what we didn't do:

- design testable interfaces
- abstraction / concepts (favored by the previous point)
- baby steps, in a progressive, ratcheting manner
- version control
- refactoring

Those are the things (with the exception of version control) in which Ruby could excel.

**It's all about the points**

When we thought about refactoring, we instantly give up, because ... you know, nobody will ever benefit from this refactoring ...

The website rewards you with **points** if you make the tests pass, and writing software is so much more than making tests pass.
But when your motivation to code is getting points in a platform
(like [code wars](https://www.codewars.com/), [hackerrank](https://www.hackerrank.com/), etc ...) you often don't deal with the most challenging things in
software development. (such as [naming things](https://martinfowler.com/bliki/TwoHardThings.html))

Sure it exercises your concentration....
And thinking realy hard can be rewarding.
Maybe that why it's called *competitive programming*.

But Ruby is not about thinking really hard.
Quite the oposite, it is about using the proper tools to **think less hard**.

Of course, competing on such platforms could help beginners to get used to the syntax, eval and type checking rules.
But at some point, it starts to limit the exposure to the language, and to programming in general.
Not to mention careless beginers could take such bad habits to production.

