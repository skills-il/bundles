# Skills-IL Bundles

Curated collections of AI agent skills for common Israeli workflows. Each bundle groups 3-7 skills that work together, so you can install everything you need with a single command.

Browse bundles at **[agentskills.co.il/bundles](https://agentskills.co.il/bundles)**

## Available Bundles

| Bundle | Skills | Description |
|--------|--------|-------------|
| [freelancer-accountant](./freelancer-accountant) | 5 | Invoices, VAT, expenses, and receipts for freelancers |
| [israeli-tax-season](./israeli-tax-season) | 5 | Annual tax filing, VAT reporting, and tax planning |
| [small-business-starter](./small-business-starter) | 5 | Invoicing, bookkeeping, payroll, and customer support |
| [israeli-dev-toolkit](./israeli-dev-toolkit) | 5 | Hebrew i18n, RTL, ID validation, phone formatting |
| [government-navigator](./government-navigator) | 5 | Bureaucracy, Bituach Leumi, forms, and fines |
| [legal-compliance](./legal-compliance) | 5 | Employment law, privacy, e-commerce, and contracts |
| [marketing-il](./marketing-il) | 5 | Hebrew SEO, social content, email, LinkedIn, ads |
| [hebrew-first](./hebrew-first) | 5 | Hebrew content, documents, accessibility, RTL, NLP |

## Install a Bundle

```bash
# Install all skills in a bundle
npx skills-il add-bundle freelancer-accountant

# Preview what will be installed
npx skills-il add-bundle freelancer-accountant --dry-run

# List all available bundles
npx skills-il bundles
```

Non-CLI users (Claude Desktop, ChatGPT) can download bundles as ZIP files from the [bundle pages](https://agentskills.co.il/bundles).

## Bundle Structure

Each bundle is a folder with:

```
bundle-name/
  bundle.json      # Metadata, skills list, FAQ, prompts
  README.md        # English description
  README_HE.md     # Hebrew description
```

### bundle.json

```json
{
  "name_en": "Bundle Name",
  "name_he": "...",
  "description_en": "Short description",
  "description_he": "...",
  "icon": "...",
  "tags": ["tag1", "tag2"],
  "tags_he": ["..."],
  "skills": [
    { "slug": "skill-slug", "repo": "skills-il/category-repo", "path": "skill-slug" }
  ],
  "faq": {
    "en": [{ "q": "Question?", "a": "Answer." }],
    "he": [{ "q": "...", "a": "..." }]
  },
  "prompts": [
    {
      "title": { "he": "...", "en": "Short title" },
      "body": { "he": "...", "en": "Full prompt text the user sends to the AI" }
    }
  ]
}
```

## Sync

Bundles are synced to the AgentSkills database via `pnpm sync-bundles` in the [skills-il](https://github.com/choroshin/skills-il) monorepo. The sync runs daily and on manual dispatch.

## Contributing

To propose a new bundle, open an issue on the [skills-il](https://github.com/choroshin/skills-il) repo describing the use case, target audience, and which skills should be included.

## License

MIT
