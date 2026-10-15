<p>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/dejima-org/dejima/main/assets/dejima-wordmark-darkmode.png">
  <img src="https://raw.githubusercontent.com/dejima-org/dejima/main/assets/dejima-wordmark-lightmode.png" alt="dejima" height="72">
</picture>
</p>

**Sandboxing for unsupervised coding agents, built on the assumption that the agent is hostile.**

A coding agent with its permission prompts off can be turned by a prompt injection or a poisoned dependency mid-session, and it will not announce it. dejima decides in advance what such a session can reach, take and break. The sister projects bound the layers a sandbox inside the machine cannot: the machine itself, the CI runner that executes the agent's pull requests, and noticing afterwards that something changed.

| Project | Runs on | What it does |
| --- | --- | --- |
| **[dejima](https://github.com/dejima-org/dejima)** | your devbox | Runs the agent in a firewalled container: deny-by-default egress, credentials that stay on the host, per-project approval. **Start here.** |
| **[dejima-devbox-hardener](https://github.com/dejima-org/dejima-devbox-hardener)** | the same devbox | Cuts the VM's reach into your network to what is declared, enforced from outside the guest. |
| **[dejima-guard](https://github.com/dejima-org/dejima-guard)** | a different machine | Notices when the devbox changes and alerts you. Detection, not enforcement. |
| **[dejima-ci-hardener](https://github.com/dejima-org/dejima-ci-hardener)** | your CI runner | Runs agent-authored pull requests without that being access to your network. |
| **[dejima-badge](https://github.com/dejima-org/dejima-badge)** | your README | A "Developed in dejima" badge. |

Only dejima is required. [The threat model](https://github.com/dejima-org/dejima/blob/main/docs/threat-model.md#the-stack-and-what-each-piece-buys) says what each of the others buys and what goes wrong without it. To get started, see [dejima's setup](https://github.com/dejima-org/dejima#setup).

**Early development, one maintainer.** None of this has been through outside review or an audit, and nothing about it is supported. Do not put it anywhere being wrong about it would matter. Report vulnerabilities as [SECURITY.md](https://github.com/dejima-org/dejima/blob/main/SECURITY.md) describes, not in public.

**These repositories are read-only mirrors.** Development happens on a private forge, so issues and pull requests are off here. Forks are welcome; see [CONTRIBUTING.md](https://github.com/dejima-org/dejima/blob/main/CONTRIBUTING.md). The code is GPL-3.0-or-later. The name, logo and wordmark are trademarks, covered by [ATTRIBUTION.md](https://github.com/dejima-org/dejima/blob/main/ATTRIBUTION.md).
