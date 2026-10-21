---
name: humanize
description: Rewrites text so it reads natural and human. Use when the user asks to "humanize this", "make it sound human", "rewrite this naturally", or "paraphrase this".
---

# Humanize

1. Send the user's full text to the Akmon `humanize_text` tool. For paraphrase requests, use `paraphrase_text`. Use `get_account_status` to check the remaining allowance.
2. Per-call limit: 2500 words for both tools. If the text is longer, split it at paragraph breaks, process each part, and join the results in the original order.
3. `humanize_text` needs at least 100 words per part; merge short trailing parts into the previous one. `paraphrase_text` has no meaningful minimum.
4. Present the returned text as the answer. Do not re-edit it.
