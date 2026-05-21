---
name: platform-aware-copy-router
description: "Meta-router that intelligently directs copywriting requests to the optimal skill based on platform. If writing for X or LinkedIn, delegates to social-media-posts (platform-specific voice, format, engagement rules). If writing for any other medium (newsletter, landing page, email, blog, article), delegates to copy-framework-router (framework selection + universal composition). TRIGGERS: any copywriting request where platform matters ('write a post', 'create a newsletter', 'draft a landing page', 'write copy for', etc.). Always ask for platform first if not stated. This skill owns the routing decision — the downstream skills own the execution."
---

# Platform-Aware Copy Router

The intelligent dispatcher for all copywriting work. Routes social media content to the platform specialist. Routes everything else to the framework engine. Saves time by preventing wrong-tool usage and ensuring every piece gets the right composition approach.

---

## Core Logic

```
IF platform == "X" or platform == "Twitter" or platform == "Tweet"
  → social-media-posts skill
  (Platform-specific voice, format, engagement window, length constraints)

ELIF platform == "LinkedIn" or platform == "LinkedIn post"
  → social-media-posts skill
  (Platform-specific voice, format, photo guidance, engagement rules)

ELSE (newsletter, email, landing page, blog, article, sales page, etc.)
  → copy-framework-router skill
  (Framework selection + universal composition techniques)
```

**This is not negotiable.** Social-media-posts owns X and LinkedIn. Copy-framework-router owns everything else.

---

## Step 1: Gather the Three Essential Inputs

Before routing, confirm these three things. If any are missing or ambiguous, ask once — briefly — before proceeding.

### 1. Platform
**Where is this content going to live?**

**Social media platforms** (route to social-media-posts):
- X (Twitter)
- LinkedIn

