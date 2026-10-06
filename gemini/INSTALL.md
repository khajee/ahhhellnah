# Gemini SEO Skills Suite

From the repository root, copy the public Gemini skill directories into your Gemini skills location:

```bash
mkdir -p "$HOME/.gemini/config/skills"
cp -R gemini/skills/* "$HOME/.gemini/config/skills/"
```

The optional SEO Director definition is in `gemini/agents/seo_director.md`. Copy it only to the agent directory supported by your Gemini host.

This public bundle intentionally excludes the proprietary keyword scraper, its implementation, and its standalone skill instructions. For keyword research, use user-provided data or an explicitly approved source. Review all skill instructions and follow the host's current configuration requirements before use.
