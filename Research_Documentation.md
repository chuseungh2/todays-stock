# Research Documentation — Today's Stock (Project 3)

> Last updated: 2026-05-27 (post-Second Test feedback incorporated)

---

## 1. The Person

- **Mom** — Korean woman in her 50s, living in Korea, Korean-speaking
- Has access to ChatGPT through dad's company benefit (ChatGPT Plus)
- **Important:** Mom is not someone who "can't use AI." She uses ChatGPT for basic, bounded tasks — like asking how to explain her symptoms in English at the doctor's office (a successful use case). But anything more complex than simple translation or unit conversion — stock analysis, finding flights, open-ended research — she struggled with. The task complexity, not the person, is what determined whether she succeeded.

---

## 2. Direct Quotes

> *Scoring note: "The person's actual words. More valuable than your interpretation." Preserve awkward phrasing as-is.*

- *(1st interview)* Mom asked ChatGPT to "find me the cheapest flight" → ChatGPT essentially told her to find it herself → she gave up
- *(Re-interview, paraphrased — exact wording to be confirmed):*
  - "I don't know if it's a low point, when to sell... buy and sell signals are always confusing to me"
  - "Stocks are hard. You have to study all day — reading reports and everything"
  - "There's just too much news"
- *(First Contact feedback, 2026-05-25 — verbatim):*
  - "I asked but it just told me to decide on my own?"
  - "What I want: 1. Look at the U.S. market from the night before and predict the direction of the Korean stock market today"
  - "2. Decide buy/sell boundaries"
- *(Second test feedback, 2026-05-27 — verbatim, via KakaoTalk):*
  - "응 아직은 좀 광범위하지만 그래도 좀더 상세해진거 같아" *(Yes, it's still a bit broad, but it feels more detailed than before)*
  - "이렇게 보여주니까 일일이 찾지 않아도 되고 브리핑해주는 비서처럼 아주 좋아. 글고 한국 시장을 미리 예측 할수 있게 되어 좋아" *(It's like having a briefing secretary — I don't have to search one by one anymore)*
  - "저번보다 좀더 외국인 수급동향과 프로그램 매매등 추정해서 알려주어 투자결정에 좀더 유리해졌어" *(Better than last time — more info on foreign flows and program trading)*

---

## 3. Environment & Behavior

**Stock information sources:**
- YouTube channels: 하보노의 주식 이야기, 페이버, 체슬리의 모닝 브리핑, 연합인포맥스
- News
- Telegram — channels that curate and compile news summaries

**Areas of interest:** Semiconductors, AI, biotech — more sector/theme-focused than individual stock names

**Investment mental model (mom's own strategy):** "Korean stocks follow U.S. stocks. So you have to follow the U.S. market."

**Format preference:** No strong preference for tables vs. prose vs. emoji. But "organized and readable" is a requirement — readability is a need, format is flexible.

**Tone preference:** Warm and conversational

**Interface:** Prefers chat. Has never used voice search or voice mode (stated explicitly).

---

## 4. Workarounds (What the System Should Replace)

- Manually gathering stock information by watching multiple YouTube videos + reading news + following Telegram digest channels
- "Studying all day" + reading reports to bridge the information gap
- For the hospital: using ChatGPT to translate symptoms to English — *this is a successful use case, not a workaround* (design signal)
- [TODO] Specific examples of how mom handles English financial terms when she encounters them

---

## 5. Constraints (Design Conditions)

- **Interface:** Mom explicitly said "chat is more comfortable" → voice mode excluded from core interface
- **English vocabulary barrier:** Reports and news in English are a wall
- **Legal constraint (core design issue):** Buy/sell/timing recommendations = unlicensed investment advice under Korean financial law → GPT cannot make recommendations under any framing
- **Cost:** $0 permanently (using dad's company ChatGPT Plus)
- **Access:** Requires login to dad's ChatGPT Plus account

---

## 6. Key Findings — 4 Major Insights

### Finding A — Mom is not someone who "can't use AI"
Mom uses ChatGPT regularly and successfully for hospital visits. She only failed with stocks.
→ The difference is not Mom — it's the type of task. Hospital = bounded, single task (explain this symptom in English). Stocks = open-ended, judgment-required task.
→ **Strengthens thesis:** If the tool is set up for the task, Mom will use it. Already proven.

### Finding B — What Mom wants most = what we can't give her (Central Design Conflict)
Mom's #1 pain = "when to buy and when to sell" (buy/sell signal confusion).
Our #1 rule = absolutely no buy/sell recommendations (legal).
→ Direct conflict. This is the central design problem of the project.
→ **Resolution direction:** The GPT doesn't make the decision for her. Instead, it lowers the cost of making the decision — explaining signals, translating English, summarizing both bullish and bearish cases, compressing the news flood.
→ **Key risk:** If it only refuses, it recreates the "flight incident." Must always refuse + immediately redirect to judgment material. Never send her away empty-handed.

### Finding C — Chat, not voice
The original Platform Rationale listed "voice mode" as a key advantage, but Mom explicitly said "chat is more comfortable" and has never used voice mode.
→ Voice argument dropped. New primary reason: "Mom is already using ChatGPT — zero new apps, zero new logins, zero new learning. We're just putting a stock GPT inside the ChatGPT she already uses."

### Finding D — "Make the investment decision yourself" is not enough
In First Contact, when the GPT responded with "investment decisions are yours to make," it was legally and ethically correct — but didn't feel like actual help to Mom. What she wanted wasn't direct buy/sell orders. She wanted:
① A way to interpret the previous day's U.S. market in terms of today's Korean market direction
② Conditions and boundaries for making buy/sell judgments
→ v1.2 fix: Don't substitute the decision, but always provide the conditions for judgment.
→ New response structure: One-line summary → bullish/bearish cases → U.S. market connection → signals to check → watch/wait/caution conditions.

---

## 7. Evidence Status
- ✅ Verbatim quotes: First Contact feedback + Second test KakaoTalk messages
- ✅ Environment photo: Mom using GPT on her phone (with permission)
- ✅ Holdings confirmed: Samsung Electronics, SK Hynix, Nvidia, Tesla
- ✅ Real-world use confirmed: Mom used GPT for actual purchase decision (LG이노텍, ₩920,000)
- ⚠️ Re-interview paraphrased quotes (Section 2) — exact wording not confirmed
