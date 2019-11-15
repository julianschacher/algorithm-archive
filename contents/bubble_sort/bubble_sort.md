# Bubble Sort
When it comes to sorting algorithms, Bubble Sort is usually the first that comes to mind.
Though it might not be the fastest tool in the shed, it's definitely straightforward to implement and is often the first sorting method new programmers think of when trying to implement a sorting method on their own.

Here's how it works: we go through each element in our vector and check to see if it is larger than the element to it's right.
If it is, we swap the elements and then move to the next element.
In this way, we sweep through the array \\(n\\) times for each element and continually swap any two adjacent elements that are improperly ordered.
This means that we need to go through the vector \\(\mathcal{O}(n^2)\\) times with code similar to the following:

### Code Examples

#### Code Example jl

```julia
{{#include code/julia/bubble.jl:1:10}}
```

#### Code Example cs

```csharp
{{#include code/csharp/BubbleSort.cs:9:27}}
```

#### Code Example c

```c
{{#include code/c/bubble_sort.c:10:20}}
```

#### Code Example c8

```chip-8
{{#include code/chip8/bubblesort.c8:39:63}}
```

#### Code Example java

```java
{{#include code/java/Bubble.java:2:12}}
```

#### Code Example kotlin

```kotlin
{{#include code/kotlin/BubbleSort.kt:1:11}}
```

#### Code Example js

```javascript
{{#include code/javascript/bubble.js:1:12}}
```

#### Code Example py

```python
{{#include code/python/bubblesort.py:4:9}}
```

#### Code Example m

```matlab
{{#include code/matlab/bubblesort.m:1:13}}
```

#### Code Example lua

```lua
{{#include code/lua/bubble_sort.lua:1:9}}
```

#### Code Example hs

```haskell
{{#include code/haskell/bubbleSort.hs}}
```

#### Code Example cpp

```cpp
{{#include code/c++/bubblesort.cpp:13:23}}
```

#### Code Example rs

```rust
{{#include code/rust/bubble_sort.rs:6:16}}
```

#### Code Example d

```d
{{#include code/d/bubble_sort.d:3:18}}
```

#### Code Example go

```go
{{#include code/go/bubbleSort.go:7:21}}
```

#### Code Example racket

```scheme
{{#include code/racket/bubbleSort.rkt:6:19}}
```

#### Code Example swift

```swift
{{#include code/swift/bubblesort.swift:1:13}}
```

#### Code Example ti83b

```ti-83_basic
{{#include code/ti83basic/BUBLSORT.txt:2:13}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/bubble.rb:3:13}}
```

#### Code Example crystal

```crystal
{{#include code/crystal/bubble.cr:1:11}}
```

#### Code Example php

```php
{{#include code/php/bubble_sort.php:4:17}}
```

#### Code Example lisp

```lisp
{{#include code/clisp/bubble_sort.lisp:3:28}}
```

#### Code Example nim

```nim
{{#include code/nim/bubble_sort.nim:5:9}}
```

#### Code Example st

```smalltalk
{{#include code/smalltalk/bubble.st:2:15}}
```

#### Code Example asm-x64

```asm-x64
{{#include code/asm-x64/bubble_sort.s:43:66}}
```

#### Code Example f90

```fortran
{{#include code/fortran/bubble.f90:19:40}}
```

#### Code Example bf

```brainfuck
{{#include code/brainfuck/bubblesort.bf:17:63}}
```

#### Code Example scala

```scala
{{#include code/scala/bubble_sort.scala:3:14}}
```

#### Code Example emojic

```emojicode
{{#include code/emojicode/bubble_sort.emojic:2:14}}
```

#### Code Example bash

```bash
{{#include code/bash/bubble_sort.bash:2:21}}
```

#### Code Example v

```v
{{#include code/v/bubble_sort.v:1:11}}
```

#### Code Example scratch

<p>
  <img  class="center" src="code/scratch/bubble_sort.svg" width="400" />
</p>

#### Code Example coffeescript

```coffeescript
{{#include code/coffeescript/bubblesort.coffee:1:6}}
```

... And that's it for the simplest bubble sort method.
Now, as you might imagine, computer scientists have optimized this to the fiery lakes of Michigan and back, so we'll come back to this in the future and talk about how to optimize it.
For now, it's fine to just bask in the simplicity that is bubble sort.
Trust me, there are plenty of more complicated algorithms that do precisely the same thing, only much, much better (for most cases).

## Example Code

### Code Examples

#### Code Example jl

```julia
{{#include code/julia/bubble.jl}}
```

#### Code Example cs

##### BubbleSort.cs

```csharp
{{#include code/csharp/BubbleSort.cs}}
```

##### Program.cs

```csharp
{{#include code/csharp/Program.cs}}
```

#### Code Example c

```c
{{#include code/c/bubble_sort.c}}
```

#### Code Example c8

```chip-8
{{#include code/chip8/bubblesort.c8}}
```

#### Code Example java

```java
{{#include code/java/Bubble.java}}
```

#### Code Example kotlin

```kotlin
{{#include code/kotlin/BubbleSort.kt}}
```

#### Code Example js

```javascript
{{#include code/javascript/bubble.js}}
```

#### Code Example py

```python
{{#include code/python/bubblesort.py}}
```

#### Code Example m

```matlab
{{#include code/matlab/bubblesort.m}}
```

#### Code Example lua

```lua
{{#include code/lua/bubble_sort.lua}}
```

#### Code Example hs

```haskell
{{#include code/haskell/bubbleSort.hs}}
```

#### Code Example cpp

```cpp
{{#include code/c++/bubblesort.cpp}}
```

#### Code Example rs

```rust
{{#include code/rust/bubble_sort.rs}}
```

#### Code Example d

```d
{{#include code/d/bubble_sort.d}}
```

#### Code Example go

```go
{{#include code/go/bubbleSort.go}}
```

#### Code Example racket

```scheme
{{#include code/racket/bubbleSort.rkt}}
```

#### Code Example swift

```swift
{{#include code/swift/bubblesort.swift}}
```

#### Code Example ti83b

```ti-83_basic
{{#include code/ti83basic/BUBLSORT.txt}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/bubble.rb}}
```

#### Code Example crystal

```crystal
{{#include code/crystal/bubble.cr}}
```

#### Code Example php

```php
{{#include code/php/bubble_sort.php}}
```

#### Code Example lisp

```lisp
{{#include code/clisp/bubble_sort.lisp}}
```

#### Code Example nim

```nim
{{#include code/nim/bubble_sort.nim}}
```

#### Code Example asm-x64

```asm-x64
{{#include code/asm-x64/bubble_sort.s}}
```

#### Code Example f90

```fortran
{{#include code/fortran/bubble.f90}}
```

#### Code Example bf

```brainfuck
{{#include code/brainfuck/bubblesort.bf}}
```

#### Code Example st

```smalltalk
{{#include code/smalltalk/bubble.st}}
```

#### Code Example scala

```scala
{{#include code/scala/bubble_sort.scala}}
```

#### Code Example emojic

```emojicode
{{#include code/emojicode/bubble_sort.emojic}}
```

#### Code Example bash

```bash
{{#include code/bash/bubble_sort.bash}}
```

#### Code Example v

```v
{{#include code/v/bubble_sort.v}}
```

#### Code Example scratch

The code snippet was taken from this [Scratch project](https://scratch.mit.edu/projects/316483792)

#### Code Example coffeescript

```coffeescript
{{#include code/coffeescript/bubblesort.coffee}}
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
