# LinkedIn Article Share Builder — User Guide

This tool is a single web page (`linkedin_article_share.html`) that finds the 3 most on-brand, recent articles worth sharing on LinkedIn, then drafts the post — and optionally the artwork — for whichever one you pick. Like the other tools in this family, it runs entirely in your browser: no install, no account, nothing sent anywhere until you copy the prompt and paste it into a Claude chat yourself.

---

## Claude Settings You'll Need Before You Start

| Setting | Why you need it | Where to find it |
|---|---|---|
| **Web search** | Required — the entire tool depends on live search for real, current articles. | Click the **+** (or slider) icon in the chat input, find **Web search**, toggle it on. |
| **Code execution and file creation** | Only needed if **Generate artwork?** is set to Yes (the default). Without it, Claude can still draft the post text, but can't build the downloadable `.png`. | **Settings → Capabilities**, toggle it on. |

---

## A Different Shape Than the Other Four Tools

This is the fifth tool in the family, but it doesn't sit in the job-search funnel the way the other four do — it's for staying visible on LinkedIn between job-search activity (or just as an ongoing personal-brand tool, whether or not you're job hunting at all). Useful on its own, independent of whether you're using any of the other four tools.

---

## 1. What Counts as "On-Brand"

| Field | What it does |
|---|---|
| **Brand keywords/topics** | Required. This is what makes "impactful" mean something specific to your niche rather than generic trending news — be as specific as your actual focus area. |
| **How recent?** | Last 24 hours / 48 hours / 3 days (default) / 1 week — a hard filter on how fresh the candidates need to be. |
| **Who's this for?** | Optional. Shapes which angle counts as most impactful — a recruiter-facing post and a client-facing post can reasonably favor different picks from the same pool of articles. |
| **Sources to prioritize or avoid** | Optional. If you know your Google Alerts/Feedly feeds skew toward certain publications, or want to steer away from low-quality aggregator sites specifically. |
| **Already covered recently** | Optional. Paste in URLs or topics from your last few posts so this run doesn't hand you something you already shared. |

---

## 2. Your Brand Identity (Set Once, Reused Every Time)

Three fields — **Your name**, **Your tagline**, and an optional **Eyebrow line** — work differently from everything else in the tool. These represent your consistent personal brand and shouldn't need retyping for every single post, the same way "Your background" works as a reusable field across the other tools in this family. Fill them in once; they carry through to the artwork every time you use the tool.

---

## 3. Options

| Toggle | Default | What it does |
|---|---|---|
| **Generate artwork?** | Yes | Produces a downloadable `.png` (1200×630) in the same visual identity used across this tool family — dark navy background, teal/blue accents, your name and tagline in the footer. |
| **Generate hashtags?** | Yes | 3–5 hashtags generated from the actual article content and your brand keywords — not generic tags, ones tied to what the specific article is about. |
| **End the post with a question?** | **No** | Off by default, deliberately. A question at the end genuinely does drive more comments — but overusing it across every single post starts to read as engagement-bait rather than a real invitation to discuss. Turn it on when you specifically want to space one in, rather than leaving it on by default for every post. |

---

## 4. The Honesty Guardrails (Not Optional)

Same discipline as every other tool in this suite, adapted to what this one produces:

- **Only real, verifiable, currently findable articles with real URLs** — never an invented source.
- **A good-faith, honestly-flagged paywall check** — "Likely free," "Paywalled," or "Uncertain," not false confidence about something that can't be fully verified from outside.
- **If genuinely on-brand, recent, free-to-read articles are thin on a given day, the tool says so** rather than padding the list with weak or off-brand picks just to fill 3 slots.
- **The 3 picks must be 3 distinct stories** — not the same underlying event covered by three different outlets. If near-duplicate coverage turns up, the tool is instructed to flag it and substitute a genuinely different story rather than quietly presenting three versions of the same news.
- **Every summary is written fresh, in Claude's own words** — never copied or lightly reworded from the source article.
- **No markdown formatting in the final post text.** LinkedIn doesn't render markdown — asterisks or pound signs would show up as literal stray characters in your post, so the generated prompt explicitly requires plain text.

---

## 5. How It Actually Runs — Two Steps

1. **Step 1**: Claude presents the top 3 candidates — headline, source, published date/time, URL, a free-to-read assessment, and one line of reasoning for why each made the cut for your brand and audience.
2. **Step 2**: once you tell Claude which of the 3 to use, it drafts the actual post — URL, personal hook, summary, hashtags (if on), and either a closing question (if on) or a plain closing statement.

If artwork is enabled, **Step 3** builds the matching image, following the exact visual template embedded in the generated prompt (colors, layout, and your brand identity fields), so every post's artwork stays visually consistent even though the headline, summary, and hashtags are different each time.

---

## 6. Output Format

- **The post text** — plain text directly in the chat response, ready to copy straight into LinkedIn's post box. No file needed for this part.
- **The artwork** (if enabled) — a real downloadable `.png` file, separate from the text, matching how LinkedIn posts actually work: paste the caption, then upload the image as its own attachment.

---

## 7. Typical Workflow, Start to Finish

1. Fill in your brand keywords and recency window.
2. Fill in your name/tagline once (first time only — reuse afterward).
3. Set your toggles (artwork, hashtags, closing question).
4. Copy the generated prompt, paste into a new Claude chat.
5. Review the top 3 candidates and their reasoning; pick one.
6. Review the drafted post and (if generated) the artwork before posting.

---

## 8. Quick Troubleshooting

| Problem | Fix |
|---|---|
| Prompt panel just shows placeholder text | You need at least Brand keywords/topics filled in. |
| No artwork came back | Confirm Code execution and file creation is enabled — without it, Claude can only produce the text. |
| All 3 picks feel off-brand or repetitive | Narrow your brand keywords, or widen the recency window if genuinely on-brand coverage was thin that day. |
| Post has stray asterisks or pound signs when pasted into LinkedIn | This shouldn't happen given the no-markdown instruction — if it does, ask Claude directly to strip any markdown formatting before you copy it. |
