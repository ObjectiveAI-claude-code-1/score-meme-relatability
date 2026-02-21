# score-meme-relatability

A scalar function that scores a single meme on its relatability — measuring how broadly it connects with the shared, often unspoken fabric of human experience.

## What It Does

`score-meme-relatability` takes a meme image and returns a score between **0** and **1**, where higher scores indicate stronger relatability. A score near 1 means the meme taps into something nearly everyone has felt. A score near 0 means it speaks only to a narrow or niche audience.

The function does not judge whether a meme is funny, well-designed, or topical. It answers one focused question: **how many people would look at this meme and feel personally seen?**

## Input

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `meme` | `image` | Yes | A self-contained meme image — typically an image with overlaid text, a captioned photo, a screenshot, or any visual format conveying a humorous or emotionally resonant observation about shared human experience. |

## Output

A scalar value in **[0, 1]** representing the meme's overall relatability.

| Score Range | Interpretation |
|-------------|----------------|
| **0.8 – 1.0** | Near-universal relatability. The meme captures an experience almost everyone has lived through, recreates how it feels, and needs no explanation. |
| **0.5 – 0.8** | Broadly relatable. The meme connects with a wide audience, though it may lean on a somewhat specific experience or require light cultural familiarity. |
| **0.2 – 0.5** | Moderately relatable. The meme resonates with a sizable group but relies on experiences or references that a significant portion of people would not share. |
| **0.0 – 0.2** | Niche. The meme is rooted in a narrow subculture, specialized knowledge, or an obscure scenario that most people would not recognize or connect with emotionally. |

## What It Evaluates

The score is derived from three distinct dimensions, each capturing a different facet of what makes a meme relatable:

### 1. Universality of Experience

How broadly has the depicted scenario been lived? A meme about forgetting why you walked into a room or the dread of hearing your full name from a parent draws on moments that transcend age, culture, and background. A meme about a niche professional frustration or a specific fandom inside joke, no matter how clever, has a lower ceiling. This dimension asks: **how many people on earth have felt what this meme describes?**

### 2. Emotional Resonance

Does the meme go beyond *describing* a common experience to *recreating how it feels*? There is a difference between a meme that says "people procrastinate" and one that captures the specific guilt of watching hours evaporate while a deadline looms. Emotional resonance is the spark of recognition that transforms a viewer from a passive observer into someone who thinks, "This is so me." This dimension asks: **does the meme make you feel the feeling, or just acknowledge the situation?**

### 3. Accessibility

Can the meme be understood and felt without specialized knowledge? A meme about the exhaustion of small talk at parties is accessible to virtually anyone. A meme that requires familiarity with a particular video game mechanic or an obscure internet subculture has built a wall around its relatability. This dimension asks: **does the meme welcome everyone in, or does it require a key to enter?**

## Use Cases

- **Content creators** can gauge whether a meme will resonate broadly or only land within a narrow community before publishing.
- **Social media strategists** can prioritize high-relatability content in campaigns designed to maximize organic sharing, tagging, and reposting.
- **Platform algorithms** can use the score as a signal to surface content that drives genuine engagement rather than passive scrolling.
- **Cultural researchers** can track how relatability trends evolve over time — what felt universal a decade ago may feel dated today as new shared experiences emerge.
- **Brand teams** can filter meme-based marketing content to ensure it connects with the widest possible audience.

## Examples

**High score (~0.9):** A meme about setting an alarm, waking up before it goes off, and feeling personally betrayed. Nearly everyone has experienced this, the emotional frustration is immediately felt, and no context is needed.

**Medium score (~0.5):** A meme about the specific anxiety of presenting in a video call and not knowing if you're on mute. Many people relate, but it's tied to remote work — a broad but not universal experience.

**Low score (~0.15):** A meme referencing a specific interaction in a niche online game that only players of that game would understand. The experience is narrow, the emotional payoff is gated, and it requires insider knowledge to decode.

## Philosophy

Relatability is not a single trait but a convergence of three forces: the breadth of the experience being depicted, the depth of the emotional response it provokes, and the openness with which it communicates. The most relatable memes achieve something quietly remarkable — they make strangers feel less alone. That is what this function measures.