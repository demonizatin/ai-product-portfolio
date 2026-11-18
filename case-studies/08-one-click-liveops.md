# One-click LiveOps

**Problem.** The app runs a fresh debate topic every day. Each one needed a topic, a write-up, an image, a quality check and a publish step, passed between content, design and engineering.

**What I built.** A desktop tool where the whole chain, from idea to creation, testing, evaluation and going live, runs from one click.

**The smart part.** There is no API integration. Several AI tools and services hand work to each other directly: one researches and writes the topics, another produces the images, and checks run between each step.

**Details that made it reliable.**
- Output from the writing step is validated against a fixed structure, with one automatic retry if it fails.
- Image jobs run in parallel, each in its own isolated workspace so images cannot get attached to the wrong topic.
- Images are compressed automatically to a size limit before upload.
- A "trending" mode researches what people in India are talking about that week.

**Result.** What used to be a manual, multi-step job is now one click.
