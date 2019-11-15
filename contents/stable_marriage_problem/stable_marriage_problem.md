# The Stable Marriage Problem
Imagine you have two groups, each of size \\(n\\).
Each individual within a group has an internal ranking associated with all members of the opposing group.
The *Stable Matching Problem* attempts to unite both groups into stable pairs.
In this case, a set of pairs is considered stable if there are no pairs that like each other more than their current partners.
This doesn't mean that everyone gets their top choices, but if an individual prefers someone else who also prefers them back, the set of pairs is not stable.

Now, this is often told as a story.
One group is male, the other is female, and everyone gets married, hence the name the *Stable Marriage Problem*.
This problem is solved by the Gale-Shapley algorithm, which can be simply described as follows:

1. All the men propose to their top choice of women.
2. The women become tentatively engaged to their top choice of the men who have proposed to them.
3. All rejected men propose to their next choice, and the women again select whichever man they prefer, possibly rejecting the one they were already engaged to.

This process continues until all individuals are paired, which means that this algorithm guarantees stable matching and also has a \\(\mathcal{O}(n^2)\\) runtime.
To be clear, even though this algorithm seems conceptually simple, it is rather tricky to implement correctly.
I do not at all claim that the code provided here is efficient and we will definitely be coming back to this problem in the future when we have more tools under our belt.
I am incredibly interested to see what you guys do and how you implement the algorithm.

## Video Explanation

Here is a video describing the stable marriage problem:

<div style="text-align:center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/A7xRZQAQU8s" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

## Example Code

### Code Examples

#### Code Example ruby

```ruby
{{#include code/ruby/stable_marriage.rb}}
```

#### Code Example Julia

```julia
{{#include code/julia/stable_marriage.jl}}
```

#### Code Example Python

```python
{{#include code/python/stable_marriage.py}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/stableMarriage.hs}}
```

#### Code Example C

```c
{{#include code/c/stable_marriage.c}}
```

#### Code Example C++

```cpp
{{#include code/c++/stable_marriage.cpp}}
```

#### Code Example JavaScript

```javascript
{{#include code/javascript/stable-marriage.js}}
```

#### Code Example C#

##### GaleShapleyAlgorithm.cs

```csharp
{{#include code/csharp/GaleShapleyAlgorithm.cs}}
```

##### Person.cs

```csharp
{{#include code/csharp/Person.cs}}
```

##### Program.cs

```csharp
{{#include code/csharp/Program.cs}}
```

##### ListExtensions.cs

```csharp
{{#include code/csharp/ListExtensions.cs}}
```

#### Code Example Java

```java
{{#include code/java/stable-marriage.java}}
```

#### Code Example PHP

```php
{{#include code/php/stable_marriage.php}}
```

#### Code Example Scala

```scala
{{#include code/scala/stable_marriage.scala}}
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
