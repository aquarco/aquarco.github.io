---
layout: default
title: aquarco — AI agents in a sealed world
permalink: /
---

## Every issue runs the full pipeline

1. **Analyze** — Understand the issue, gather context, map affected code paths, identify dependencies.
2. **Design** — Draft an implementation approach, identify risks, choose a path that won't break things.
3. **Implement** — Write the code. All changes happen inside the VM — nothing touches the host.
4. **Test** — Run the full test suite. Catch regressions before they leave the tank.
5. **Review** — Self-review the diff. Check edge cases, security implications, code style.
6. **Submit** — Open a pull request with a clear description. You review. You merge.

> The VM is a hard boundary. Agents have full autonomy **inside the glass** — network access, file writes, process execution — but nothing escapes. No credentials leak. No supply-chain surprises. The isolation layer is **not an afterthought. It is the product.**

## How we describe it

- **Issues go in.** Pull requests come out.
- The glass is **not a limitation.** It's the product.
- Sandboxed VM. Autonomous agents. **Git-native pipelines.**
- An aquarium is not a prison. **It's a world with glass walls.**
- AI agents that ship code. **Safely. While you sleep.**
