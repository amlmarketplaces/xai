# amlmarketplaces/xai

Claude Code marketplace federating all `@amlplugins/xai-*` plugins.

## Install

Add to your project's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "aml-xai": {
      "source": { "source": "github", "repo": "amlmarketplaces/xai" }
    }
  },
  "enabledPlugins": {
      "xai-chat@aml-xai": true,
      "xai-images@aml-xai": true
    }
}
```

Then launch Claude Code in the project. The marketplace is fetched from `amlmarketplaces/xai`, cached under `~/.claude/plugins/cache/aml-xai/`, and each enabled plugin is loaded from its `amlplugins` source repo.

## Plugins (2 total)

- `xai-chat` — [@amlplugins/xai-chat](https://github.com/amlplugins/xai-chat)
- `xai-images` — [@amlplugins/xai-images](https://github.com/amlplugins/xai-images)

## Related

- npm packages: `@amlplugins/xai-*` published to GitHub Packages (`https://npm.pkg.github.com`).
- Aggregating parent: [`amlmarketplaces/aml`](https://github.com/amlmarketplaces/aml) — federates every `@amlplugins/*` plugin under a single marketplace.
- AML topology: see `.claude/rules/definitions/ageni.md` § "GitHub Topology" — this repository is a Tier-4 HUB-INSTANCE under the `amlmarketplaces/` Tier-3 HUB-ORGANIZATION.

> Built by `.claude/skills/aml/metateam/marketplace/test/cross-org-amlmarketplaces-batch.mjs`.
