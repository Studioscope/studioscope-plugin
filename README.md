# Studioscope agent plugins

Plugin marketplace for [Studioscope](https://studioscope.app), the studio management app for creative studios. The `studioscope` plugin bundles the Studioscope connector (a remote MCP server) and three skills: review status, scheduling from emails and notes, and drafting scopes from meeting notes. See [the plugin README](plugins/studioscope/README.md).

```bash
claude plugin marketplace add studioscope/studioscope-plugin
claude plugin install studioscope@studioscope
```

Other agents (skills only):

```bash
npx skills add studioscope/studioscope-plugin
```
