# Monte Carlo Integration

Monte Carlo methods were some of the first methods I ever used for research, and when I learned about them, they seemed like some sort of magic.
Their premise is simple: random numbers can be used to integrate arbitrary shapes embedded into other objects.
Nowadays, "Monte Carlo" has become a bit of a catch-all term for methods that use random numbers to produce real results, but it all started as a straightforward method to integrate objects.
No matter how you slice it, the idea seems a bit crazy at first.
After all, random numbers are random.
How could they possibly be used to find non-random values?

Well, imagine you have a square.
The area of the square is simple, \\(\text{Area}_{\text{square}} = \text{length} \times \text{width}\\).
Since it's a square, the \\(\text{length}\\) and \\(\text{width}\\) are the same, so the formula is technically just \\(\text{Area}_{\text{square}} = \text{length}^2\\).
If we embed a circle into the square with a radius \\(r = \tfrac{length}{2}\\) (shown below), then its area is \\(\text{Area}_{\text{circle}}=\pi r^2\\).
For simplicity, we can also say that \\(\text{Area}_{\text{square}}=4r^2\\).

<p>
    <img  class="center" src="res/square_circle.png" width="300"/>
</p>

Now, let's say we want to find the area of the circle without an equation.
As we said before, it's embedded in the square, so we should be able to find some ratio of the area of the square to the area of the circle:

\\[
\text{Ratio} = \frac{\text{Area}_{\text{circle}}}{\text{Area}_{\text{square}}}
\\]

This means,

\\[
\text{Area}_{\text{circle}} = \text{Area}_{\text{square}}\times\text{Ratio} = 4r^2 \times \text{ratio}
\\]

