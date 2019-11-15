# Euclidean Algorithm

Computer science is (almost by definition) a science about computers -- a device first conceptualized in the 1800's. Computers have become so revolutionary, that it is difficult to think of our lives today without them. That said, *algorithms* are much older and have existed in the world for millennia. Incredibly, a few of the algorithms created before the Common Era (AD) are still in use today. One such algorithm was first described in Euclid's *Elements* (~ 300 BC) and has come to be known as the *Euclidean Algorithm*.

The algorithm is a simple way to find the *greatest common divisor* (GCD) of two numbers, which is useful for a number of different applications (like reducing fractions). The first method (envisioned by Euclid) uses simple subtraction:

### Code Examples

#### Code Example c

```c_cpp
{{#include code/c/euclidean_example.c:17:30}}
```

#### Code Example cs

```csharp
{{#include code/csharp/EuclideanAlgorithm.cs:8:23}}
```

#### Code Example clj

```clojure
{{#include code/clojure/euclidean_example.clj:2:8}}
```

#### Code Example cpp

```c_cpp
{{#include code/c++/euclidean.cpp:18:31}}
```

#### Code Example java

```java
{{#include code/java/EuclideanAlgo.java:3:16}}
```

#### Code Example kotlin

```kotlin
{{#include code/kotlin/Euclidean.kt:3:13}}
```

#### Code Example js

```javascript
{{#include code/javascript/euclidean_example.js:15:29}}
```

#### Code Example lisp

```lisp
{{#include code/clisp/euclidean.lisp:3:12}}
```

#### Code Example py

```python
{{#include code/python/euclidean_example.py:11:22}}
```

#### Code Example haskell

```haskell
{{#include code/haskell/euclidean_example.hs:2:8}}
```

#### Code Example rs

```rust
{{#include code/rust/euclidean_example.rs:3:15}}
```

#### Code Example ml

```ocaml
{{#include code/ocaml/euclidean_example.ml:9:17}}
```

#### Code Example go

```go
{{#include code/go/euclidean.go:25:38}}
```

#### Code Example swift

```swift
{{#include code/swift/euclidean_algorithm.swift:1:14}}
```

#### Code Example matlab

```matlab
{{#include code/matlab/euclidean.m:3:17}}
```

#### Code Example lua

```lua
{{#include code/lua/euclidean.lua:1:14}}
```

#### Code Example jl

```julia
{{#include code/julia/euclidean.jl:12:25}}
```

#### Code Example nim

```nim
{{#include code/nim/euclid_algorithm.nim:13:24}}
```

#### Code Example asm-x64

```asm-x64
{{#include code/asm-x64/euclidean_example.s:35:56}}
```

#### Code Example f90

```fortran
{{#include code/fortran/euclidean.f90:1:19}}
```

#### Code Example php

```php
{{#include code/php/euclidean.php:4:18}}
```

#### Code Example factor

```factor
{{#include code/factor/euclid.factor:1:13}}
```

#### Code Example ws

```whitespace
{{#include code/whitespace/euclidian_sub.ws}}
```

#### Code Example scala

```scala
{{#include code/scala/euclidean.scala:3:8}}
```

#### Code Example racket

```lisp
{{#include code/racket/euclidean_algorithm.rkt:3:14}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/euclidean.rb:8:19}}
```

#### Code Example st

```smalltalk
{{#include code/smalltalk/euclid.st:1:13}}
```

#### Code Example emojic

```emojicode
{{#include code/emojicode/euclidean_algorithm.emojic:2:17}}
```

#### Code Example lolcode

```LOLCODE
{{#include code/lolcode/euclid.lol:25:40}}
```

#### Code Example bash

```bash
{{#include code/bash/euclid.bash:24:38}}
```

#### Code Example d

```d
{{#include code/d/euclidean_algorithm.d:19:33}}
```

#### Code Example piet

> ![](code/piet/subtract/euclidian_algorithm_subtract_large.png) ![](code/piet/subtract/euclidian_algorithm_subtract.png)

#### Code Example ss

```scheme
{{#include code/scheme/euclidalg.ss:1:7}}
```

#### Code Example scratch

<p>
  <img  class="center" src="code/scratch/euclid_sub.svg" width="200" />
</p>


Here, we simply line the two numbers up every step and subtract the lower value from the higher one every timestep. Once the two values are equal, we call that value the greatest common divisor. A graph of `a` and `b` as they change every step would look something like this:

<p>
    <img  class="center" src="res/subtraction.png" width="500" />
