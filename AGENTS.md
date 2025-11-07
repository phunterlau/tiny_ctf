# picoCTF Agent Playbook

## Mission Mindset
- Clarify the challenge objective, its input/output expectations, and success criteria before touching the keyboard.
- Keep a running hypothesis list; update or discard hypotheses as evidence arrives.
- Track assumptions explicitly so they can be validated or discarded quickly.
- Always ask: *Which tools can I use right now?* Favor quick probes before deep dives.

## Workflow Habits
- Start with lightweight enumeration (strings, file, linpeas-style scripts, etc.) to map the landscape.
- Script repeatable tasks; document command snippets and parameters for later reuse.
- Log discoveries, dead ends, and ideas so context survives breaks.
- Stick to the currently activated conda environment for all tooling; avoid switching mid-challenge.
- For each challenge directory, maintain a `memory.md` stored inside that directory (e.g. `./276/memory.md`) to keep notes isolated per problem; always append updates and revisit it before continuing work.
- Set checkpoints; if progress stalls, revisit the initial objective and constraints.

## Sanity Checks
- Reconfirm the intended flag format and submission portal requirements.
- Cross-check puzzle artifacts against known formats (magic numbers, headers, hashes).
- Validate exploits locally before deploying against the remote service.
- Ask regularly: *Have I jumped into a rabbit hole?* If so, back out and reassess.

## Collaboration Cues
- Share partial findings and weird observations early; another agent may see the angle.
- When requesting help, provide the steps already taken and the evidence collected.
- Respect handoffs: leave concise notes, artifacts, and next-step suggestions.

## Toolbelt Essentials
- Core CLI: `file`, `strings`, `xxd`, `hexdump`, `grep`, `awk`, `sed`, `jq`.
- Reverse engineering: `ghidra`, `radare2`, `gdb`, `pwntools`.
- Web: `burpsuite`, browser DevTools, `curl`, `sqlmap`.
- Crypto/forensics: `sage`, `z3`, `hashcat`, `binwalk`, `volatility`.
- Binary artifacts: identify with `file`, then pick the right tool (`objdump`, `readelf`, `strings`, etc.); for `.pyc` use `decompyle3` or `xdis`, either via CLI or a quick Python decompiler script.
- Infrastructure: SSH tunneling, port forwarding, Docker for replicas.
- Keep notes on tool quirks, flags, and gotchas encountered mid-CTF.

## Time Management
- Break the challenge into milestones; estimate effort and reassess after each milestone.
- Rotate tasks between team members to avoid burnout and bring fresh perspectives.
- If an approach yields no signal after a reasonable slice of time, escalate or pivot.
- Save confirmed vulnerabilities, scripts, and payloads in a shared repository for future reuse.

## Finishing Strong
- Sanitize and archive artifacts, scripts, and write-ups immediately after capture.
- Verify the flag submission (typos, whitespace) before declaring victory.
- Always produce a walkthrough markdown covering highlights, tools, failures, path to victory, and reflection for each CTF challenge.
- After grabbing the flag, save a `walkthrough.md` in the challenge directory with the write-up.
- Reflect on what worked, what failed, and which skills or tools to sharpen next.
