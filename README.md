# Content-Multiplier-Skill

A Claude Code plugin that transforms a single piece of content into multiple platform-optimized formats — X/Twitter threads, LinkedIn posts, email newsletters, Instagram captions, YouTube descriptions, and blog summaries.

## What It Does

Give it one piece of content (a blog post, article, notes, or raw text) and it generates platform-native versions for 6 formats:

| Format | What You Get |
|--------|-------------|
| **X/Twitter Thread** | 5-10 tweet thread with hook and CTA |
| **LinkedIn Post** | Professional post with white space and engagement question |
| **Email Newsletter** | Subject line, preview text, and conversational body |
| **Instagram/TikTok** | Caption with hook, value, CTA, and hashtags |
| **YouTube Description** | SEO summary, timestamps, takeaways, subscribe CTA |
| **Blog Summary** | TL;DR, key takeaways, SEO title, meta description |

## Installation

```bash
claude plugin install /path/to/Content-Multiplier-Skill
```

Or add to your project's `.claude/settings.json`:

```json
{
  "plugins": ["/path/to/Content-Multiplier-Skill"]
}
```

## Usage

### Command

```
/multiply [source content or file path]
```

Examples:

```
/multiply Here's my blog post about remote work productivity...
```

```
/multiply ./blog/my-latest-post.md
```

### Auto-Triggered Skill

The skill also activates automatically when you say things like:
- "Turn this into social media posts"
- "Repurpose this content"
- "Make a Twitter thread from this"
- "Adapt this for LinkedIn"

## Plugin Structure

```
Content-Multiplier-Skill/
├── .claude-plugin/
│   └── plugin.json
├── commands/
│   └── multiply.md
├── skills/
│   └── content-multiplier/
│       ├── SKILL.md
│       ├── examples/
│       │   └── example-output.md
│       └── references/
│           └── platform-specs.md
└── README.md
```

## How It Works

1. **Analyze** — Reads your source content and extracts core message + key insights
2. **Transform** — Generates platform-native content for each format
3. **Deliver** — Outputs everything to `content-multiplied.md` and displays results

Each output follows platform best practices:
- Character limits respected
- Tone adapted (casual for X, professional for LinkedIn, conversational for email)
- Every format has a hook and CTA
- No copy-pasting between formats — each feels native

## License

MIT
