**SALE FISH**

MARKETING AND CONSULTING

# LinkedIn Article Share Builder

*User Guide*

**Live Tool:** [https://tjackson8817.github.io/LinkedIN-Article-Share/linkedin_article_share.html](https://tjackson8817.github.io/LinkedIN-Article-Share/linkedin_article_share.html)

Created By: Tom Jackson
August 13, 2026

This tool is a single web page (linkedin_article_share.html) that finds the top 3 on-brand, recent articles worth sharing on LinkedIn, automatically ranks them, then drafts two genuinely different post options for each — an Informational Share and a Position/Stance take — plus optional matching artwork for whichever one you pick. Like the other tools in this family, it runs entirely in your browser: no install, no account, nothing sent anywhere until you copy the prompt and paste it into an AI chat yourself.

## Claude Settings You'll Need Before You Start

| Setting | Why you need it / Where to find it |
|---|---|
| Web search | Required — the entire tool depends on live search for real, current articles. |
| Code execution and file creation | Needed if artwork generation is on, or if you choose the downloadable Word document output format. |

The tool works with any AI chat tool that can browse the web — but artwork generation is Claude-specific. ChatGPT and most other tools have no equivalent way to execute code and hand back a real downloadable file from a pasted prompt, so pasting this into ChatGPT with artwork on will produce text but no image, regardless of wording.

## A Different Shape Than the Other Tools

This is the sixth tool in the family, but it doesn't sit in the job-search funnel the way the first five do — it's for staying visible on LinkedIn and building an actual thought-leadership position, whether or not you're job hunting at all.

## 1. What Counts as "On-Brand"

| Field | What it does |
|---|---|
| Brand keywords/topics | Required. Makes "impactful" specific to your niche rather than generic trending news. |
| How recent? | Last 24h / 48h / 3 days (default) / 1 week. |
| Who's this for? | Optional. Shapes which angle counts as most impactful — a recruiter-facing post and a client-facing post can reasonably favor different picks from the same pool. |
| Sources to prioritize or avoid | Optional. |
| Already covered recently | Optional — avoids repeating a topic you already posted about. |
| Ongoing themes you're building a position on | Optional. Thought leadership compounds across posts that connect to a few recognizable throughlines, not one-off reactions. Also feeds the hashtags on the Position/Stance variant, so they help build a consistent community of interest around you rather than just tagging each article in isolation. |

## 2. Your Brand Identity

**Your name**, **your tagline**, and an optional **eyebrow line** feed the artwork and post signature. **Your background/expertise** (optional) is what grounds the Position/Stance variant in something real — paste your resume, LinkedIn About section, a short bio, or just a few sentences on your actual experience. Without it, that variant stays more general and analytical rather than inventing a personal claim or credential you didn't give it.

**These fields are not remembered automatically** — closing the tab clears them, exactly like every other field on the page. Use **Save brand identity (.json)** to download a small file with your name/tagline/eyebrow/background/themes, and **Load brand identity** to read one back in next time, instead of retyping. Keep the downloaded file somewhere you'll find it again — the tool has no way to remind you where you saved it.

## 3. Options

| Toggle | Default | What it does |
|---|---|---|
| Generate hashtags? | Yes | 3-5 hashtags per variant. On the Informational variant, drawn from the article's content and your brand keywords. On the Position/Stance variant, drawn from **both the article and your background/themes**, deliberately — the goal is hashtags that build a recognizable community of interest around your actual expertise over time, not just tags for one article in isolation. |
| Generate artwork for whichever I end up choosing? | Yes | A downloadable `.png` (1200×630), generated as a separate follow-up step scoped to just the one post you pick — not all 6 drafts upfront. Claude only, requires Code execution and file creation. |
| Output format | Table in chat | The alternative, Downloadable Word document, lays out all 3 articles × 2 variants for offline comparison before you pick. |

There's no longer a standalone "end with a question?" toggle. That judgment is now made per-take inside the Position/Stance variant itself — the model decides, for that specific point of view, whether a genuine question or a strong statement is the more effective close, rather than a single global setting applied to every post regardless of content.

## 4. The Honesty Guardrails (Not Optional)

- Only real, verifiable, currently findable articles with real URLs — never an invented source.
- A good-faith, honestly-flagged paywall check — "Likely free," "Paywalled," or "Uncertain."
- If genuinely on-brand, recent, free-to-read articles are thin on a given day, the tool reports fewer than 3 and says so rather than padding the list.
- The 3 picks must be distinct stories, not the same underlying event covered by multiple outlets.
- Every summary is written fresh, in the model's own words — never copied or lightly reworded from the source.
- No markdown formatting anywhere in the output — LinkedIn doesn't render it.
- **The Position/Stance variant never invents anything about you.** It leans on real background/themes if you gave them, and stays general if you didn't — but it never fabricates a claim, credential, or experience either way. This matters more here than in a one-off message: a fabricated personal anecdote in a public LinkedIn post is a much bigger problem than one in a private draft, since it's out there under your name.

## 5. How It Actually Runs — One Response, Then a Follow-Up

**Step 1** (everything below happens in one response): the model ranks candidates automatically using five weighted criteria — keyword/topic match depth, recency, source credibility, likely shareability for your stated audience, and distinctiveness — and narrows to the **top 3**, stating the rank logic in one line up front.

For each of the 3, you get:

- **Context** (to read, not copy): headline, source, published date, free-to-read assessment, why it ranked here.
- **Variant A — Informational Share:** URL, then a short factual summary — typically one sentence, never more than two — with little to no personal commentary. The safe, high-frequency default. Ends on a statement.
- **Variant B — Position/Stance:** URL, then a real take grounded in your background/themes (agree, disagree, extend the argument, connect it to a pattern, make a prediction), with the article's core point folded in tightly rather than presented as a separate summary. Closes on a genuine question or a strong statement, whichever the model judges is the stronger move for that specific take.

That's 6 fully drafted posts in one response — not 3 teasers waiting for you to request the actual draft.

**Follow-up, once you've picked one:** if artwork is enabled, tell the model which of the 6 you're using, and it builds the matching image for that post specifically, following the exact visual template embedded in the prompt (colors, layout, your brand identity fields). This step only produces a real file in Claude with code execution enabled.

## 6. Output Format

- **Table in chat** (default) — all 3 articles and 6 drafts presented directly in the response.
- **Downloadable Word document** — the same content, laid out for offline comparison: one section per article, Variant A then Variant B, clearly labeled.
- **The artwork** (if enabled) — always a separate, real downloadable `.png`, regardless of which format you chose for the text.

## 7. Typical Workflow, Start to Finish

1. Fill in your brand keywords and recency window.
2. Fill in your brand identity — or load a previously saved one.
3. Optionally add your background/expertise and ongoing themes.
4. Set your toggles — hashtags, artwork, output format.
5. Copy the generated prompt, paste it into a new Claude chat.
6. Review all 6 drafts (3 articles × 2 variants); pick your favorite.
7. If artwork is on, tell the model which one you're using and review the image before posting.
8. Before closing the tab, use Save brand identity if you changed anything you want to keep.

## 8. Quick Troubleshooting

| Problem | Fix |
|---|---|
| Prompt panel shows placeholder text | Fill in Brand keywords/topics. |
| No artwork came back | Confirm Code execution and file creation is enabled and you're in Claude — this doesn't work in ChatGPT regardless of wording. Artwork is a follow-up step; make sure you actually told the model which of the 6 drafts to build it for. |
| My saved brand identity won't load | Confirm it's a `.json` file actually downloaded from this tool's Save button — the Load button expects that exact format and will show an error rather than silently failing on anything else. |
| Position/Stance variant feels generic | Check whether you filled in Background/expertise — without it, that variant intentionally stays general rather than inventing a personal claim. |
| Picks feel off-brand or repetitive | Narrow your brand keywords, or widen the recency window if genuinely on-brand coverage was thin that day. |
| Stray formatting characters in a post | Ask the model directly to strip any markdown before you copy it. |
| In ChatGPT (or another tool), it responds with a plan or asks questions instead of running the task | The prompt opens with an explicit "execute this now" instruction to head this off — restate it more bluntly as a follow-up if it still happens. |
