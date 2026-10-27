# nano-prompts (public)

On-device Gemini Nano prompt variants for [code4rain/nano-prompt-test](https://github.com/code4rain/nano-prompt-test).

## Raw URL (no auth)

```
https://raw.githubusercontent.com/code4rain/nano-prompts/main/variants.json
```

## Schema (`variants.json`)

```json
{
  "schemaVersion": 1,
  "updatedAt": "ISO-8601",
  "remoteUrl": "https://raw.githubusercontent.com/code4rain/nano-prompts/main/variants.json",
  "variants": [
    {
      "id": "article-summary",
      "kind": "article_summary | share_summary | discussion_summary | title_translate | comment_translate",
      "label": "human label",
      "version": 1,
      "system": "system prompt text",
      "userTemplate": "… {{title}} … {{body}} …",
      "temperature": 0.2,
      "maxOutputTokens": 900,
      "history": [{ "version": 1, "note": "why", "at": "ISO-8601" }]
    }
  ]
}
```

When Grok Bot improves a prompt: bump `version`, append `history`, keep `id` stable, push here. The test app refreshes without a GitHub token.

## Delivering prompts to the phone

1. Push this file (preferred), or
2. Share JSON / text containing the full `variants.json` into **Nano 프롬프트 테스트** (ACTION_SEND), or
3. Open `nanotest://prompts?url=https://…/variants.json`
