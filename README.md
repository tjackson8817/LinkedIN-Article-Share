# LinkedIn Article Share Builder

A single self-contained HTML tool that finds the 3 most on-brand, recent articles worth sharing on LinkedIn, then drafts the post — and optionally the artwork — for whichever one you pick.

**[Open the live tool](https://tjackson8817.github.io/LinkedIN-Article-Share/linkedin_article_share.html)**

No install, no account, nothing sent anywhere — it's a static form that assembles text entirely in your browser.

## A different shape than the other four tools

This is the fifth tool alongside:
- **[Target-Company-Prompt-Builder](https://tjackson8817.github.io/Target-Company-Prompt-Builder/prompt_builder.html)**
- **[Job-Posting-Finder](https://tjackson8817.github.io/Job-Posting-Finder/job_posting_finder.html)**
- **[Resume-Cover-Letter-Builder](https://tjackson8817.github.io/Resume-Cover-Letter-Builder/resume_cover_letter_tailoring.html)**
- **[Outreach-Message-Builder](https://tjackson8817.github.io/Outreach-Message-Builder/outreach_message_builder.html)**

...but it doesn't sit in the job-search funnel the way the other four do. It's for staying visible on LinkedIn between job-search activity, or just as an ongoing personal-brand tool whether or not you're job hunting at all.

## Files in this repo

| File | What it is |
|---|---|
| `linkedin_article_share.html` | The interactive tool. |
| `LinkedIn_Article_Share_User_Guide.md` | Full usage guide. |
| `LinkedIn_Article_Share_User_Guide.docx` | Same guide, as a Word document. |

## Quick start

1. Open `linkedin_article_share.html`.
2. Fill in your brand keywords and recency window.
3. Fill in your name/tagline once (reused every time after that).
4. Set your toggles — artwork, hashtags, closing question.
5. Copy the generated prompt and paste it into a new Claude chat.
6. Review the top 3 candidates and their reasoning, pick one, and review the drafted post (and artwork, if generated) before posting.

## The honesty guardrails

Only real, verifiable, currently findable articles with real URLs — never an invented source. A good-faith paywall check, honestly flagged as "Likely free," "Paywalled," or "Uncertain" rather than false confidence. If genuinely on-brand articles are thin on a given day, the tool says so rather than padding the list. The 3 picks must be 3 distinct stories, not the same event covered by three outlets. Every summary is written fresh, never copied from the source. No markdown formatting in the output, since LinkedIn doesn't render it.

## Notes

- This repo can be public or private — GitHub Pages on the free tier requires a public repo (or a paid plan for private-repo Pages).
- Requires Claude's **Web search** capability (the entire tool depends on live search) and **Code execution and file creation** if artwork generation is enabled.
