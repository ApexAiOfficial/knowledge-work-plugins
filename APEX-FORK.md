# ApexAiOfficial fork of anthropics/knowledge-work-plugins

This fork is the ApexAI workstation's authoritative source for the components it
uses from [anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins). Architecture, provenance and runbooks:
ApexAiOfficial/agent-skills-platform (private).

## Branches

| Branch | Meaning | Who moves it |
|---|---|---|
| `main` | Untouched mirror of upstream `main`. Never commit here. | `scripts/upstream-sync` (fast-forward only) |
| `apex/dev` | ApexAI changes on top of upstream. Upstream is merged in here first. | ApexAI maintainers |
| `apex/stable` | Reviewed, known-good revision that runtimes pin to. | `scripts/promote` (fast-forward + `apex-stable-*` tag) |

## ApexAI changes

Marketplace renamed so Claude Code / Codex accept it from a non-upstream source
(upstream names are reserved for the upstream organisation):

| Manifest | Upstream name | ApexAI name |
|---|---|---|
| `.claude-plugin/marketplace.json` | `knowledge-work-plugins` | `apex-knowledge-work` |

Plugin and skill names are unchanged. Each component keeps its own upstream license
and terms; see the component's LICENSE file.
