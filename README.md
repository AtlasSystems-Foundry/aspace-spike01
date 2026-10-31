# aspace-spike01

Test customization repository for spike 1 of Archie-Engine (`AtlasSystems-Foundry/Archie-Engine`,
`spikes/01-aspace-sandbox-from-nothing.md`). It stands in for a customer's ArchivesSpace
customization repository in the conventional layout of the hosting plan §3.12. It is public
because the spike's VM clones it anonymously; nothing here is a secret or a customer's.

| Path | What it is |
|---|---|
| `manifest.yaml` | What this tree was last qualified against and what it pins |
| `config/config.rb` | Site settings; the platform's rendered `config.rb` loads it last, so these win |
| `plugins/local/` | The local plugin: locale overrides and theme files |
| `plugins/` | Other plugins, each in its own directory, listed in the manifest |
| `stylesheets/` | XSL for exports (not web theming); empty here |
| `theme/`, `locales/` | Reserved by the layout; empty here |

Secrets never enter this repository: database and admin credentials arrive from Azure Key
Vault through the pipeline.

Unverified until the spike runs: the locale key `brand.title` in
`plugins/local/public/locales/en.yml` (the directory is documented in research note 02; the
key is from memory, and the spike report records whether it took effect).