**Everything else** (route to copy-framework-router):
- Newsletter / email
- Landing page / sales page
- Blog post / article
- Email sequence
- Social post for TikTok, Instagram, Facebook, YouTube, etc. (these go to copy-framework-router as they don't have dedicated platform rules yet)
- Long-form content of any kind

### 2. Goal
**What is this piece trying to do?**

- Build awareness / establish authority
- Drive engagement (replies, shares, comments)
- Convert to a sale or offer
- Deliver standalone value / educate
- Research (gather replies and data)
- Spark discussion

### 3. Topic / Message
**What's the core idea?**

Get specific. "Productivity" is not a topic. "Why most people's morning routines fail by 9am" is.

---

## Step 2: Route to the Right Skill

Use this decision table:

| Platform | Route To | Why |
|----------|----------|-----|
| X, Twitter | social-media-posts | Has X-specific rules: 70–100 char optimal, text-only best, no hashtags/links, fast reply window |
| LinkedIn | social-media-posts | Has LinkedIn-specific rules: 140-char hook, carousel format (24.42% engagement), personal photo guidance, narrative voice |
| Newsletter, Email | copy-framework-router | Framework selection (Pain-Insight-Action, PAIPS, etc.) matters more than platform mechanics |
| Landing page, Sales page | copy-framework-router | Always 5-4-3-2-1 framework — this is defined, not emergent |
| Blog, Article, Long-form | copy-framework-router | Framework selection (Pyramid Principle, Zero-Click Micro-Story, etc.) + universal composition |
| TikTok, Instagram, Facebook, YouTube, etc. | copy-framework-router | No dedicated platform rules yet; use framework + composition |

---

## Step 3: Execute the Delegation

**If routing to social-media-posts:**

You are done routing. The social-media-posts skill now owns the entire workflow:
- It will ask about voice calibration if needed
- It will apply platform-specific rules automatically
- It will deliver in platform-native format (with line breaks, spacing, structure)
- It will provide platform notes and optional variations

**If routing to copy-framework-router:**

You are done routing. The copy-framework-router skill now owns the entire workflow:
- It will select the optimal framework based on goal and medium
- It will apply universal composition techniques
- It will deliver multiple variants if meaningful alternatives exist
- It will flag any trade-offs or strategic decisions

---

## Decision Tree (Visual Reference)

```
User brings copywriting request
         ↓
Is the platform explicitly stated?
    ↙                    ↖
  YES                     NO
   ↓                       ↓
Platform = X or LinkedIn? Ask: "Where is this going?"
   ↙         ↖              ↓
  YES        NO         [User answers]
   ↓         ↓             ↓
ROUTE TO   ROUTE TO    Does answer match X/LinkedIn?
social-   copy-frame     ↙        ↖
media-    work-router   YES      NO
posts              ↓       ↓
                 ROUTE TO both paths
              social-media-posts
              or copy-framework-router
```

---

## What This Router Does NOT Do

- **It does not write the copy.** That's the downstream skill's job.
- **It does not make framework recommendations.** Copy-framework-router does that.
- **It does not apply platform rules.** Social-media-posts does that.
- **It does not hold strategic opinions about voice.** Each skill owns voice for their domain.

This router is a decision layer only. Its job is to ask one clarifying question, make the route, and hand off completely.

---

## When to Ask Clarifying Questions

Ask **once and only once** if:

1. **Platform is not stated**: "Where is this going—X, LinkedIn, newsletter, landing page, or something else?"
2. **Platform is ambiguous**: User says "social media" but doesn't specify which platform → "X or LinkedIn?" (these need different skills; everything else goes to framework-router)
3. **Medium is unclear**: User says "create a post" but you don't know if it's X or a blog post → "Where will this live?"

Do **not** ask about goal, topic, or voice. Those are each downstream skill's responsibility. This router only cares about platform.

---

## Output Format

Once you've routed, your output is simply:

**[Routing decision stated clearly]**

Example outputs:

---

"**Routing to: social-media-posts** (X detected — this needs platform-specific voice, format, and engagement rules)"

[Then execute social-media-posts workflow]

---

"**Routing to: copy-framework-router** (Newsletter detected — this needs framework selection + universal composition)"

[Then execute copy-framework-router workflow]

---

That's it. The routing decision is stated. Then you hand off to the downstream skill's full workflow.

---

## The Three Skill Ecosystem

This is how all three work together:

```
User Request
     ↓
Platform-Aware Copy Router (routing decision only)
     ↓                              ↓
X or LinkedIn?                   Everything else?
     ↓                              ↓
social-media-posts              copy-framework-router
(platform rules,                (framework selection,
 voice calibration,             universal composition,
 format selection)              red flag test)
     ↓                              ↓
Platform-optimized            Framework-driven
social content                 persuasive content
```

---

## Reference: When Each Skill Owns the Work

| Skill | Owns | Does Not Own |
|-------|------|--------------|
| **platform-aware-copy-router** | Routing decision, platform classification | Writing, framework selection, composition |
| **social-media-posts** | X and LinkedIn posts, platform rules, voice calibration, format selection | Other platforms, frameworks, long-form content |
| **copy-framework-router** | Framework selection, universal composition, any non-social medium | Platform-specific rules, social media voice, X/LinkedIn constraints |

---

## Important Notes

- **This router is transparent.** You state which skill you're routing to and why. No hidden magic.
- **The downstream skill is complete.** Once routed, that skill executes its full workflow. You don't interrupt or override.
- **No skill redundancy.** If social-media-posts can handle it, copy-framework-router doesn't touch it. Vice versa.
- **Platform is the primary decision lever.** Everything else (goal, topic, voice) is secondary and handled downstream.

---

## Examples of Routing in Action

**User:** "Create an X post about Tony Robbins and decision-making"

**Router:** Routing to: **social-media-posts** (X detected)

[social-media-posts executes: asks about voice/goal, applies X rules, delivers 70–100 char post with Pattern Interrupt format, no links/hashtags]

---

**User:** "Write a newsletter about decision-making frameworks"

**Router:** Routing to: **copy-framework-router** (Newsletter detected)

[copy-framework-router executes: selects Pain-Insight-Action or PAIPS framework, applies staccato rhythm + anaphora, delivers newsletter-length copy]

---

**User:** "I need to write something about my new offer"

**Router:** "What medium — X, LinkedIn, newsletter, landing page, email, or blog post?"

**User:** "Landing page"

**Router:** Routing to: **copy-framework-router** (Landing page detected)

[copy-framework-router executes: routes to 5-4-3-2-1 framework, builds the page with benefits/objections/testimonials/pricing/bonus]

---

**User:** "Help me write a LinkedIn post about decision-making"

**Router:** Routing to: **social-media-posts** (LinkedIn detected)

[social-media-posts executes: asks about format (Story Hook vs List Post), recommends personal photo, applies LinkedIn voice (narrative, credibility-forward), delivers with 140-char hook + white space structure]

---

## When to Suggest This Router

Offer this to users who:
- Ask for copywriting across multiple platforms (you clarify once, eliminate confusion)
- Don't know which skill to use for their content
- Have a piece that's not fitting well with one skill's approach (reroute via this router)
- Want a single point of entry for all copy work

Say: "I can route this to the right skill depending on where it's going. Platform?"
