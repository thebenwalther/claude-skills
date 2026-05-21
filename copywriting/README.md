# Copywriting Skills

A three-skill router stack for producing platform-optimized, masters-level copy. The skills are hierarchical — always enter through `platform-aware-copy-router`, which owns the routing decision and dispatches to the right downstream skill.

---

## How the stack works

```
platform-aware-copy-router        ← always start here
        │
        ├── social-media-posts    ← X or LinkedIn
        │
        └── copy-framework-router ← everything else
                                    (newsletter, landing page, email, blog, article)
```

**Never invoke `social-media-posts` or `copy-framework-router` directly** unless you know exactly which one you need. The router exists to make that judgment for you based on platform context.

---

## Skills

### platform-aware-copy-router
The entry point. Asks for platform if not stated, then routes to the appropriate downstream skill. Owns the routing decision; the downstream skills own the execution.

**Triggers:** any copywriting request — `write a post`, `create a newsletter`, `draft a landing page`, `write copy for`, `help me write something for [platform]`

> If platform is unclear, it will ask before routing.

---

### social-media-posts
Creates high-engagement, platform-optimized posts for **LinkedIn** and **X (Twitter)**. Applies data-backed formatting rules, platform-specific voice, and sharp human-sounding copy. Built for personal brands, solopreneurs, and thought leaders building in public.

**Routed here when:** the platform is X or LinkedIn
**Direct triggers:** `write a tweet`, `write a LinkedIn post`, `what should I post about X`, repurposing content for social

**What it handles:**
- Single posts and threads
- Hook writing
- Repurposing long-form content into social-native formats
- Platform-specific formatting (character limits, line breaks, hashtag strategy)

---

### copy-framework-router
Selects the optimal copywriting framework for the job and drafts masters-level copy. Applies 1-3-1 formatting, staccato rhythm, curiosity gaps, and anaphora automatically — no need to name a framework.

**Routed here when:** the platform is newsletter, landing page, email, blog, or article
**Direct triggers:** `write a newsletter`, `draft a landing page`, `write email copy`, `write a hook`, `write a thread`

**What it handles:**
- Newsletters and essays
- Landing pages and sales copy
- Email sequences
- Long-form hooks and leads
- Any persuasive writing that isn't X or LinkedIn
