# Codex Storyboarding Assistance

This is my Codex workspace designed to assist with **storyboarding, worldbuilding, lore development, story planning, and narrative critique**.

The workspace is centered around the [`director`](./.agents/skills/director/SKILL.md) skill, which acts as an AI story editor and orchestrator. Rather than handling every creative task through a single agent, the Director can either perform a task itself or delegate parts of a larger task to specialized subagents.

## Director and Subagents

The Director determines which approach is appropriate based on the complexity of the request.

For simple or focused tasks, the Director may handle the work directly. For larger story-development tasks, it can delegate work between specialized subagents:

- **Researcher** — examines existing story material, lore, mechanics, characters, and continuity.
- **Moodboarder** — gathers relevant inspiration from fiction, real-world concepts, history, science, culture, and other sources.
- **Theorycrafter** — develops plausible theories and possible directions for improving or progressing existing story ideas.
- **Writer** — turns sufficiently defined ideas into drafts that fit the existing story. Substantial additions require user approval before being treated as integrated material.
- **Viewer** — reviews ideas and drafts from either a new viewer's perspective or that of a dedicated fan familiar with the story.

The system is designed to preserve the distinction between **established canon, proposed ideas, inference, and speculation**, rather than allowing generated ideas to silently become part of the story.

See the full [`director`](./.agents/skills/director/SKILL.md)[ skill](./.agents/skills/director/SKILL.md) for its orchestration rules and behavior.

## Models

Most subagents default to **GPT-5.6 Luna**, as this workspace is primarily configured with ChatGPT Plus users in mind.

The model used by each subagent can be changed through its configuration in the [`agents`](./.codex/agents)[ directory](./.codex/agents).

## Configuring Your Workspace

The workspace is intentionally fairly barebones so that it can be adapted to different story projects.

For better results, customize [`AGENTS.md`](AGENTS.md) with information about how your project is organized. This can include the locations of:

- story drafts;
- character documents;
- lore and worldbuilding files;
- timelines;
- reference material;
- approved canon;
- planning documents.

This is particularly important for drafts. Subagents do not automatically know where your project expects generated drafts or story material to be placed.

Define those locations and conventions in `AGENTS.md` so the Director and its subagents can navigate the workspace consistently.

## Project Philosophy

The Director and its subagents are intended to **assist the author's creative process rather than take ownership of it**.

Agents should work from material already established by the user, clearly identify speculation or proposed additions, and ask for clarification when an important creative decision cannot be reliably inferred from the existing story.
