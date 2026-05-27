# Post-Mortem — Today's Stock (Project 3)

> AI 201 submission. What worked, what didn't, what I'd do differently.
> ⚠️ Sections marked [ ] are for Kelly to fill in directly.

---

## What Worked

**1 — Mom actually opened the GPT and used it**

Choosing the platform she was already on was the right call. No new app, no new login, no friction. In First Contact, mom accessed the GPT independently and entered questions. The feedback she gave wasn't "I don't know how to use this" — it was "I asked but it just told me to decide on my own?" That's the feedback of someone who knows how to use the tool. The platform barrier was zero.

**2 — Mom's problem was diagnosed accurately**

The interviews and First Contact confirmed Findings A, B, C, and D in the field. Finding B in particular — the central design conflict (what mom wants most = what the GPT legally cannot give her) — turned out to be the most important tension in the project, and v1.2's "refuse + redirect" structure was a direct response to it.

**3 — Records of Resistance led to real product decisions**

Every time I pushed back on AI's suggestions, there was a better reason to — and each rejection led to a concrete improvement. Rejecting the all-in-one GPT connected directly to the project thesis. Rejecting "recommended stocks" framing kept the GPT on the right side of a legal line.

**4 — Mom's behavior shifted in a way that was observable**

Watching mom shift from one-way commands ("translate this") to natural back-and-forth conversations with the GPT felt like the clearest sign it was working. She started asking follow-up questions on her own — without anyone telling her to. By the second test, she called it "like a briefing secretary" and used it for an actual purchase decision. That change in behavior was more meaningful than any feature working correctly.

---

## What Didn't Work

**1 — v1.1's refusal structure recreated the flight incident**

The original reason mom stopped using ChatGPT for stocks was the "flight incident" — she asked for the cheapest flight and got told to find it herself. In First Contact, v1.1 produced the exact same pattern. "Investment decisions are yours to make" was legally correct and ethically right, but functionally useless. It took actually putting the prototype in front of mom to see it.

**2 — The thesis took too long to stabilize**

The thesis went through six evolutions — KakaoTalk digest, bot, invisible AI layer, single all-in-one GPT, unified mom GPT, and finally a topic-specific GPT family with Today's Stock as the first instance. That much iteration on the core idea put the project about a week behind schedule, which compressed everything that came after.

**3 — A third iteration round wasn't possible**

The ideal loop is: First Contact → iteration → second test → third iteration. The core loop closed — mom tested v1.2 on a real purchase she had just made — but there wasn't time to address her follow-up requests (price bands, hold/sell guidance during drops). Those requests are still in the legally prohibited zone, so the design tension remains unresolved at the feature level.

---

## What I'd Do Differently

**1 — First Contact earlier**

Even a rougher version of the prototype — earlier. The most useful data came from putting it in front of mom, not from building in isolation. Telling her "this is rough, it might break" and handing it over earlier would have left more iteration time.

**2 — Capture exact quotes from the start**

Several of mom's quotes in the research documentation are paraphrased. Exact wording is what scores points in Research Documentation. From the first interview, I should have written down her words verbatim, not my interpretation of what she meant.

**3 — Designing for a real person vs. a hypothetical user**

Designing for mom meant building with the assumption that she can't write good prompts — and that the tool has to work without her needing to. With a hypothetical user, you can write "assumes basic AI familiarity" and move on. With mom, that assumption would have broken everything. Every design decision ran through the same filter: does this add friction? Does this require her to learn something new? The goal was to remove as much complexity and burden as possible on her end, so the tool could do the heavy lifting that she couldn't ask it to do herself.

---

## The One-Sentence Takeaway

> "Set up the tool for the task, and the person will use it. Mom was already proving that at the doctor's office."
