# Prompt Framework — AI SEO Blog & Content Cluster Generator
**Task 3 | Future Interns Prompt Engineering Internship**

---

## Overview

This document outlines the structured prompt system designed to generate SEO-optimized blog content and content clusters for business websites using AI tools.

Real SEO agencies don't write random blog posts. They build **content clusters** where a single strong pillar article is supported by several smaller blogs, all internally linked, all targeting related keywords. This framework replicates that system using structured prompts.

---

## Prompt Architecture

The system uses a **5-layer prompt structure**:

```
Layer 1: Business & SEO Context    --> Business type, location, target keywords, audience
Layer 2: Keyword Strategy          --> Primary + secondary keywords, search intent mapping
Layer 3: Pillar Blog Generation    --> Long-form, authority-building main article
Layer 4: Supporting Blog Cluster   --> 3-5 smaller blogs that link back to the pillar
Layer 5: Local SEO Adaptation      --> City + service keyword integration
```

---

## Main Context Prompt (Run First)

```
You are an SEO content strategist and blog writer for a digital marketing agency.
Your job is to write helpful, search-optimised blog content that ranks on Google
and builds trust with potential clients.

Business Name: [BUSINESS_NAME]
Business Type: [TYPE — e.g., digital marketing agency, dental clinic, gym]
Location: [CITY, COUNTRY]
Target Audience: [WHO THEY SERVE — e.g., small business owners in Dubai]
Primary Service: [MAIN SERVICE — e.g., SEO, social media marketing, web design]
Primary Keyword: [MAIN KEYWORD TO RANK FOR]
Tone: [TONE — e.g., professional but approachable, authoritative, friendly]
Goal: [BUSINESS GOAL — e.g., generate leads, build authority, attract local clients]

Content rules:
- Write for humans first, search engines second
- Use headings (H1, H2, H3) clearly and logically
- Include the primary keyword naturally — never stuff it
- Every blog must end with a business-focused conclusion and CTA
- Keep paragraphs short and scannable
- Avoid generic filler content — every section must add value

Acknowledge this brief and wait for section-specific instructions.
```

---

## Prompt 1 — Keyword Strategy & Content Cluster Map

Run this before writing any content. It maps out the entire cluster so all blogs are coordinated.

```
Using the business context above, create a keyword strategy and content cluster map.

Include:

PRIMARY KEYWORD
- The main keyword the pillar blog will target
- Search intent (informational / commercial / navigational / transactional)
- Why this keyword was chosen

CONTENT CLUSTER MAP
List 1 pillar blog and 4 supporting blogs:

For each blog include:
- Blog title (SEO-friendly, include keyword)
- Target keyword
- Search intent
- Why it supports the pillar
- Suggested internal link anchor text

LOCAL SEO KEYWORDS
- 5 location-based keyword variations
  (e.g., "digital marketing agency Dubai", "SEO services Dubai SMEs")
- Explain where each should appear naturally in content

Format as a clear table or structured list.
```

---

## Prompt 2 — Pillar Blog Generation

```
Using the keyword strategy above, write the full pillar blog.

Requirements:
- H1: Include primary keyword, under 60 characters
- Introduction: 100-150 words, hook + problem + what the article covers
- H2 sections: 5-7 main sections, each 150-250 words
- H3 subsections: Use where content needs further breakdown
- Include primary keyword in: H1, first paragraph, at least 2 H2s, conclusion
- Internal linking: Add 3 [LINK TO: blog title] placeholders where supporting blogs fit naturally
- Conclusion: 100 words, summarise + soft CTA (contact / get a quote / learn more)
- Word count: 1200-1500 words total
- Tone: Match business tone from context prompt

Do not use keyword stuffing. Write as if advising a friend who owns a small business.
```

---

## Prompt 3 — Supporting Blog Generation

Run this prompt once per supporting blog, changing the target keyword each time.

```
Write a supporting blog for the content cluster.

Target keyword: [SUPPORTING KEYWORD]
Search intent: [INTENT]
How it links to pillar: [RELATIONSHIP]

Requirements:
- H1: Include target keyword, under 60 characters
- Introduction: 75-100 words
- H2 sections: 3-4 sections, each 100-150 words
- Include 1 [LINK TO: Pillar Blog Title] internal link placeholder
- Conclusion: 75 words with soft CTA
- Word count: 600-800 words
- Tone: Match business tone from context prompt

Focus on answering one specific question the reader has.
Do not try to cover everything — this blog supports the pillar, it doesn't replace it.
```

---

## Prompt 4 — Local SEO Adaptation

```
Review the pillar blog and suggest local SEO improvements.

Provide:

KEYWORD PLACEMENT REVIEW
- Where to naturally add location keywords (Dubai, UAE, specific districts)
- Which headings should include location
- Meta title suggestion (under 60 characters, includes keyword + location)
- Meta description suggestion (under 155 characters, includes CTA)

SCHEMA MARKUP SUGGESTION
- Recommend the most relevant schema type (LocalBusiness, Article, FAQ)
- Explain why it helps this content rank locally

PEOPLE ALSO ASK TARGETS
- List 5 questions from Google's People Also Ask that this content cluster should answer
- Suggest which blog (pillar or supporting) should answer each one

Format clearly with section labels.
```

---

## Prompt Engineering Notes

| Principle | How It's Applied |
|---|---|
| **Role prompting** | "SEO content strategist and blog writer" sets expert behaviour |
| **Constraint-based prompting** | Word counts, heading rules, keyword placement rules prevent generic output |
| **Cluster thinking** | Pillar + supporting structure baked into Layer 1 planning prompt |
| **Intent mapping** | Search intent specified per blog to align content with what users actually want |
| **Local SEO layer** | Separate prompt dedicated to location keyword integration |
| **Modular design** | Supporting blog prompt runs independently, reusable per keyword |

---

## Tool Used
**Claude (claude.ai)** — Selected for its ability to maintain consistent tone across long-form content and follow complex structural constraints reliably.

---

*Task 3 — Future Interns Prompt Engineering Internship Program*