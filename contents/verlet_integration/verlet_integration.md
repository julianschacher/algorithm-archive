# Verlet Integration

Verlet integration is essentially a solution to the kinematic equation for the motion of any object,

\\[
x = x_0 + v_0t + \frac{1}{2}at^2 + \frac{1}{6}bt^3 + \cdots
\\]

where \\(x\\) is the position, \\(v\\) is the velocity, \\(a\\) is the acceleration, \\(b\\) is the often forgotten jerk term, and \\(t\\) is time. This equation is a central equation to almost every Newtonian physics solver and brings up a class of algorithms known as *force integrators*. One of the first force integrators to work with is *Verlet Integration*.

So, let's say we want to solve for the next timestep in \\(x\\). To a close approximation (actually performing a Taylor Series Expansion about \\(x(t\pm \Delta t)\\)), that might look like this:

\\[
x(t+\Delta t) = x(t) + v(t)\Delta t + \frac{1}{2}a(t)\Delta t^2 + \frac{1}{6}b(t) \Delta t^3 + \mathcal{O}(\Delta t^4)
\\]

This means that if we need to find the next \\(x\\), we need the current \\(x\\), \\(v\\), \\(a\\), etc. However, because few people calculate the jerk term, our error is typically \\(\mathcal{O}(\Delta t^3)\\). That said, we can calculate \\(x\\) with less knowledge and higher accuracy if we play a trick! Let's say we want to calculate \\(x\\) of the *previous* timestep. Again, to a close approximation, that might look like this:

\\[
x(t-\Delta t) = x(t) - v(t)\Delta t + \frac{1}{2}a(t)\Delta t^2 - \frac{1}{6}b(t) \Delta t^3 + \mathcal{O}(\Delta t^4)
\\]

Now, we have two equations to solve for two different timesteps in x, one of which we already have. If we add the two equations together and solve for \\(x(t+\Delta t)\\), we find that

\\[
x(t+ \Delta t) = 2x(t) - x(t-\Delta t) + a(t)\Delta t^2 + \mathcal{O}(\Delta t^4)
\\]

