Analyzable sandboxing
=====================

Analyzable sandboxing - programming language feature allowing to controllably execute untrusted code.

The closest solution today is sanboxing in [Lua](https://www.lua.org/) programming language.

And although the Lua way is most developed technological approach for today,
it still has a lot of disadvantages drastically reducing amount of applications:
- no way to guarantee not only execution time of untrusted function but a fact of completion itself
- dynamic typing of the language itself make programs in the language ineffective both in terms of performance and memory usage

The HardCode programming language way solve declared issues brilliantly:
- source code analyzability allows to know full function execution computational complexity and function interruption computational complexity (if there is an interruption)
  "out-of-the-box" <b><i>at compilation stage</i></b>
- and so there is a way to estimate execution duration and interruption latency and allow only quota complying functions for execution
  (quotation can be done both by estimated execution duration and computation complexity)
- static typing combined with dynamic linkage gives the language performance that sometimes may beat even C,
  yet implementing the most advanced embedding and sandboxing

More details are given in [presentations](../presentations).
