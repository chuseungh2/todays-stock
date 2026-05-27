# AI Direction Log — Today's Stock (Project 3)

> AI 201 submission. What I asked AI to do, what it produced, what I changed / rejected / kept, and why.
> 7 entries total.

---

## Entry 1 — Rejected platform suggestion: Gemini/Claude → stayed with ChatGPT

**What I asked AI:** Review platform options for a stock information tool for my mom

**What AI gave me:** A suggestion that Gemini and Claude offer similar capabilities to Custom GPT and might be more flexible

**Decision:** Kept ChatGPT Custom GPT

**Why:** The feature comparison was accurate, but it missed the point. Mom is already using ChatGPT for doctor visits. "Zero new apps, zero new logins, zero new learning" isn't a feature spec — it comes from knowing the user. The best tool is the one she'll actually open.

---

## Entry 2 — Rejected all-in-one GPT → rebuilt as topic-specific GPT family

**What I asked AI:** Design a GPT structure for my mom

**What AI gave me:** An all-in-one "Mom GPT" that would handle stocks, travel, health, and other topics in a single GPT

**Decision:** Rejected. Rebuilt as a topic-specific GPT family. Today's Stock ("오늘의 주식") is the first instance.

**Why:** A single GPT for everything sounds clean in theory, but creates confusion in practice. Stock questions and travel questions use completely different vocabulary and expectations. For a user whose needs vary sharply by task, the tools should too. This connects directly to the project thesis.

---

## Entry 3 — Rejected "recommended stocks" starter → rebuilt as "trending stocks" (informational framing)

**What I asked AI:** Write 4 conversation starters for the GPT

**What AI gave me:** A starter along the lines of "What stocks are worth paying attention to right now?" — implying a recommendation

**Decision:** Rejected. Replaced with "What stocks are people talking about lately?"

**Why:** "Worth paying attention to" implies a recommendation. Under Korean financial law, that could constitute unlicensed investment advice — which the GPT's absolute rules prohibit. Same information, different framing. One word can cross a legal line.

---

## Entry 4 — Redirected system prompt v1.1 fix → rebuilt refusal structure from scratch

**What I asked AI:** Revise the system prompt based on First Contact feedback from mom

**What AI gave me:** Softened refusal language — same structure, more polite wording

**Decision:** Changed direction entirely. Not softer refusals — a new structure where every refusal is immediately followed by judgment material (refuse + redirect).

**Why:** Mom's feedback — "I asked but it just told me to decide on my own?" — wasn't a tone problem. The refusal itself wasn't the issue. The problem was that she left empty-handed. AI suggested fixing the wording. The real fix was structural. To avoid recreating the "flight incident" (why she gave up on ChatGPT for stocks in the first place), the refusal and the answer had to happen simultaneously.

---

## Entry 5 — Rejected voice mode suggestion → locked in chat interface

**What I asked AI:** Review feature settings and interface options

**What AI gave me:** A suggestion that voice search / voice mode might be more natural for users in their 50s than typing

**Decision:** Rejected. Chat only.

**Why:** This was a generalization about 50-somethings. Mom explicitly said "chat is more comfortable" and has never used voice mode. User interview data beats demographic assumptions every time.

---

## Entry 6 — Rejected report-style answer structure → rebuilt as judgment-oriented response format

**What I asked AI:** Structure answers for judgment questions like "How's the market today?" or "Should I get into Samsung?"

**What AI gave me:** A standard stock analysis report format (background → current situation → outlook)

**Decision:** Rebuilt. New structure: one-line summary → 2–3 bullish reasons → 2–3 bearish reasons → signals to check (U.S. market / foreign investor flow / exchange rate / earnings / recent run-up or correction) → watch / wait / caution conditions

**Why:** Report format is how analysts write. Mom isn't an analyst — she needs a quick sense of how to read today. AI's structure had more information; mine was faster to act on.

---

## Entry 7 — Rejected Knowledge File upload → embedded holdings directly in system prompt

**What I asked AI:** How and where to store mom's stock holdings information

**What AI gave me:** Upload holdings as a separate Knowledge File

**Decision:** Rejected. Embedded directly as a `# Holdings` section in the system prompt as plain text.

**Why:** Knowledge Files use search-based retrieval. For a simple list of 4 stocks, that's overengineering. Direct embedding is more reliable and lets the GPT instantly recognize "my stocks" as a trigger phrase. Sometimes simple is correct — that's also an editorial call.
