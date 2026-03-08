# security-skills

> PUBLIC REPO — No secrets, no PII, no internal references. Assume strangers read everything.

## Purpose

Claude Code plugin for **dev security** — tools and methodologies for finding vulnerabilities in code. Includes Joern CPG analysis, with future pentest methodology skills (injection, XSS, auth, authz, SSRF, recon).

This is NOT ops security (secrets management, credential handling). Those concerns live in workspace toolkits (ops-toolkit, threads-toolkit).

## Type

Plugin (Claude Code marketplace format)

## Origin

OWN — built on Kali. Source of truth for security skills deployed across machines.

## Structure

```
.claude-plugin/
  marketplace.json          # marketplace metadata
  plugin.json               # plugin metadata (name, version, description)
skills/
  joern-analysis/SKILL.md   # Joern CPG security analysis workflow
```

## Install

```bash
claude plugin marketplace add BlockSecCA/security-skills
claude plugin install security-skills@security-skills --scope user
```

## Development

- Edit skills here, validate with `claude plugin validate .`
- joern-analysis source of truth is `~/public/joern-mcp/.claude/skills/joern-analysis/SKILL.md` — copy here after changes
- Pentest skills are developed in `~/private/pentest-playbooks/` and graduate here as SKILL.md files when complete
- This is a PUBLIC plugin — no secrets, no internal references, no machine-specific paths

## Practices

- After corrections: "Update CLAUDE.md so you don't make that mistake again"
- Bump version in both `marketplace.json` and `plugin.json` on changes
- Validate before pushing: `claude plugin validate .`
