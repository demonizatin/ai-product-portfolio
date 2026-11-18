# Speech lessons

**Problem.** New learners needed guided speaking practice before an open conversation with the tutor. Speech recognition tuned for American English kept failing them, and a learner who is told "wrong" when they were right does not come back.

**What I built.** Playable speaking lessons (tap, build a sentence, then say it) on top of a speech stack chosen for Indian accents, with a second provider as fallback.

**Problems found by watching learners.**
- **Lost first words.** Recording started a fraction of a second after the mic button turned green, so the first word was cut. The mic now keeps about a second of audio in a rolling buffer and prepends it. A mic fix, not a model fix.
- **Recognition that "helps".** Priming the recogniser with the expected sentence made it hear the right answer even when the learner said something else. I turned priming off so it reports what was really said.
- **No sign of life.** Learners could not tell whether the mic was listening. Added a live level meter driven by the same audio.

**How it was tested.** A tester mode recorded each session to a dashboard, so I could see where real learners got stuck and fix both the screens and the lesson content.

