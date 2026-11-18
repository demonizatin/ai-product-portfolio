# Simulated learners

**Problem.** Memory bugs only show up after several sessions with the same person. Testing that by hand takes days, and real users should not be the ones who find the failures.

**What I built.** A test rig where several AI-played learner personas talk to the tutor over many sessions. Each persona has a personality (one-word answerer, over-sharer, someone who contradicts themselves). A separate judge reads the transcripts and flags problems.

**The failure it caught.** The most useful find was a chain of three small errors:

1. The tutor's opening line took a vague memory and sharpened it into a specific detail that was never said.
2. The simulated learner, being polite, played along.
3. The memory system saved the invented detail as a fact.

One hallucination had turned into a permanent false memory. No single step looked wrong on its own.

**The fix.** Two rules: a vague memory must stay vague when it is brought up, and only concrete things the learner said can be followed up. Then I re-ran the same personas to confirm it was gone.

**What I took from it.** Each fix was followed by another run. Several rounds in, the remaining issues were tone and variety, not correctness.
