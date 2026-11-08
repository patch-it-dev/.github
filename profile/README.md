<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/wordmark-plain-on-dark.svg">
    <img alt="patch-it" src="assets/wordmark-plain-on-light.svg" width="320">
  </picture>
</p>

<p align="center"><b>You get the fix, not the alert.</b></p>

<p align="center">
  <img alt="Patchy, the patch-it bot, flies in and says: I'm Patchy. I work nights. When an API you use changes, you wake up to the fix." src="assets/patchy-night-shift.svg" width="880">
</p>

Every codebase pays a maintenance tax. We pay it for you.

When an API your code depends on changes, patch-it finds the exact lines it breaks and opens a pull request with the fix. Stripe removes a parameter, OpenAI shuts down a model, Anthropic retires a version: you wake up to a PR, not a production incident.

### They bump versions. Patchy fixes your code.

Use both. Dependabot and Renovate keep your packages fresh. patch-it keeps your code working when the API underneath it moves, even if you never upgraded a thing.

| | Dependabot / Renovate | patch-it |
|---|---|---|
| What sets it off | A new version of a package is released | An API you call changes, or a model you use is shut down |
| What the pull request changes | Version numbers in your manifest and lockfile | The code that calls the changed API |
| A breaking change in the new version | Left for you to fix | That's the fix |
| If you never upgrade | Nothing to do: nothing new to bump | Still needed: a shutdown breaks pinned code too |
| Where it runs | GitHub (Dependabot) or your own setup (Renovate) | Your CI, with your own model key |

### How Patchy works the night shift

| | |
|---|---|
| <img alt="asleep" src="assets/bot-asleep.svg" width="72"> | **He works while you sleep.** A GitHub Action in your CI checks the APIs you list, on a schedule. |
| <img alt="found one" src="assets/bot-found-one.svg" width="72"> | **He finds the exact lines.** Only code that actually calls the changed API; an Azure deployment named `gpt-4` is left alone. |
| <img alt="merged" src="assets/bot-merged.svg" width="72"> | **You review and merge.** A small pull request, with the source of the change linked. If he isn't sure, he opens an issue instead. Silence beats a wrong PR. |

Your code never leaves your CI, and it runs on your own model key.

### Proof

Six maintainers we'd never met have merged patch-it's pull requests (6 of 23 opened, median 1.5 days to merge, as of 2026-10-28).

### Links

[patch-it.dev](https://patch-it.dev) (go on, poke Patchy) · docs at [docs.patch-it.dev](https://docs.patch-it.dev) · status at [status.patch-it.dev](https://status.patch-it.dev)

Got fixed by patch-it? Add the badge: [![patched by patch-it](assets/patched-by-patch-it.svg)](https://patch-it.dev)

<sub>[^^] patch-it · the night shift for your dependencies</sub>
