# AI product work

I'm Priyansh, a product manager in Bengaluru. I'm currently the only PM at PeerUp, an AI spoken-English app with close to 5M users, most of them first-time learners from Tier 2 and 3 cities in India.

I build the AI features I propose: the prompts, the pipeline around them, and the tests that tell me whether they work. This repo is a set of short write-ups of that work. The code belongs to my employer, so what you get here is the design: what the problem was, how the AI is used, what broke, and what I changed.

| Project | What it is | The interesting part |
|---|---|---|
| [Tutor memory](case-studies/01-tutor-memory.md) | An AI tutor that remembers a learner across sessions | The model never decides what is true. Code does. |
| [Personalisation engine](case-studies/02-personalisation-engine.md) | Decides what to notify, when, and what to teach next | Driven by what the learner said and the mistakes they make |
| [Simulated learners](case-studies/03-simulated-learners.md) | AI-played personas that stress-test the tutor | Caught a failure where an invented detail became a saved "fact" |
| [Post-call feedback](case-studies/04-post-call-feedback.md) | Line-by-line feedback after a speaking call | One big prompt replaced by a chain of small checks |
| [Evals before changes](case-studies/05-evals.md) | Hand-labelling tool and model benchmark | The result was "don't switch models" |
| [Speech lessons](case-studies/06-speech-lessons.md) | Speaking lessons for Indian accents | Learners were losing their first words. Fixed in the mic, not the model. |
| [Competitor digest](case-studies/07-competitor-digest.md) | Automated digest of what competitors ship | Many sources, one dashboard |
| [One-click LiveOps](case-studies/08-one-click-liveops.md) | Daily content from idea to live in one click | AI tools handing work to each other, no API integration |
| [Word games](case-studies/09-word-games.md) | Two-player English word games and a daily puzzle | Real-time multiplayer, built and shipped solo |

## How I work with AI

A few rules I keep coming back to. Each one came from something going wrong.

1. **Code picks, the model phrases.** Anything that has to be correct (dates, which topic to raise, whether something was already said) is decided in code. The model only writes the sentence.
2. **Small prompts beat one big prompt.** A chain of narrow checks is easier to test, and when it fails you can see which step failed.
3. **Check the model's work with a second call.** Cheap, and it catches suggestions that sound fluent but are wrong.
4. **Label real outputs by hand before changing anything.** A hundred labelled cases settle arguments faster than opinions.
5. **Test with fake users first.** Simulated learners find the embarrassing failures before real ones do.

## Contact

[LinkedIn](https://www.linkedin.com/in/priyansh-shekhar-a3b212231/)
