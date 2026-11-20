# Studioscope plugin

Connects your AI assistant to [Studioscope](https://studioscope.app), the studio management app for creative studios, and adds skills for review status, scheduling from notes and drafting scopes.

## What it does

- **Connector** (`.mcp.json`): the Studioscope MCP server at `https://studioscope.app/api/mcp`. You sign in with your Studioscope account the first time; it then acts as you, in the studios you belong to. It can list projects and read deliverable approval status, review feedback and schedules. Staff can add milestones, events and tasks. Studio admins can also read the rate card, draft and revise scopes, check signing status, look up client contact details, create projects and change a project's title or deadline. Clients can ask the studio for changes on a deliverable. It never sends a scope, approves work or changes a project's status.
- **Skill** `studioscope-review-status`: answers "what's waiting on the client?" by combining approval status and open feedback into a short update.
- **Skill** `studioscope-schedule-from-notes`: turns an email or call notes into milestones, shoot days, calls and tasks, after you confirm the plan.
- **Skill** `studioscope-scope-from-notes`: drafts a scope from meeting notes, priced from your rate card, for you to review and send in Studioscope.

## Data

Requests go only to Studioscope, under your own account and permissions. Clients and team members see only the projects they are assigned to. See the [privacy policy](https://studioscope.app/privacy).

## Install

- Claude Code: `claude plugin marketplace add studioscope/studioscope-plugin`, then `claude plugin install studioscope@studioscope`
- Other agents (skills only): `npx skills add studioscope/studioscope-plugin`
