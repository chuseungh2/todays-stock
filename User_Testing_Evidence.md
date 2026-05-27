# User Testing Evidence — Today's Stock (Project 3)

> AI 201 submission. Documented evidence of a real person using the prototype.
> Test sessions, observations, direct quotes, and iteration record.

---

## Test 1 — First Contact

**Tester:** Mom (Korean woman in her 50s, primary user)

**Prototype tested:** Today's Stock Custom GPT v1.1

**How:** Mom opened the GPT directly on her device and typed in questions. Kelly observed.

**Setup:** Dad's ChatGPT Plus account, accessed on mom's device

---

### Observed Behavior

Mom opened the prototype independently and entered stock-related questions.
The GPT responded with: "Investment decisions are yours to make."
Mom did not ask a follow-up question.

---

### Direct Quotes (First Contact feedback — verbatim, as received)

> "I asked but it just told me to decide on my own?"

> "What I want: 1. Look at the U.S. market from the night before and predict the direction of the Korean stock market today"

> "2. Decide buy/sell boundaries"

*(These quotes are mom's exact words as sent in text)*

---

### What Worked / What Failed / What Was Surprising

**Failed:** The v1.1 refusal structure recreated the "flight incident" — the same reason mom gave up on ChatGPT for stocks in the first place. "Investment decisions are yours to make" was legally correct but didn't feel like actual help. She left empty-handed.

**Worked:** Mom accessed the GPT independently and entered a question. The platform barrier was zero — she already knows how to use ChatGPT.

**Surprising:** Mom didn't want a direct "buy this" command. She wanted:
① A way to read the previous night's U.S. market in terms of today's Korean market direction
② Conditions for making buy/sell boundary decisions

Both of those are information requests — not recommendations. They're within what the GPT can provide.

---

### Iteration: v1.1 → v1.2

Based on First Contact feedback, the system prompt was updated.

**What changed:**
- Removed: refuse-only response structure
- Added: refuse + immediately provide judgment material (the "never send her away empty-handed" rule, made explicit)
- Added: judgment-oriented answer structure — one-line summary → bullish/bearish cases → U.S. market connection → signals to check → watch/wait/caution conditions
- Mom's want ① ("U.S. market → Korean market direction") → translated into a morning context brief (not a prediction — a contextualization)
- Mom's want ② ("buy/sell boundaries") → addressed through conditional frameworks, not specific price calls

**Conversation starters also updated:**
- v1.1: Generic stock information starters
- v1.2: "Walk me through last night's U.S. market and what it might mean for Korean stocks today" / "Just give me the decision framework for whether to enter Samsung right now" — directly reflecting what mom said she actually wanted

---

---

## Test 2 — Second Test

**Tester:** Mom

**Prototype tested:** Today's Stock Custom GPT v1.2

**How:** Mom used the GPT independently for a real stock she had just purchased (LG Innotek / LG이노텍, bought at ₩920,000). Kelly observed via KakaoTalk exchange.

---

### Observed Behavior

Mom ran an actual analysis on LG이노텍 through the GPT. The GPT returned a detailed response including: conditional responses by scenario, judgment criteria (U.S. tech sentiment, foreign investor flow, exchange rate, earnings/iPhone sales news), a one-line conclusion, and bullish/bearish reasons. Mom then sent additional feature requests over KakaoTalk — showing she was engaged enough to want more, not giving up.

---

### Direct Quotes (verbatim, as received via KakaoTalk)

> "응 아직은 좀 광범위하지만 그래도 좀더 상세해진거 같아"
> *(Yes, it's still a bit broad, but it feels more detailed than before)*

> "이렇게 보여주니까 일일이 찾지 않아도 되고 브리핑해주는 비서처럼 아주 좋아. 글고 한국 시장을 미리 예측 할수 있게 되어 좋아"
> *(Showing it like this means I don't have to search one by one — it's like having a briefing secretary. And it's good that I can get a read on the Korean market in advance)*

> "저번보다 좀더 외국인 수급동향과 프로그램 매매등 추정해서 알려주어 투자결정에 좀더 유리해졌어"
> *(Compared to last time, it gives more information on foreign investor flows and program trading — that makes investment decisions easier)*

**Mom's additional requests (still wants):**
> "단기급등시 수급에 따른 매매 결정을 할 수 있는 가격밴드를 어느정도 알려겼으면 해"
> *(I'd like it to give me a price band for making buy/sell decisions based on supply/demand during short-term spikes)*

> "아니면 단기하락이 있을경우 이유와 홀딩인지 아니면 단기 차액실현을 해야하는지 알려겼으면 해"
> *(Or when there's a short-term drop, I'd like to know the reason and whether to hold or realize short-term gains)*

*Note: Both additional requests are still in the legally prohibited zone (direct buy/sell guidance). The redirect structure in v1.2 is handling this correctly — but mom continues to want more decisive direction, which confirms the central design conflict documented in Finding B.*

---

### What Worked / What Changed from Test 1

**Clear improvement:** Mom used the phrase "브리핑해주는 비서처럼" (like a briefing secretary) — the exact outcome the GPT was designed to create. She no longer has to search across multiple sources.

**Real-world use:** Mom ran the analysis on a stock she had actually just purchased at ₩920,000. This was not a test scenario — she used the GPT as part of a real investment decision.

**Engagement:** Instead of walking away after one response (as in Test 1), mom sent multiple follow-up messages with feature requests. That shift in behavior — from "I asked but it told me to decide on my own" to "I want more of this" — is the clearest evidence of improvement.

**Still unresolved:** Mom's continued requests for price bands and hold/sell guidance confirm the central design tension hasn't disappeared. The GPT is handling it better (redirect instead of bare refusal), but the gap between what mom wants and what the tool can legally give remains the core challenge of this product.

---

## Environment Photo

✅ Photo obtained (with permission): Mom's hand holding her phone showing the GPT response to "가격밴드결정해줘" — the v1.2 refuse + redirect structure visible on screen.

*File: `mom_using_gpt.jpg` — include in repo*
