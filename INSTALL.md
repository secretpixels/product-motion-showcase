# Install and use

This is one skill folder, `product-motion-showcase/`, with a `SKILL.md`, reference files and three images. It follows the open Agent Skills format, and it is plain text plus images: no scripts, no code to run.

How you install it differs per product. Menu names and availability can change, so check the current instructions of your product (sources at the bottom).

**Downloads:** the ready-made skill ZIP, `product-motion-showcase.zip`, is on this repository's Releases page. The repository itself holds the same folder under `skills/product-motion-showcase/`.

## At a glance

| | Claude Code | Claude app | ChatGPT | Codex |
| --- | --- | --- | --- | --- |
| What you install | The folder | A ZIP with the folder inside | An upload from your computer | The folder |
| Where | `~/.claude/skills/` or `<project>/.claude/skills/` | Customize > Skills | Plugins > Skills tab > Create | `$HOME/.agents/skills/` or `<repo>/.agents/skills/` |
| Upload needed | No | Yes, a ZIP | Yes | No |
| Start it | `/product-motion-showcase` or describe the task | Describe the task, or pick it from the `/` menu | Type `@` and select it, or describe the task | `$product-motion-showcase` or describe the task |
| Availability | See sources | Free, Pro, Max, Team and Enterprise plans. Code execution must be on | Eligible Business, Enterprise, Healthcare and Edu workspaces. Admin settings apply | See sources |

The skill itself is the same everywhere. Only the folder or file you hand over and the steps in your product differ.

## Claude Code

1. Get the folder `product-motion-showcase/`: unzip `product-motion-showcase.zip` from the latest Release, or copy `skills/product-motion-showcase/` from this repository.
2. Copy it into one of these places, so that `SKILL.md` ends up inside the folder:
   - For all your projects: `~/.claude/skills/product-motion-showcase/`
   - For one project: `<project>/.claude/skills/product-motion-showcase/`
3. Start `claude`. Type `/skills` to check that it is listed.
4. Use it: type `/product-motion-showcase`, or describe the task ("make an interface video of my app").

Optional: a third-party installer, `npx skills add secretpixels/product-motion-showcase`, can copy the skill for you once the repository is public. Choose Claude Code when it asks for the target. It is not an Anthropic tool.

## Claude app (claude.ai and desktop)

1. Make sure code execution and file creation are on (Settings > Capabilities on Free, Pro and Max). On Team and Enterprise plans an owner must enable Skills under Organization settings > Skills. Anthropic states that skills need code execution to work.
2. Download `product-motion-showcase.zip` from the latest Release. The ZIP has the folder `product-motion-showcase/` at its top level, with `SKILL.md` inside that folder, which is what the app expects. Do not unzip and re-zip the files from inside the folder.
3. Go to Customize > Skills, click `+`, then Create skill, then Upload a skill, and choose the ZIP.
4. Turn the skill on in the list.
5. Use it in a new conversation: describe the task, or type `/` and pick the skill.

Uploaded skills are private to your account. On Team and Enterprise plans an owner can share a skill.

## ChatGPT

1. Skills are available to eligible ChatGPT Business, Enterprise, Healthcare and Edu users, subject to workspace settings. On Enterprise and Edu, an admin has to allow skills and skill uploading under Permissions & roles.
2. In the sidebar, select Plugins, then the Skills tab in the Plugin Directory.
3. Select Create, then Upload from your computer, and choose the skill. OpenAI's article does not say which file format the uploader accepts. Try `product-motion-showcase.zip` first, and follow the uploader's message if it asks for something else.
4. ChatGPT scans the upload before it becomes available. It is available right away, marked Needs Review, or marked Blocked.
5. Use it: type `@` and select the skill, or describe the task.

## Codex

- **Install:** Codex reads skills from `.agents/skills` in your repository (from the working folder up to the repository root) and from `$HOME/.agents/skills` for personal use. Copy the folder `product-motion-showcase/` into one of those. Codex detects changes by itself. If the skill does not show up, restart Codex.
- **Use it:** type `$product-motion-showcase`, or run `/skills`. Codex can also choose the skill by itself from its description.
- **From this repository:** you can ask Codex's built-in `$skill-installer` to download a skill from another repository. Give it the repository and the path `skills/product-motion-showcase`. Check its own prompt for the exact syntax.
- **Where it works:** according to OpenAI, standalone skills are available in the ChatGPT desktop app, Codex CLI and the IDE extension.
- **Sharing with other people:** OpenAI recommends packaging a skill as a plugin when you want others to install it.

`agents/openai.yaml` in the skill folder is the optional OpenAI metadata file. It only sets a display name, a short description and a default prompt. Other products ignore it.

## After installing, on any product

1. Start a new conversation and ask for "an interface video of my app".
2. The assistant should ask one question at a time, starting with whether it is for an app, a website or a brand.
3. Rendering a video needs code execution and file creation. If your product cannot run code, the assistant delivers the plan, the timing table and the scripts, and tells you what to run yourself. After Effects, if you want it, runs on your own computer.

Skills can steer an assistant, so read a skill before you enable it. This one has no scripts.

## Sources (read on 26 October 2026)

- Claude app: [Use skills in Claude](https://support.claude.com/en/articles/12512180) and [Create custom skills](https://claude.com/docs/skills/how-to).
- Claude Code: [Extend Claude with skills](https://code.claude.com/docs/en/skills).
- ChatGPT: [Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt).
- ChatGPT and Codex: [Build skills](https://learn.chatgpt.com/docs/build-skills).
- Open format: [Agent Skills specification](https://agentskills.io/specification).
