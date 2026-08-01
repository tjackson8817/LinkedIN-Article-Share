# LinkedIn Article Share Builder — User Guide

This tool is a single web page (`linkedin_article_share.html`) that finds the 5 most on-brand, recent articles worth sharing on LinkedIn, automatically ranks them, then drafts the post — and optionally the artwork — for whichever one you pick. Like the other tools in this family, it runs entirely in your browser: no install, no account, nothing sent anywhere until you copy the prompt and paste it into an AI chat yourself.

---

## Claude Settings You'll Need Before You Start

| Setting | Why you need it | Where to find it |
|---|---|---|
| **Web search** | Required — the entire tool depends on live search for real, current articles. | Click the **+** (or slider) icon in the chat input, find **Web search**, toggle it on. |
| **Code execution and file creation** | Only needed if **Generate artwork?** is set to Yes (the default). Without it, Claude can still draft the post text, but can't build the downloadable `.png`. | **Settings → Capabilities**, toggle it on. |

The tool works with any AI chat tool that can browse the web, not just Claude — but **artwork generation is Claude-specific.** ChatGPT and most other tools have no equivalent way to execute code and hand back a real downloadable file from a pasted prompt, so if you paste this into ChatGPT with artwork on, you'll get the text but no image, no matter how the prompt is worded.

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
| **Generate artwork?** | Yes | Produces a downloadable `.png` (1200×630) in the same visual identity used across this tool family. Only works when the prompt is run in Claude with Code execution and file creation enabled — the generated prompt explicitly instructs Claude to render it using Python's Pillow library and save a real file, and to say plainly if it can't rather than just describing a design that isn't a real file. |
| **Generate hashtags?** | Yes | 3–5 hashtags generated from the actual article content and your brand keywords — shown for **all 5 candidates in Step 1**, not just whichever one you end up picking, so you can factor likely hashtags into your choice. The same set carries through unchanged into the final Step 2 post. |
| **End the post with a question?** | **No** | Off by default, deliberately. A question at the end genuinely does drive more comments — but overusing it across every single post starts to read as engagement-bait rather than a real invitation to discuss. Turn it on when you specifically want to space one in, rather than leaving it on by default for every post. |

---

## 4. The Honesty Guardrails (Not Optional)

Same discipline as every other tool in this suite, adapted to what this one produces:

- **Only real, verifiable, currently findable articles with real URLs** — never an invented source.
- **A good-faith, honestly-flagged paywall check** — "Likely free," "Paywalled," or "Uncertain," not false confidence about something that can't be fully verified from outside.
- **If genuinely on-brand, recent, free-to-read articles are thin on a given day, the tool reports fewer than 5 and says so** rather than padding the list with weak or off-brand picks just to fill 5 slots.
- **The picks must be distinct stories** — not the same underlying event covered by multiple outlets. If near-duplicate coverage turns up, the tool is instructed to flag it and substitute a genuinely different story rather than quietly presenting several versions of the same news.
- **Every summary is written fresh, in Claude's own words** — never copied or lightly reworded from the source article.
- **No markdown formatting anywhere in the output.** LinkedIn doesn't render markdown — asterisks or pound signs would show up as literal stray characters in your post, so the generated prompt explicitly requires plain text throughout, not just in the final post.

---

## 5. How It Actually Runs — Two Steps

**Step 1**: the model automatically ranks candidates using five weighted criteria — keyword/topic match depth, recency, source credibility, likely shareability for your stated audience, and distinctiveness — and presents the **top 5 in ranked order**, best first, with a one-line explanation of the rank logic up front. Each candidate is shown in two parts:

- *Context* (for you to read): headline, source, published date/time, free-to-read assessment, and one line on why it ranked where it did.
- *Ready to copy* (exactly three lines, nothing else mixed in): `URL`, `Summary` (one LinkedIn-ready sentence), and `Hashtags` (if enabled) — formatted so you can select and paste just that block straight into a post without any cleanup.

**Step 2**: once you tell the model which of the 5 to use, it drafts the actual post in the same shape — `URL`, then `Post` (personal hook + summary combined into one tight paragraph, closing on a question or a statement depending on your toggle), then `Hashtags` (the same set already generated in Step 1, not regenerated).

If artwork is enabled, **Step 3** builds the matching image, following the exact visual template embedded in the generated prompt (colors, layout, and your brand identity fields), so every post's artwork stays visually consistent even though the headline, summary, and hashtags are different each time. This step only produces a real file in Claude with code execution enabled — anywhere else, the model is instructed to say so rather than pretend.

---

## 6. Output Format

- **The post text** — plain text directly in the chat response, in the `URL / Post / Hashtags` order, ready to copy straight into LinkedIn's post box. No file needed for this part.
- **The artwork** (if enabled, Claude only) — a real downloadable `.png` file, separate from the text, matching how LinkedIn posts actually work: paste the caption, then upload the image as its own attachment.

---

## 7. Typical Workflow, Start to Finish

1. Fill in your brand keywords and recency window.
2. Fill in your name/tagline once (first time only — reuse afterward).
3. Set your toggles (artwork, hashtags, closing question).
4. Copy the generated prompt, paste into a new Claude chat (with Web search, and Code execution and file creation if you want artwork).
5. Review the ranked top 5 candidates and the rank logic; pick one.
6. Review the drafted post and (if generated) the artwork before posting.

---

## 8. Quick Troubleshooting

| Problem | Fix |
|---|---|
| Prompt panel just shows placeholder text | You need at least Brand keywords/topics filled in. |
| No artwork came back | Confirm Code execution and file creation is enabled, and that you're in Claude — this step doesn't work in ChatGPT or other tools regardless of prompt wording. The prompt now explicitly directs Claude to render the image with Pillow and save a real file — if it still doesn't produce one, ask directly for it to save the .png to the outputs folder and confirm the file exists. |
| All 5 picks feel off-brand or repetitive | Narrow your brand keywords, or widen the recency window if genuinely on-brand coverage was thin that day. |
| Post has stray asterisks or pound signs when pasted into LinkedIn | This shouldn't happen given the no-markdown instruction — if it does, ask the model directly to strip any markdown formatting before you copy it. |
| In ChatGPT (or another tool), it responds with a plan/recommendations or asks questions instead of just running the task | The generated prompt now opens with an explicit "execute this now — don't ask clarifying questions, don't outline a plan" instruction specifically to head this off, along with permission to make and state reasonable assumptions instead of pausing. If it still happens, you can restate that instruction even more bluntly in your own words as a follow-up message. |