</p>

Modern implementations, though, often use the modulus operator (%) like so

### Code Examples

#### Code Example c

```c_cpp
{{#include code/c/euclidean_example.c:4:16}}
```

#### Code Example cs

```csharp
{{#include code/csharp/EuclideanAlgorithm.cs:25:39}}
```

#### Code Example clj

```clojure
{{#include code/clojure/euclidean_example.clj:9:13}}
```

#### Code Example cpp

```c_cpp
{{#include code/c++/euclidean.cpp:5:15}}
```

#### Code Example java

```java
{{#include code/java/EuclideanAlgo.java:18:26}}
```

#### Code Example kotlin

```kotlin
{{#include code/kotlin/Euclidean.kt:15:26}}
```

#### Code Example js

```javascript
{{#include code/javascript/euclidean_example.js:1:13}}
```

#### Code Example lisp

```lisp
{{#include code/clisp/euclidean.lisp:14:18}}
```

#### Code Example py

```python
{{#include code/python/euclidean_example.py:1:9}}
```

#### Code Example haskell

```haskell
{{#include code/haskell/euclidean_example.hs:10:14}}
```

#### Code Example rs

```rust
{{#include code/rust/euclidean_example.rs:17:27}}
```

#### Code Example ml

```ocaml
{{#include code/ocaml/euclidean_example.ml:3:7}}
```

#### Code Example go

```go
{{#include code/go/euclidean.go:14:23}}
```

#### Code Example swift

```swift
{{#include code/swift/euclidean_algorithm.swift:16:27}}
```

#### Code Example matlab

```matlab
{{#include code/matlab/euclidean.m:19:31}}
```

#### Code Example lua

```lua
{{#include code/lua/euclidean.lua:16:25}}
```

#### Code Example jl

```julia
{{#include code/julia/euclidean.jl:1:10}}
```

#### Code Example nim

```nim
{{#include code/nim/euclid_algorithm.nim:1:11}}
```

#### Code Example asm-x64

```asm-x64
{{#include code/asm-x64/euclidean_example.s:10:33}}
```

#### Code Example f90

```fortran
{{#include code/fortran/euclidean.f90:21:34}}
```

#### Code Example php

```php
{{#include code/php/euclidean.php:20:30}}
```

#### Code Example factor

```factor
{{#include code/factor/euclid.factor:15:25}}
```

#### Code Example ws

```whitespace
{{#include code/whitespace/euclidian_mod.ws}}
```

#### Code Example scala

```scala
{{#include code/scala/euclidean.scala:10:14}}
```

#### Code Example racket

```lisp
{{#include code/racket/euclidean_algorithm.rkt:16:24}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/euclidean.rb:1:6}}
```

#### Code Example st

```smalltalk
{{#include code/smalltalk/euclid.st:15:25}}
```

#### Code Example emojic

```emojicode
{{#include code/emojicode/euclidean_algorithm.emojic:19:31}}
```

#### Code Example lolcode

```LOLCODE
{{#include code/lolcode/euclid.lol:9:23}}
```

#### Code Example bash

```bash
{{#include code/bash/euclid.bash:10:22}}
```

#### Code Example d

```d
{{#include code/d/euclidean_algorithm.d:4:17}}
```

#### Code Example piet

> ![](code/piet/mod/euclidian_algorithm_mod_large.png) ![](code/piet/mod/euclidian_algorithm_mod.png)

#### Code Example ss

```scheme
{{#include code/scheme/euclidalg.ss:9:12}}
```

#### Code Example scratch

<p>
  <img  class="center" src="code/scratch/euclid_mod.svg" width="200" />
</p>


Here, we set `b` to be the remainder of `a%b` and `a` to be whatever `b` was last timestep. Because of how the modulus operator works, this will provide the same information as the subtraction-based implementation, but when we show `a` and `b` as they change with time, we can see that it might take many fewer steps:

<p>
    <img  class="center" src="res/modulus.png" width="500" />
</p>

The Euclidean Algorithm is truly fundamental to many other algorithms throughout the history of computer science and will definitely be used again later. At least to me, it's amazing how such an ancient algorithm can still have modern use and appeal. That said, there are still other algorithms out there that can find the greatest common divisor of two numbers that are arguably better in certain cases than the Euclidean algorithm, but the fact that we are discussing Euclid two millennia after his death shows how timeless and universal mathematics truly is. I think that's pretty cool.

## Video Explanation

Here's a video on the Euclidean algorithm:

