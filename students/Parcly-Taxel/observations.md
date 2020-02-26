### Project: MarkBind / D3

Essentially "Markdown plus", MarkBind is a tool to generate dynamic websites using a Markdown-like syntax. It supports tooltips, icons, search, navigation and more.

[D3](https://d3js.org) stands for Data-Driven Documents and is a JavaScript library for manipulating web pages based on data. It is comprised of several modules (d3-array, d3-color, etc.) that can be imported either independently or all at once, and contributions to this project are per-module. [Observable](https://observablehq.com), by the same author as D3 ([Mike Bostock](https://github.com/mbostock)), is a web application for creating interactive notebooks that uses D3.

### My Contributions

* MarkBind: authored [pull request #1035](https://github.com/MarkBind/markbind/pull/1035) to fix [issue #1001](https://github.com/MarkBind/markbind/issues/1001).
* [d3-random](https://github.com/d3/d3-random): authored [pull request #30](https://github.com/d3/d3-random/pull/30) that fixed three issues among other improvements. It was subsequently merged as part of a new release [v2.1.0](https://github.com/d3/d3-random/releases/tag/v2.1.0).

### My Observations

MarkBind is an NUS-OSS project that functions much like other projects out in the open.

* Pull requests need at least one approval (review) before merging.
* There is a set template that appears when making a new pull request, detailing fields that ideally should be filled in before submitting.

For D3:

* Despite the project's size and reach, Bostock is the only person who performs the actual merges. He was very busy handling other parts of D3 while my pull request awaited merging.
* The use of Observable notebooks to explain new contributions to D3 is encouraged.
* D3 uses modules, but other ES6 features (e.g. `**` for exponentiation) are not widely used in older code – the project started before ES6 came out. There is no style guide on this matter; seeing that d3-random did not heavily use ES6, I stuck to ES5 when writing the pull request for it, and Bostock did not mind.
