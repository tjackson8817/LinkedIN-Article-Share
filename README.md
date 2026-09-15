# LinkedIn Article Share Builder

A single self-contained HTML tool that finds the top 3 on-brand, recent articles worth sharing on LinkedIn, automatically ranks them, then drafts **two genuinely different post options for each** — an Informational Share and a Position/Stance take — so you're choosing between real options, not approving one draft. Optional matching artwork for whichever one you pick.

**[Open the live tool](https://tjackson8817.github.io/LinkedIN-Article-Share/linkedin_article_share.html)**

No install, no account, nothing sent anywhere — it's a static form that assembles text entirely in your browser.

## A different shape than the other five tools

This is the sixth tool alongside the five-tool job-search funnel (Target Company Prompt Builder, Job Posting Finder, Resume & Cover Letter Tailoring, Outreach Message Builder, Interview Prep Guide Builder, Salary Negotiator) and the Recruiter Message & Job Posting Sanity Check — but it isn't a funnel step. It's for staying visible on LinkedIn and building an actual thought-leadership position, whether or not you're job hunting at all.

## What changed in this rebuild

If you used an earlier version: the shape of the output changed meaningfully, not just the wording.

- **Two variants per article, not one.** Every article now gets an Informational Share (short, factual, low-key) and a Position/Stance take (your real point of view, grounded in your background) — you pick which one to post, per article, per mood.
- **Top 3 articles, not 5.** 5 articles × 2 variants would be 10 full drafts to review — too much. 3 × 2 = 6 is actually reviewable in one pass.
- **New: Your background/expertise field.** Grounds the Position/Stance variant in something real instead of generic commentary or — worse — an invented personal claim.
- **New: Ongoing themes field.** Thought leadership compounds across posts connected to a few recognizable throughlines, not one-off reactions.
- **Removed the false "set once, reused every time" promise.** Your brand identity fields were never actually persisted — closing the tab cleared them, exactly like every other field. Replaced with a real **Save/Load brand identity** file (a small `.json` you keep and reload), which actually does what the old label claimed.
- **Removed the standalone "end with a question?" toggle** — folded into the Position/Stance variant's own judgment instead (it decides, per take, whether a question or a statement is the stronger close, rather than a global on/off switch).
- **Artwork moved to a separate follow-up step**, scoped to just the one post you actually pick, not generated for all 6 drafts upfront.
- Fixed a stale reference in the honesty-guardrail copy that mismatched the actual candidate count, and added mobile responsiveness and proper label accessibility, matching the rest of this tool family.

## Claude Settings You'll Need Before You Start

| Setting | Why you need it | Where to find it |
|---|---|---|
| **Web search** | Required — the entire tool depends on live search for real, current articles. | Click the **+** (or slider) icon in the chat input, find **Web search**, toggle it on. |
| **Code execution and file creation** | Always needed — Step 1's text always comes back as a downloadable Word document, and artwork generation (if used) needs it too. | **Settings → Capabilities**, toggle it on. |

The tool works with any AI chat tool that can browse the web — but **artwork generation is Claude-specific.** ChatGPT and most other tools have no equivalent way to execute code and hand back a real downloadable file from a pasted prompt.

## Quick start

1. Open `linkedin_article_share.html`.
2. Fill in your brand keywords and recency window.
3. Fill in your name/tagline/eyebrow, and optionally your background and ongoing themes — or load a previously saved brand identity file.
4. Set your toggles — hashtags, artwork.
5. Copy the generated prompt and paste it into a new Claude chat.
6. Review all 3 articles × 2 variants (6 drafts), pick your favorite, and request artwork for it if you want it.

## The honesty guardrails

Only real, verifiable, currently findable articles with real URLs — never an invented source. A good-faith paywall check, honestly flagged. If genuinely on-brand articles are thin on a given day, the tool reports fewer than 3 and says so. Picks must be distinct stories, not the same event from multiple outlets. Every summary is written fresh, never copied from the source. No markdown formatting, since LinkedIn doesn't render it. **The Position/Stance variant only draws on background/themes you actually gave it** — with nothing given, it stays general commentary rather than inventing a personal claim or credential.

## Files in this repo

| File | What it is |
|---|---|
| `linkedin_article_share.html` | The interactive tool. |
| `LinkedIn_Article_Share_User_Guide.md` / `.docx` | Full usage guide, same content, two formats. |
| `sample_prompt.txt` | A real example of the generated prompt, produced by the actual tool code. |
| `Example_LinkedIn_Posts.docx` | A real, currently-live article found via live search, with both variants drafted to show the tool's intended output shape. See the note on its first page for exactly what's real vs. illustrative in that document. |

## Notes

- This repo can be public or private — GitHub Pages on the free tier requires a public repo (or a paid plan for private-repo Pages).
- Requires web search capability in whatever AI chat tool runs the prompt, and Claude's Code execution and file creation — always, since every result now comes back as a downloadable Word document, and for artwork generation too.
- The generated prompt opens with an explicit "execute this now — don't ask clarifying questions, don't just outline a plan" instruction, aimed at AI tools that sometimes respond with questions or recommendations instead of just running the task.
- Brand identity (name, tagline, eyebrow, background, themes) is not saved automatically anywhere — use the Save/Load buttons and keep the downloaded `.json` file somewhere you'll find it again.
