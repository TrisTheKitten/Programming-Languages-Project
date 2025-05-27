# Programming-Languages-Project
Nim Programming Language – Project README Summary
1 Overview

Nim is a statically-typed, compiled language that tries to read like Python while running as fast as C/C++

.
2 Origins

    Early 2000s – Andreas Rumpf sketches a Python-fast-as-C idea.

    2008 – First public release as Nimrod.

    2014 – Renamed to Nim; community and tooling mature 

    .

3 Key Strengths

    Speed & Portability – Compiles to C/C++/JS, so final code rivals hand-written C++ in benchmarks 

.

Powerful Macros – Compile-time AST macros let you build domain-specific mini-languages and cut boilerplate

.

Memory Choices – Mix tracing GC, reference counting, or manual ptr work; custom allocators allowed

.

Multi-Paradigm + Async – Imperative, OO, and functional styles live side-by-side; async/await coroutines make I/O code lean

    .

4 Main Weaknesses

    Small Library Pool – Fewer ready-made packages; more DIY work 

.

Steep On-Ramp – Macros and mixed memory modes demand study; docs still thin in spots

.

Shifting Ground – Spec and compiler still change; some code may break between releases

    .

5 How Nim Works
5.1 Syntax in a Nutshell

    Python-style indent blocks or optional {} braces.

    var (mutable), let (immutable), const (compile-time).

    Uniform Function Call Syntax lets any free function look like a method 

    .

5.2 Compilation Pipeline

parse → semantic-check → macro-expand → optimize → C-emit → backend compile

.
5.3 Runtime Snapshot

    Default deferred-ref-count GC with cycle detection.

    Manual memory and custom allocators for hot paths.

    Zero-cost exceptions when nothing throws.

    True threads for CPU tasks; coroutines for async I/O 

    .

6 Performance at a Glance
Longest Path benchmark (Intel Q9300 @ 2.5 GHz) showed:
Metric	Nim	C++
Exec time	1400 ms	1478 ms
Peak RAM	1460 KB	1460 KB
Compressed source	486 B	865 B
Nim led in speed and code compactness while keeping memory low

.
7 When to Pick Nim
Choose Nim when you need C-level speed, like clean readable code, and want one codebase that can target native apps, command-line tools, and browser JS without switch-rewriting.

8 When to Skip
Skip Nim for projects that rely on huge third-party ecosystems, demand iron-clad long-term ABI stability, or must onboard many new developers in a hurry.

9 Project Team
Min Myint Moh Soe · Hpone Pyae Khine · Ahkar Min Oo 

