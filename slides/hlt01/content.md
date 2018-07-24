# 
<!-- .element: class="title" -->

# Introduction
<!-- .element: class="section-heading" -->
What is Haskell, and why is it called as a “Pure Functional Language”
<!-- .element: class="section-brief" -->

---

# Introduction
<!-- .element: class="title" -->
<br/>
<!-- .element: style="line-height: 1;" -->
### What is Haskell?

Pure _Functional Programming_ Language
<!-- .element: style="text-align: center;" -->

![04-01](images/04-01.png)
<!-- .element: style="border:0;" -->

_Functional Programming_ is a style in which the basic method of computations is by _**application of functions to arguments**_.
In the illustration above:

<div>
- `f()` is **applied** to `arg1` and `arg2`
- `g()` is **applied** to output of `f()` and another function `h()`, i.e., _`h()` itself becomes an argument to `g()`!_
</div>
<!-- .element: style="text-align: left; line-height: 1.5;" -->

---

# Introduction
<!-- .element: class="title" -->
<br/>
### What is a "pure" Function?

Output depends only on the inputs, i.e., a function of only inputs.
<!-- .element: style="text-align: center;" -->

![05-01](images/05-01.png)
<!-- .element: style="border:0;" -->

Pure function maintains **Referential Transparency**.

Everytime `f()` is called with the same `arg1` and `arg2`, it always outputs the same value. In other words, `f()` can be replaced by its output value without affecting the program behaviour.

---

# Introduction
<!-- .element: class="title" -->
<br/>
### Impure function

Output depends NOT only on the inputs, but also on some side-effects
<!-- .element: style="text-align: center;" -->

![06-01](images/06-01.png)
<!-- .element: style="border:0;" -->

An impure function “adds” additional effects to its outputs. These effects are unpredictable, because they originate from within the function. 

---

Introduction
<!-- .element: class="title" -->

<!-- Left side content -->
<div>
### Pure Function example* 
<!-- .element: style="text-align: center"-->

```
function f(a, b)
{
  return a + b
}
```

Output depends only on values of arguments `a` and `b`.

</div>
 <!-- .element: style="line-height: 1.5; float:left; width: 49%; text-align: left;" -->

<!-- Right side content -->
<div>
### Impure function example*
<!-- .element: style="text-align: center"-->

```
c = 6

function f(a, b)
{
  return a + b + c
}
```

Output depends on not only arguments `a` and `b`, but also on an external variable `c`. This is the side-effect: the function cannot control its output, and is always also dependant on `c` (not controlled by the function).

<br/>

</div>
<!-- .element: style="line-height: 1.5; float: right; width: 49%; text-align: left;" -->

<div>
*The examples are not Haskell examples, just a generic language for illustration.
</div>
<!-- .element: style="font-size: 20px; text-align: center; position: absolute; bottom: 0; width: 100%" -->

---

Introduction
<!-- .element: class="title" -->
<br/>
<!-- .element: style="line-height: 1;" -->
### More examples of impure functions
<!-- .element: style="color: white;" --> 

<!-- Left side content -->
<div>
#### Read from a memory address
<!-- .element: style="text-align: center"-->

![07-01](images/07-01.png)
<!-- .element: style="border:0;" -->

Function returns a `value` from a memory address `addr`, and has no control on its contents.

</div>
 <!-- .element: class="left-box" -->

<!-- Right side content -->
<div>
#### Read a key from keyboard
<!-- .element: style="text-align: center"-->

![07-02](images/07-02.png)
<!-- .element: style="border:0;" -->

Function returns the key pressed and _can_ return different values everytime.

<br/>

</div>
<!-- .element: class="right-box" -->

---

Introduction
<!-- .element: class="title" -->
<br/>
<!-- .element: style="line-height: 1;" -->
### Why does 'purity' matter?
<!-- .element: style="color: white;" -->

![08-01](images/08-01.png)
<!-- .element: style="border:0;" -->

### Some advantages:
<div>
- Makes “Static Code Analysis” very good
- Compiler can reason, and optimise better
- Testing of code can be based on reasoning
- Concurrency can be automatically achieved 
- And many more...
</div>
<!-- .element: style="line-height: 1.5;" -->

---

# 
<!-- .element: class="title" -->

# Code break
<!-- .element: class="section-heading" -->
Show me some code! Navigate down with down-arrow.
<!-- .element: class="section-brief" -->

===

# Basic Haskell
<!-- .element: class="title" -->

# &lt;To be continued&gt;

---

# 
<!-- .element: class="title" -->

# &lt;To be continued&gt;

---

<!-- CREDITS -->

Credits
<!-- .element: class="title" -->

<div>
&lt;Name1&gt; [github-username](https://github.com/github-username>)
</div>
<!-- .element: style="font-family: 'Courier New', Courier, monospace;font-size: 20px" -->
        
<div>
&lt;Name2&gt; [github-username](https://github.com/github-username>)
</div>
<!-- .element: style="font-family: 'Courier New', Courier, monospace;font-size: 20px" -->

---

# 
<!-- .element: class="title" -->

# Thank you!
<!-- .element: class="section-heading" -->

<div>
Want more? Join the [Haskell India Group](https://t.me/haskellindia)!
</div>
<!-- .element: class="section-brief" -->