So, if we can find the \\(\text{Ratio}\\) and we know \\(r\\), we should be able to easily find the \\(\text{Area}_{\text{circle}}\\).
The question is, "How do we easily find the \\(\text{Ratio}\\)?"
Well, one way is with *random sampling*.
We basically just pick a bunch of points randomly in the square, and
each point is tested to see whether it's in the circle or not:

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/monte_carlo.jl:2:7}}
```

#### Code Example Clojure

```clojure
{{#include code/clojure/monte_carlo.clj:3:10}}
```

#### Code Example C

```c
{{#include code/c/monte_carlo.c:7:9}}
```

#### Code Example C++

```cpp
{{#include code/c++/monte_carlo.cpp:7:16}}
```

#### Code Example JavaScript

```javascript
{{#include code/javascript/monte_carlo.js:2:6}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/monteCarlo.hs:7:7}}
```

#### Code Example Rust

```rust
{{#include code/rust/monte_carlo.rs:7:9}}
```

#### Code Example D

```d
{{#include code/d/monte_carlo.d:2:5}}
```

#### Code Example Go

```go
{{#include code/go/monteCarlo.go:12:14}}
```

#### Code Example R

```r
{{#include code/r/monte_carlo.R:2:6}}
```

#### Code Example Java

```java
{{#include code/java/MonteCarlo.java:12:14}}
```

#### Code Example swift

```swift
{{#include code/swift/monte_carlo.swift:1:3}}
```

#### Code Example Python

```python
{{#include code/python/monte_carlo.py:5:7}}
```

#### Code Example C#

```csharp
{{#include code/csharp/Circle.cs:23:23}}
```

#### Code Example Nim

```nim
{{#include code/nim/monte_carlo.nim:6:7}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/monte_carlo.rb:1:4}}
```

#### Code Example Fortran90

```fortran
{{#include code/fortran/monte_carlo.f90:1:8}}
```

#### Code Example Factor

```factor
{{#include code/factor/monte_carlo.factor:9:12}}
```

#### Code Example Emojicode

```emojicode
{{#include code/emojicode/monte_carlo.emojic:23:27}}
```

#### Code Example PHP

```php
{{#include code/php/monte_carlo.php:4:7}}
```

#### Code Example Lua

```lua
{{#include code/lua/monte_carlo.lua:1:3}}
```

#### Code Example Racket

```lisp
{{#include code/racket/monte_carlo.rkt:2:4}}
```

#### Code Example Scala

```scala
{{#include code/scala/monte_carlo.scala:3:3}}
```

#### Code Example Common Lisp

```lisp
{{#include code/clisp/monte-carlo.lisp:3:5}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/monte_carlo.s:21:32}}
```

#### Code Example Bash

```bash
{{#include code/bash/monte_carlo.bash:2:10}}
```

#### Code Example Kotlin

```kotlin
{{#include code/kotlin/MonteCarlo.kt:3:3}}
```

If it's in the circle, we increase an internal count by one, and in the end,

\\[
\text{Ratio} = \frac{\text{count in circle}}{\text{total number of points used}}
\\]

If we use a small number of points, this will only give us a rough approximation, but as we start adding more and more points, the approximation becomes much, much better (as shown below)!

<p>
    <img  class="center" src="res/monte_carlo.gif" width="400"/>
</p>

The true power of Monte Carlo comes from the fact that it can be used to integrate literally any object that can be embedded into the square.
As long as you can write some function to tell whether the provided point is inside the shape you want (like `in_circle()` in this case), you can use Monte Carlo integration!
This is obviously an incredibly powerful tool and has been used time and time again for many different areas of physics and engineering.
I can guarantee that we will see similar methods crop up all over the place in the future!

## Video Explanation

Here is a video describing Monte Carlo integration:

<div style="text-align:center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/AyBNnkYrSWY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

## Example Code
Monte Carlo methods are famous for their simplicity.
It doesn't take too many lines to get something simple going.
Here, we are just integrating a circle, like we described above; however, there is a small twist and trick.
Instead of calculating the area of the circle, we are instead trying to find the value of \\(\pi\\), and
rather than integrating the entire circle, we are only integrating the upper right quadrant of the circle from \\(0 < x, y < 1\\).
This saves a bit of computation time, but also requires us to multiply our output by \\(4\\).

That's all there is to it!
Feel free to submit your version via pull request, and thanks for reading!

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/monte_carlo.jl}}
```

#### Code Example Clojure

```clojure
{{#include code/clojure/monte_carlo.clj}}
```

#### Code Example C

```c
{{#include code/c/monte_carlo.c}}
```

#### Code Example C++

```cpp
{{#include code/c++/monte_carlo.cpp}}
```

#### Code Example JavaScript

```javascript
{{#include code/javascript/monte_carlo.js}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/monteCarlo.hs}}
```

#### Code Example Rust

```rust
{{#include code/rust/monte_carlo.rs}}
```

#### Code Example D

```d
{{#include code/d/monte_carlo.d}}
```

#### Code Example Go

```go
{{#include code/go/monteCarlo.go}}
```

#### Code Example R

```r
{{#include code/r/monte_carlo.R}}
```

#### Code Example Java

```java
{{#include code/java/MonteCarlo.java}}
```

#### Code Example swift

```swift
{{#include code/swift/monte_carlo.swift}}
```

#### Code Example Python

```python
{{#include code/python/monte_carlo.py}}
```

#### Code Example C#

##### MonteCarlo.cs

```csharp
{{#include code/csharp/MonteCarlo.cs}}
```

##### Circle.cs

```csharp
{{#include code/csharp/Circle.cs}}
```

##### Program.cs

```csharp
{{#include code/csharp/Program.cs}}
```

#### Code Example Nim

```nim
{{#include code/nim/monte_carlo.nim}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/monte_carlo.rb}}
```

#### Code Example Fortran90

```fortran
{{#include code/fortran/monte_carlo.f90}}
```

#### Code Example Factor

```factor
{{#include code/factor/monte_carlo.factor}}
```

#### Code Example Emojicode

```emojicode
{{#include code/emojicode/monte_carlo.emojic}}
```

#### Code Example PHP

```php
{{#include code/php/monte_carlo.php}}
```

#### Code Example Lua

```lua
{{#include code/lua/monte_carlo.lua}}
```

#### Code Example Racket

```lisp
{{#include code/racket/monte_carlo.rkt}}
```

#### Code Example Scala

```scala
{{#include code/scala/monte_carlo.scala}}
```

#### Code Example Common Lisp

```lisp
{{#include code/clisp/monte-carlo.lisp}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/monte_carlo.s}}
```

#### Code Example Bash

```bash
{{#include code/bash/monte_carlo.bash}}
```

#### Code Example Kotlin

```kotlin
{{#include code/kotlin/MonteCarlo.kt}}
```

<script>
MathJax.Hub.Queue(["Typeset",MathJax.Hub]);
</script>

## License

##### Code Examples

The code examples are licensed under the MIT license (found in [LICENSE.md](https://github.com/algorithm-archivists/algorithm-archive/blob/master/LICENSE.md)).

##### Text

The text of this chapter was written by [James Schloss](https://github.com/leios) and is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/legalcode).

[<p><img  class="center" src="../cc/CC-BY-SA_icon.svg" /></p>](https://creativecommons.org/licenses/by-sa/4.0/)

##### Images/Graphics
- The image "[squarecircle](res/square_circle.png)" was created by [James Schloss](https://github.com/leios) and is licenced under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/legalcode).
- The animation "[simplemontecarlo](res/monte_carlo.gif)" was created by [James Schloss](https://github.com/leios) and is licenced under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/legalcode).


##### Pull Requests

After initial licensing ([#560](https://github.com/algorithm-archivists/algorithm-archive/pull/560)), the following pull requests have modified the text or graphics of this chapter:
- none
