# Bogo Sort
Look, Bogo Sort doesn't really sort anything out.
In fact, it should never be used in practice for any reason I can think of and really only serves as a joke in the programming community.
As far as jokes go, though, this one's pretty good.

So, here's how it goes:
imagine you have an array of \\(n\\) elements that you want sorted.
One way to do it is to shuffle the array at random and hope that all the elements will be magically in order after shuffling.
If they are not in order, just shuffle everything again.
And then again. And again.
In the best case, this algorithm runs with a complexity of \\(\Omega(n)\\), and in the worst, \\(\mathcal{O}(\infty)\\).

In code, it looks something like this:

### Code Examples

#### Code Example jl

```julia
{{#include code/julia/bogo.jl:12:16}}
```

#### Code Example cs

```csharp
{{#include code/csharp/BogoSort.cs:9:15}}
```

#### Code Example clj

```clojure
{{#include code/clojure/bogo.clj:7:11}}
```

#### Code Example c

```c
{{#include code/c/bogo_sort.c:25:29}}
```

#### Code Example java

```java
{{#include code/java/Bogo.java:2:6}}
```

#### Code Example js

```javascript
{{#include code/javascript/bogo.js:11:15}}
```

#### Code Example py

```python
{{#include code/python/bogo.py:10:12}}
```

#### Code Example hs

```haskell
{{#include code/haskell/bogoSort.hs:17:20}}
```

#### Code Example m

```matlab
{{#include code/matlab/bogosort.m:21:28}}
```

#### Code Example lua

```lua
{{#include code/lua/bogosort.lua:1:22}}
```

#### Code Example cpp

```cpp
{{#include code/c++/bogosort.cpp:33:38}}
```

#### Code Example rs

```rust
{{#include code/rust/bogosort.rs:16:20}}
```

#### Code Example swift

```swift
{{#include code/swift/bogosort.swift:13:19}}
```

#### Code Example php

```php
{{#include code/php/bogo_sort.php:15:22}}
```

#### Code Example nim

```nim
{{#include code/nim/bogo_sort.nim:16:18}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/bogo.rb:12:16}}
```

#### Code Example emojic

```emojicode
{{#include code/emojicode/bogo_sort.emojic:2:6}}
```

#### Code Example factor

```factor
{{#include code/factor/bogo_sort.factor:10:12}}
```

#### Code Example f90

```fortran
{{#include code/fortran/bogo.f90:24:32}}
```

#### Code Example racket

```lisp
{{#include code/racket/bogo_sort.rkt:3:8}}
```

#### Code Example st

```smalltalk
{{#include code/smalltalk/bogosort.st:2:6}}
```

#### Code Example bash

```bash
{{#include code/bash/bogo_sort.bash:38:45}}
```

#### Code Example asm-x64

```asm-x64
{{#include code/asm-x64/bogo_sort.s:93:113}}
```

#### Code Example lisp

```lisp
{{#include code/clisp/bogo-sort.lisp:20:24}}
```

#### Code Example crystal

```crystal
{{#include code/crystal/bogo.cr:10:14}}
```

#### Code Example r

```r
{{#include code/r/bogo_sort.r:1:6}}
```

#### Code Example scala

```scala
{{#include code/scala/bogo.scala:12:16}}
```

#### Code Example go

```go
{{#include code/go/bogo_sort.go:27:31}}
```

That's it.
Ship it!
We are done here!

## Example Code

### Code Examples

#### Code Example jl

```julia
{{#include code/julia/bogo.jl}}
```

#### Code Example cs

##### BogoSort.cs

```csharp
{{#include code/csharp/BogoSort.cs}}
```

##### Program.cs

```csharp
{{#include code/csharp/Program.cs}}
```

#### Code Example clj

```clojure
{{#include code/clojure/bogo.clj}}
```

#### Code Example c

```c
{{#include code/c/bogo_sort.c}}
```

#### Code Example java

```java
{{#include code/java/Bogo.java}}
```

#### Code Example js

```javascript
{{#include code/javascript/bogo.js}}
```

#### Code Example py

```python
{{#include code/python/bogo.py}}
```

#### Code Example hs

```haskell
{{#include code/haskell/bogoSort.hs}}
```

#### Code Example m

```matlab
{{#include code/matlab/bogosort.m}}
```

#### Code Example lua

```lua
{{#include code/lua/bogosort.lua}}
```

#### Code Example cpp

```cpp
{{#include code/c++/bogosort.cpp}}
```

#### Code Example rs

```rust
{{#include code/rust/bogosort.rs}}
```

#### Code Example swift

```swift
{{#include code/swift/bogosort.swift}}
```

#### Code Example php

```php
{{#include code/php/bogo_sort.php}}
```

#### Code Example nim

```nim
{{#include code/nim/bogo_sort.nim}}
```

#### Code Example ruby

```ruby
{{#include code/ruby/bogo.rb}}
```

#### Code Example emojic

```emojicode
{{#include code/emojicode/bogo_sort.emojic}}
```

#### Code Example factor

```factor
{{#include code/factor/bogo_sort.factor}}
```

#### Code Example f90

```fortran
{{#include code/fortran/bogo.f90}}
```

#### Code Example racket

```lisp
{{#include code/racket/bogo_sort.rkt}}
```

#### Code Example st

```smalltalk
{{#include code/smalltalk/bogosort.st}}
```

#### Code Example bash

```bash
{{#include code/bash/bogo_sort.bash}}
```

#### Code Example asm-x64

```asm-x64
{{#include code/asm-x64/bogo_sort.s}}
```

#### Code Example lisp

```lisp
{{#include code/clisp/bogo-sort.lisp}}
```

#### Code Example crystal

```crystal
{{#include code/crystal/bogo.cr}}
```

#### Code Example r

```r
{{#include code/r/bogo_sort.r}}
```

#### Code Example scala

```scala
{{#include code/scala/bogo.scala}}
```

#### Code Example go

```go
{{#include code/go/bogo_sort.go}}
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