So, this means we can find our next \\(x\\) simply by knowing our current \\(x\\), the \\(x\\) before that, and the acceleration! No velocity necessary! In addition, this drops the error to \\(\mathcal{O}(\Delta t^4)\\), which is great!
Here is what it looks like in code:

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/verlet.jl:1:13}}
```

#### Code Example C++

```cpp
{{#include code/c++/verlet.cpp:9:22}}
```

#### Code Example C

```c
{{#include code/c/verlet.c:3:14}}
```

#### Code Example Java

```java
{{#include code/java/Verlet.java:2:17}}
```

#### Code Example Python

```python
{{#include code/python/verlet.py:1:10}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/verlet.hs:14:21}}
```

#### Code Example Scratch

Unfortunately, this has not yet been implemented in scratch, so here's Julia code:

```julia
{{#include code/julia/verlet.jl:1:13}}
```

#### Code Example matlab

Unfortunately, this has not yet been implemented in matlab, so here's Julia code:

```julia
{{#include code/julia/verlet.jl:1:13}}
```

#### Code Example LabVIEW

Unfortunately, this has not yet been implemented in LabVIEW, so here's Julia code:

```julia
{{#include code/julia/verlet.jl:1:13}}
```

#### Code Example javascript

```javascript
{{#include code/javascript/verlet.js:1:14}}
```

#### Code Example Rust

```rust
{{#include code/rust/verlet.rs:1:13}}
```

#### Code Example swift

```swift
{{#include code/swift/verlet.swift:1:15}}
```

#### Code Example Fortran90

```fortran
{{#include code/fortran/verlet.f90:1:20}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/verlet.rb:1:14}}
```

#### Code Example Go

```go
{{#include code/golang/verlet.go:5:16}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/verlet.s:18:42}}
```

#### Code Example Kotlin

```kotlin
{{#include code/kotlin/verlet.kt:3:15}}
```

#### Code Example Nim

```nim
{{#include code/nim/verlet.nim:1:14}}
```

#### Code Example Common Lisp

```lisp
{{#include code/clisp/verlet.lisp:3:13}}
```

Now, obviously this poses a problem; what if we want to calculate a term that requires velocity, like the kinetic energy, \\(\frac{1}{2}mv^2\\)? In this case, we certainly cannot get rid of the velocity! Well, we can find the velocity to \\(\mathcal{O}(\Delta t^2)\\) accuracy by using the Stormer-Verlet method, which is the same as before, but we calculate velocity like so

\\[
v(t) = \frac{x(t+\Delta t) - x(t-\Delta t)}{2\Delta t} + \mathcal{O}(\Delta t^2)
\\]

Note that the 2 in the denominator appears because we are going over 2 timesteps. It's essentially solving \\(v=\frac{\Delta x}{\Delta t}\\). In addition, we can calculate the velocity of the next timestep like so

\\[
v(t+\Delta t) = \frac{x(t+\Delta t) - x(t)}{\Delta t} + \mathcal{O}(\Delta t)
\\]

However, the error for this is \\(\mathcal{O}(\Delta t)\\), which is quite poor, but it gets the job done in a pinch.  Here's what it looks like in code:

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/verlet.jl:15:31}}
```

#### Code Example C++

```cpp
{{#include code/c++/verlet.cpp:24:41}}
```

#### Code Example C

```c
{{#include code/c/verlet.c:16:31}}
```

#### Code Example Java

```java
{{#include code/java/Verlet.java:19:37}}
```

#### Code Example Python

```python
{{#include code/python/verlet.py:12:23}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/verlet.hs:23:28}}
```

#### Code Example Scratch

Unfortunately, this has not yet been implemented in scratch, so here's Julia code:

```julia
{{#include code/julia/verlet.jl:15:31}}
```

#### Code Example matlab

Unfortunately, this has not yet been implemented in matlab, so here's Julia code:

```julia
{{#include code/julia/verlet.jl:15:31}}
```

#### Code Example LabVIEW

Unfortunately, this has not yet been implemented in LabVIEW, so here's Julia code:

```julia
{{#include code/julia/verlet.jl:15:31}}
```

#### Code Example javascript

```javascript
{{#include code/javascript/verlet.js:16:32}}
```

#### Code Example Rust

```rust
{{#include code/rust/verlet.rs:15:32}}
```

#### Code Example swift

```swift
{{#include code/swift/verlet.swift:17:34}}
```

#### Code Example Fortran90

```fortran
{{#include code/fortran/verlet.f90:22:42}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/verlet.rb:16:32}}
```

#### Code Example Go

```go
{{#include code/golang/verlet.go:18:30}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/verlet.s:44:71}}
```

#### Code Example Kotlin

```kotlin
{{#include code/kotlin/verlet.kt:17:30}}
```

#### Code Example Nim

```nim
{{#include code/nim/verlet.nim:16:32}}
```

#### Code Example Common Lisp

```lisp
{{#include code/clisp/verlet.lisp:15:26}}
```


Now, let's say we actually need the velocity to calculate out next timestep. Well, in this case, we simply cannot use the above approximation and instead need to use the *Velocity Verlet* algorithm.

# Velocity Verlet

In some ways, this algorithm is even simpler than above. We can calculate everything like

\\[
\begin{align}
x(t+\Delta t) &=x(t) + v(t)\Delta t + \frac{1}{2}a(t)\Delta t^2 \\
a(t+\Delta t) &= f(x(t+\Delta t)) \\
v(t+\Delta t) &= v(t) + \frac{1}{2}(a(t) + a(t+\Delta t))\Delta t
\end{align}
\\]

which is literally the kinematic equation above, solving for \\(x\\), \\(v\\), and \\(a\\) every timestep. You can also split up the equations like so

\\[
\begin{align}
v(t+\frac{1}{2}\Delta t) &= v(t) + \frac{1}{2}a(t)\Delta t \\
x(t+\Delta t) &=x(t) + v(t+\frac{1}{2}\Delta t)\Delta t \\
a(t+\Delta t) &= f(x(t+\Delta t)) \\
v(t+\Delta t) &= v(t+\frac{1}{2}\Delta t) + \frac{1}{2}a(t+\Delta t)\Delta t
\end{align}
\\]

Here is the velocity Verlet method in code:

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/verlet.jl:33:45}}
```

#### Code Example C++

```cpp
{{#include code/c++/verlet.cpp:43:54}}
```

#### Code Example C

```c
{{#include code/c/verlet.c:33:43}}
```

#### Code Example Java

```java
{{#include code/java/Verlet.java:39:51}}
```

#### Code Example Python

```python
{{#include code/python/verlet.py:25:34}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/verlet.hs:30:35}}
```

#### Code Example Scratch

Unfortunately, this has not yet been implemented in scratch, so here's Julia code:

```julia
{{#include code/julia/verlet.jl:33:45}}
```

#### Code Example matlab

Unfortunately, this has not yet been implemented in matlab, so here's Julia code:

```julia
{{#include code/julia/verlet.jl:33:45}}
```

#### Code Example LabVIEW

Unfortunately, this has not yet been implemented in LabVIEW, so here's Julia code:

```julia
{{#include code/julia/verlet.jl:33:45}}
```

#### Code Example javascript

```javascript
{{#include code/javascript/verlet.js:34:45}}
```

#### Code Example Rust

```rust
{{#include code/rust/verlet.rs:34:45}}
```

#### Code Example swift

```swift
{{#include code/swift/verlet.swift:36:49}}
```

#### Code Example Fortran90

```fortran
{{#include code/fortran/verlet.f90:44:60}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/verlet.rb:34:46}}
```

#### Code Example Go

```go
{{#include code/golang/verlet.go:32:42}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/verlet.s:73:101}}
```

#### Code Example Kotlin

```kotlin
{{#include code/kotlin/verlet.kt:32:42}}
```

#### Code Example Nim

```nim
{{#include code/nim/verlet.nim:34:45}}
```

#### Code Example Common Lisp

```lisp
{{#include code/clisp/verlet.lisp:28:35}}
```

Even though this method is more widely used than the simple Verlet method mentioned above, it unforunately has an error term of \\(\mathcal{O}(\Delta t^2)\\), which is two orders of magnitude worse. That said, if you want to have a simulaton with many objects that depend on one another --- like a gravity simulation --- the Velocity Verlet algorithm is a handy choice; however, you may have to play further tricks to allow everything to scale appropriately. These types of simulatons are sometimes called *n-body* simulations and one such trick is the Barnes-Hut algorithm, which cuts the complexity of n-body simulations from \\(\sim \mathcal{O}(n^2)\\) to \\(\sim \mathcal{O}(n\log(n))\\).

## Video Explanation

Here is a video describing Verlet integration:

<div style="text-align:center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/g55QvpAev0I" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

## Example Code

Both of these methods work simply by iterating timestep-by-timestep and can be written straightforwardly in any language. For reference, here are snippets of code that use both the classic and velocity Verlet methods to find the time it takes for a ball to hit the ground after being dropped from a given height.

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/verlet.jl}}
```

#### Code Example C++

```cpp
{{#include code/c++/verlet.cpp}}
```

#### Code Example C

```c
{{#include code/c/verlet.c}}
```

#### Code Example Java

```java
{{#include code/java/VerletValues.java}}
```

```java
{{#include code/java/Verlet.java}}
```

#### Code Example Python

```python
{{#include code/python/verlet.py}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/verlet.hs}}
```

#### Code Example Scratch

Submitted by Jie

<p>
    <img  class="center" src="code/scratch/verlet_scratch.png" />
</p>

Link: [https://scratch.mit.edu/projects/173039394/](https://scratch.mit.edu/projects/173039394/)

#### Code Example matlab

```matlab
{{#include code/matlab/verlet.m}}
```

#### Code Example LabVIEW

Submitted by P. Mekhail

<p>
    <img  class="center" src="code/labview/verlet_labview.png" />
</p>

#### Code Example javascript

```javascript
{{#include code/javascript/verlet.js}}
```

#### Code Example Rust

```rust
{{#include code/rust/verlet.rs}}
```

#### Code Example swift

```swift
{{#include code/swift/verlet.swift}}
```

#### Code Example Fortran90

```fortran
{{#include code/fortran/verlet.f90}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/verlet.rb}}
```

#### Code Example Go

```go
{{#include code/golang/verlet.go}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/verlet.s}}
```

#### Code Example Kotlin

```kotlin
{{#include code/kotlin/verlet.kt}}
```

#### Code Example Nim

```nim
{{#include code/nim/verlet.nim}}
```

#### Code Example Common Lisp

```lisp
{{#include code/clisp/verlet.lisp}}
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

##### Pull Requests

After initial licensing ([#560](https://github.com/algorithm-archivists/algorithm-archive/pull/560)), the following pull requests have modified the text or graphics of this chapter:
- none
