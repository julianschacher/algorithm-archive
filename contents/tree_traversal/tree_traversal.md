# Tree Traversal

Trees are naturally recursive data structures, and because of this, we cannot access their elements like we might access the elements of a vector or array. Instead, we need to use more interesting methods to work through each element. This is often called *Tree Traversal*, and there are many different ways to do this. For now, we will restrict the discussion to two common and related methods of tree traversal: *Depth-First* and *Breadth-First Search*. Note that trees vary greatly in shape and size depending on how they are used; however, they are composed primarily of nodes that house other, children nodes, like so:

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/Tree.jl:3:7}}
```

#### Code Example C++

```cpp
{{#include code/c++/tree_example.cpp:12:15}}
```

#### Code Example C#

```csharp
{{#include code/csharp/Tree.cs:7:11}}
```

#### Code Example C

```c
{{#include code/c/tree_traversal.c:7:11}}
```

#### Code Example Java

```java
{{#include code/java/Tree.java:110:126}}
```

#### Code Example JavaScript

```javascript
{{#include code/javascript/tree.js:1:10}}
```

As a note, a `node` struct is not necessary in javascript, so this is an example of how a tree might be constructed.

#### Code Example Python

```python
{{#include code/python/Tree_example.py:1:4}}
```

#### Code Example Scratch

<p>
  <img  class="center" src="code/scratch/struct.svg" width="250" />
</p>

#### Code Example Rust

```rust
{{#include code/rust/tree.rs:4:7}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/TreeTraversal.hs:1:4}}
```

#### Code Example swift

```swift
{{#include code/swift/tree.swift:1:9}}
```

#### Code Example PHP

```php
{{#include code/php/tree_traversal.php:4:37}}
```

#### Code Example Crystal

```crystal
{{#include code/crystal/tree-traversal.cr:1:5}}
```

#### Code Example Go

```go
{{#include code/golang/treetraversal.go:5:8}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/tree_traversal.s:24:27}}
```

#### Code Example Emojicode

```emojicode
{{#include code/emojicode/tree_traversal.emojic:1:3}}
```

Because of this, the most straightforward way to traverse the tree might be recursive. This naturally leads us to the Depth-First Search (DFS) method:

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/Tree.jl:9:16}}
```

#### Code Example C++

```cpp
{{#include code/c++/tree_example.cpp:17:24}}
```

#### Code Example C#

```csharp
{{#include code/csharp/Tree.cs:34:45}}
```

#### Code Example C

```c
{{#include code/c/tree_traversal.c:37:45}}
```

#### Code Example Java

```java
{{#include code/java/Tree.java:21:27}}
```

#### Code Example JavaScript

```javascript
{{#include code/javascript/tree.js:12:15}}
```

#### Code Example Python

```python
{{#include code/python/Tree_example.py:18:23}}
```

#### Code Example Scratch

<p>
  <img  class="center" src="code/scratch/dfs.svg" width="250" />
  <img  class="center" src="code/scratch/dfs-from.svg" width="250" />
</p>

#### Code Example Rust

```rust
{{#include code/rust/tree.rs:9:15}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/TreeTraversal.hs:6:7}}
```

#### Code Example swift

```swift
{{#include code/swift/tree.swift:24:30}}
```

#### Code Example PHP

```php
{{#include code/php/tree_traversal.php:41:49}}
```

#### Code Example Crystal

```crystal
{{#include code/crystal/tree-traversal.cr:7:10}}
```

#### Code Example Go

```go
{{#include code/golang/treetraversal.go:10:15}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/tree_traversal.s:290:314}}
```

#### Code Example Emojicode

```emojicode
{{#include code/emojicode/tree_traversal.emojic:27:34}}
```

At least to me, this makes a lot of sense. We fight recursion with recursion! First, we first output the node we are on and then we call `DFS_recursive(...)` on each of its children nodes. This method of tree traversal does what its name implies: it goes to the depths of the tree first before going through the rest of the branches. In this case, the ordering looks like:

<p>
    <img  class="center" src="res/DFS_pre.png" width="500" />
</p>

Note that the in the code above, we are missing a crucial step: *checking to see if the node we are using actually exists!* Because we are using a vector to store all the nodes, we will be careful not to run into a case where we call `DFS_recursive(...)` on a node that has yet to be initialized; however, depending on the language we are using, we might need to be careful of this to avoid recursion errors!

Now, in this case the first element searched through is still the root of the tree. This type of tree traversal is known as *pre-order* DFS. We perform an action (output the ID) *before* searching through the children. If we shift the function around and place the data output at the end of the function, we can modify the order in which we search through the tree to be *post-order* and look something like this:


### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/Tree.jl:18:26}}
```

#### Code Example C++

```cpp
{{#include code/c++/tree_example.cpp:26:31}}
```

#### Code Example C#

```csharp
{{#include code/csharp/Tree.cs:47:58}}
```

#### Code Example C

```c
{{#include code/c/tree_traversal.c:47:53}}
```

#### Code Example Java

```java
{{#include code/java/Tree.java:34:41}}
```

#### Code Example JavaScript

```javascript
{{#include code/javascript/tree.js:17:20}}
```

#### Code Example Python

```python
{{#include code/python/Tree_example.py:26:31}}
```

#### Code Example Scratch

<p>
  <img  class="center" src="code/scratch/dfs-post.svg" width="300" />
</p>

#### Code Example Rust

```rust
{{#include code/rust/tree.rs:17:24}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/TreeTraversal.hs:9:10}}
```

#### Code Example swift

```swift
{{#include code/swift/tree.swift:32:38}}
```

#### Code Example PHP

```php
{{#include code/php/tree_traversal.php:51:57}}
```

#### Code Example Crystal

```crystal
{{#include code/crystal/tree-traversal.cr:12:15}}
```

#### Code Example Go

```go
{{#include code/golang/treetraversal.go:17:22}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/tree_traversal.s:316:344}}
```

#### Code Example Emojicode

```emojicode
{{#include code/emojicode/tree_traversal.emojic:36:43}}
```

<p>
    <img  class="center" src="res/DFS_post.png" width="500" />
</p>

In this case, the first node visited is at the bottom of the tree and moves up the tree branch by branch. In addition to these two types, binary trees have an *in-order* traversal scheme that looks something like this:

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/Tree.jl:28:43}}
```

#### Code Example C++

```cpp
{{#include code/c++/tree_example.cpp:34:52}}
```

#### Code Example C#

```csharp
{{#include code/csharp/Tree.cs:60:79}}
```

#### Code Example C

```c
{{#include code/c/tree_traversal.c:55:73}}
```

#### Code Example Java

```java
{{#include code/java/Tree.java:48:62}}
```

#### Code Example JavaScript

```javascript
{{#include code/javascript/tree.js:22:34}}
```

#### Code Example Python

```python
{{#include code/python/Tree_example.py:34:46}}
```

#### Code Example Scratch

<p>
  <img  class="center" src="code/scratch/dfs-in.svg" width="300" />
</p>

#### Code Example Rust

```rust
{{#include code/rust/tree.rs:25:40}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/TreeTraversal.hs:12:16}}
```

#### Code Example swift

```swift
{{#include code/swift/tree.swift:40:53}}
```

#### Code Example PHP

```php
{{#include code/php/tree_traversal.php:59:78}}
```

#### Code Example Crystal

```crystal
{{#include code/crystal/tree-traversal.cr:17:31}}
```

#### Code Example Go

```go
{{#include code/golang/treetraversal.go:24:38}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/tree_traversal.s:346:396}}
```

#### Code Example Emojicode

```emojicode
{{#include code/emojicode/tree_traversal.emojic:45:62}}
```

<p>
    <img  class="center" src="res/DFS_in.png" width="500" />
</p>


The order here seems to be some mix of the other 2 methods and works through the binary tree from left to right.

Now, at this point, it might seem that the only way to search through a recursive data structure is with recursion, but this is not necessarily the case! Rather surprisingly, we can perform a DFS non-recursively by using a stack, which are data structures that hold multiple elements, but only allow you to interact with the very last element you put in. The idea here is simple:

1. Put the root node in the stack
2. Take it out and put in its children
3. Pop the top of the stack and put its children in
4. Repeat 3 until the stack is empty

In code, it looks like this:

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/Tree.jl:45:56}}
```

#### Code Example C++

```cpp
{{#include code/c++/tree_example.cpp:55:70}}
```

#### Code Example C#

```csharp
{{#include code/csharp/Tree.cs:81:94}}
```

#### Code Example C

```c
{{#include code/c/tree_traversal.c:75:93}}
```

#### Code Example Java

```java
{{#include code/java/Tree.java:65:79}}
```

#### Code Example JavaScript

```javascript
{{#include code/javascript/tree.js:36:43}}
```

#### Code Example Python

```python
{{#include code/python/Tree_example.py:49:60}}
```

#### Code Example Scratch

<p>
  <img  class="center" src="code/scratch/dfs-stack.svg" width="400" />
</p>

#### Code Example Rust

```rust
{{#include code/rust/tree.rs:41:48}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/TreeTraversal.hs:18:22}}
```

#### Code Example swift

```swift
{{#include code/swift/tree.swift:55:67}}
```

#### Code Example PHP

```php
{{#include code/php/tree_traversal.php:80:91}}
```

#### Code Example Crystal

```crystal
{{#include code/crystal/tree-traversal.cr:33:41}}
```

#### Code Example Go

```go
{{#include code/golang/treetraversal.go:40:49}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/tree_traversal.s:398:445}}
```

#### Code Example Emojicode

```emojicode
{{#include code/emojicode/tree_traversal.emojic:64:79}}
```

All this said, there are a few details about DFS that might not be ideal, depending on the situation. For example, if we use DFS on an incredibly long tree, we will spend a lot of time going further and further down a single branch without searching the rest of the data structure. In addition, it is not the natural way humans would order a tree if asked to number all the nodes from top to bottom. I would argue a more natural traversal order would look something like this:

<p>
    <img  class="center" src="res/BFS_simple.png" width="500" />
</p>

And this is exactly what Breadth-First Search (BFS) does! On top of that, it can be implemented in the same way as the `DFS_stack(...)` function above, simply by swapping the `stack` for a `queue`, which is similar to a stack, except that it only allows you to interact with the very first element instead of the last. In code, this looks something like:

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/Tree.jl:58:69}}
```

#### Code Example C++

```cpp
{{#include code/c++/tree_example.cpp:73:86}}
```

#### Code Example C#

```csharp
{{#include code/csharp/Tree.cs:96:109}}
```

#### Code Example C

```c
{{#include code/c/tree_traversal.c:95:113}}
```

#### Code Example Java

```java
{{#include code/java/Tree.java:81:95}}
```

#### Code Example JavaScript

```javascript
{{#include code/javascript/tree.js:45:52}}
```

#### Code Example Python

```python
{{#include code/python/Tree_example.py:63:75}}
```

#### Code Example Scratch

<p>
  <img  class="center" src="code/scratch/bfs.svg" width="400" />
</p>

#### Code Example Rust

```rust
{{#include code/rust/tree.rs:50:58}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/TreeTraversal.hs:24:28}}
```

#### Code Example swift

```swift
{{#include code/swift/tree.swift:69:81}}
```

#### Code Example PHP

```php
{{#include code/php/tree_traversal.php:93:104}}
```

#### Code Example Crystal

```crystal
{{#include code/crystal/tree-traversal.cr:43:51}}
```

#### Code Example Go

```go
{{#include code/golang/treetraversal.go:51:60}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/tree_traversal.s:447:498}}
```

#### Code Example Emojicode

```emojicode
{{#include code/emojicode/tree_traversal.emojic:81:96}}
```

## Video Explanation

Here is a video describing tree traversal:

<div style="text-align:center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/cZPXfl_tUkA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

## Example Code

### Code Examples

#### Code Example Julia

```julia
{{#include code/julia/Tree.jl}}
```

#### Code Example C++

```cpp
{{#include code/c++/tree_example.cpp}}
```

#### Code Example C#

##### Tree.cs

```csharp
{{#include code/csharp/Tree.cs}}
```

##### Program.cs

```csharp
{{#include code/csharp/Program.cs}}
```

#### Code Example C

##### utility.h

```c
{{#include code/c/utility.h}}
```

##### tree_traversal.c

```c
{{#include code/c/tree_traversal.c}}
```

#### Code Example Java

##### Tree.java

```java
{{#include code/java/Tree.java}}
```

##### MainClass.java

```java
{{#include code/java/MainClass.java}}
```

#### Code Example JavaScript

```javascript
{{#include code/javascript/tree.js}}
```

#### Code Example Python

```python
{{#include code/python/Tree_example.py}}
```

#### Code Example Scratch

The code snippets were taken from this [Scratch project](https://scratch.mit.edu/projects/174017753/)

#### Code Example Rust

```rust
{{#include code/rust/tree.rs}}
```

#### Code Example Haskell

```haskell
{{#include code/haskell/TreeTraversal.hs}}
```

#### Code Example swift

```swift
{{#include code/swift/tree.swift}}
```

#### Code Example PHP

```php
{{#include code/php/tree_traversal.php}}
```

#### Code Example Crystal

```crystal
{{#include code/crystal/tree-traversal.cr}}
```

#### Code Example Go

```go
{{#include code/golang/treetraversal.go}}
```

#### Code Example X86-64 Assembly

```asm-x64
{{#include code/asm-x64/tree_traversal.s}}
```

#### Code Example Emojicode

```emojicode
{{#include code/emojicode/tree_traversal.emojic}}
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
- The image "[DFSpreorder](res/DFS_pre.png)" was created by [James Schloss](https://github.com/leios) and is licenced under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/legalcode).
- The image "[DFSpostorder](res/DFS_post.png)" was created by [James Schloss](https://github.com/leios) and is licenced under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/legalcode).
- The image "[DFSinorder](res/DFS_in.png)" was created by [James Schloss](https://github.com/leios) and is licenced under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/legalcode).
- The image "[BFSsimple](res/BFS_simple.png)" was created by [James Schloss](https://github.com/leios) and is licenced under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/legalcode).


##### Pull Requests

After initial licensing ([#560](https://github.com/algorithm-archivists/algorithm-archive/pull/560)), the following pull requests have modified the text or graphics of this chapter:
- none
