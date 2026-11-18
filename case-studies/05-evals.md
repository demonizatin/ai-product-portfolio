# Evals before changes

**Problem.** The team suspected the feedback model was the weak link and wanted to try a newer one. Nobody could say how often the current one was actually wrong.

**What I built.**
- A small tool that loads real production outputs and lets a person mark each one correct or incorrect, quickly, with keyboard shortcuts. Human judgment is the gate, capped at about a hundred a day so quality holds.
- An analysis step where a stronger model reads the labelled set and looks for patterns in the failures.
- A benchmark that runs the same labelled cases through a dozen-plus candidate models with the production prompt.

**What it found.**
- The model already in production came out on top. Switching would have cost time and made things worse.
- The real problems were in the output format: fields returned in the wrong shape, positions in the text that were made up, and a few responses wrapped in a way the app could not read. Those are prompt and parsing fixes, not model problems.

**What I took from it.** "Try a better model" is the most tempting fix and often the wrong one. A couple of hundred labelled cases was enough to know.

**Try it.** A generic, open version of this approach, on invented sample data: [live demo](https://demonizatin.github.io/llm-eval-kit/) and [code with tests](https://github.com/demonizatin/llm-eval-kit).