<div style="text-align:center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/h86RzlyHfUE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

## Example Code

### Code Examples

#### Code Example c

```c_cpp
{{#include code/c/euclidean_example.c}}
```

#### Code Example cs

##### EuclideanAlgorithm.cs

```csharp
{{#include code/csharp/EuclideanAlgorithm.cs}}
```

##### Program.cs

```csharp
{{#include code/csharp/Program.cs}}
```

#### Code Example clj

```clojure
{{#include code/clojure/euclidean_example.clj}}
```

#### Code Example cpp

```c_cpp
{{#include code/c++/euclidean.cpp}}
```

#### Code Example java

```java
{{#include code/java/EuclideanAlgo.java}}
```

#### Code Example js

```javascript
{{#include code/javascript/euclidean_example.js}}
```

#### Code Example lisp

```lisp
{{#include code/clisp/euclidean.lisp}}
```

#### Code Example py

```python
{{#include code/python/euclidean_example.py}}
```

#### Code Example haskell

```haskell
{{#include code/haskell/euclidean_example.hs}}
```

#### Code Example rs

```rust
{{#include code/rust/euclidean_example.rs}}
```

#### Code Example ml

```ocaml
{{#include code/ocaml/euclidean_example.ml}}
```

#### Code Example go

```go
{{#include code/go/euclidean.go}}
```

#### Code Example swift

```swift
{{#include code/swift/euclidean_algorithm.swift}}
```

#### Code Example matlab

```matlab
{{#include code/matlab/euclidean.m}}
```

#### Code Example lua

```lua
{{#include code/lua/euclidean.lua}}
```

#### Code Example jl

```julia
{{#include code/julia/euclidean.jl}}
```

#### Code Example nim

```nim
{{#include code/nim/euclid_algorithm.nim}}
```

#### Code Example asm-x64

```asm-x64
{{#include code/asm-x64/euclidean_example.s}}
```

#### Code Example f90

```fortran
{{#include code/fortran/euclidean.f90}}
```

#### Code Example php

```php
{{#include code/php/euclidean.php}}
```

#### Code Example factor

```factor
{{#include code/factor/euclid.factor}}
```

#### Code Example ws

Here is a readable version of the algorithms with comments. First, subtraction method:

```whitespace
{{#include code/whitespace/euclidian_sub_comments.ws}}
```

and modulo method:

```whitespace
{{#include code/whitespace/euclidian_mod_comments.ws}}
```

#### Code Example scala

```scala
{{#include code/scala/euclidean.scala}}
```

#### Code Example racket

```lisp
{{#include code/racket/euclidean_algorithm.rkt}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/euclidean.rb}}
```

#### Code Example st

```smalltalk
{{#include code/smalltalk/euclid.st}}
```

#### Code Example emojic

```emojicode
{{#include code/emojicode/euclidean_algorithm.emojic}}
```

#### Code Example lolcode

```LOLCODE
{{#include code/lolcode/euclid.lol}}
```

#### Code Example bash

```bash
{{#include code/bash/euclid.bash}}
```

#### Code Example d

```d
{{#include code/d/euclidean_algorithm.d}}
```

#### Code Example piet

A text version of the program is provided for both versions.

#### Subtraction

> ![](code/piet/subtract/euclidian_algorithm_subtract_large.png) ![](code/piet/subtract/euclidian_algorithm_subtract.png)

```piet
{{#include code/piet/euclidian_algorithm.piet:23:107}}
```

#### Modulo

> ![](code/piet/mod/euclidian_algorithm_mod_large.png) ![](code/piet/mod/euclidian_algorithm_mod.png)

```piet
{{#include code/piet/euclidian_algorithm.piet:126:146}}
```

#### Code Example ss

```scheme
{{#include code/scheme/euclidalg.ss}}
```

#### Code Example scratch

The code snippets were taken from this [Scratch project](https://scratch.mit.edu/projects/278727055/)

<p>
  <img  class="center" src="code/scratch/main.svg" width="200" />
</p>


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
- The image "[Euclidsub](res/subtraction.png)" was created by [James Schloss](https://github.com/leios) and is licenced under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/legalcode).
- The image "[Euclidmod](res/modulus.png)" was created by [James Schloss](https://github.com/leios) and is licenced under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/legalcode).


##### Pull Requests

After initial licensing ([#560](https://github.com/algorithm-archivists/algorithm-archive/pull/560)), the following pull requests have modified the text or graphics of this chapter:
- none
