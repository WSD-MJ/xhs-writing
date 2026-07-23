---
name: xiaohongshu-note-generator
description: >
  Generate complete, publish-ready Xiaohongshu (小红书 / RED / RedNote / XHS) notes
  from a topic. Produces a fully-styled note — catchy title, body copy, emoji, and
  hashtags — matching the RED content style, ready to post. Use when the user wants
  to write a Xiaohongshu note, write 小红书, produce 小红书文案 / RED note / RedNote post,
  do xiaohongshu copywriting, create a 种草 / product-seeding note, or draft social
  content for the Chinese RED platform. Trigger keywords: xiaohongshu, 小红书, RED,
  RedNote, XHS, note generator, 笔记生成, copywriting, 文案, 种草, seeding. Requires an
  API key from wsdsocial.com.
---

# Xiaohongshu (RED) Note Generator

Generate a complete Xiaohongshu (小红书 / RED / RedNote) style note from a topic.
Provide a topic and optional style requirements, and the AI creates a fully-formatted,
ready-to-publish note (title + body + emoji + hashtags).

## Setup

1. Get your API key at https://ai.wsdsocial.com/skills
2. Set as environment variable: `WSD_API_KEY`

## Usage

```bash
curl -X POST "https://ai.wsdsocial.com/api/pub/skills/red-note-generator/_tool_86" \
  -H "Content-Type: application/json" \
  -H "key: ${WSD_API_KEY}" \
  -d '{
    "topic": "Top 5 skincare products for summer 2024",
    "request": "Friendly tone, use emoji, include bullet points, 400-600 words"
  }'
```

## Parameters

| Param     | Type   | Required | Description |
|-----------|--------|:--------:|-------------|
| `topic`   | String | Yes      | The note topic / subject |
| `request` | String | No       | Style, word count, format requirements |

## Response

Returns the generated complete Xiaohongshu (RED) note content.
