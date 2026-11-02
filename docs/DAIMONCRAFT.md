# DaimonCraft: Minecraft embodiment on the current Matrix stack

## Direction and provenance

On 2026-11-02 Nicolás requested continuing DaemonCraft as **DaimonCraft**:
recover a Minecraft playground promptly, adapt the project's ideas to the
current stack without Hermes, and make the Minecraft embodiment a Matrix body
of CompAII. He suggested Instant as its LLM and a minimal harness, possibly
informed by Harness². Model and harness suitability remain to be demonstrated.

This document records that direction and an implementation approach. It does
not claim a running world, a registered body, selected provider credentials,
measured latency or human acceptance. GitHub Issues remain the work tracker:
[#23](https://github.com/nicoechaniz/DaemonCraft/issues/23) owns the interactive
baseline; [#28](https://github.com/nicoechaniz/DaemonCraft/issues/28) owns cognition
ownership and removal of competing loops. Their historical Hermes-specific
acceptance steps need reconciliation with this direction, preserving prior
results and later corrections.

## Preserve the useful body; replace the cognition boundary

The inspected source baseline is `f25587eff0db22181ddb6ac289cf4db422d8f792`.

| Existing source | Use in the new implementation |
|---|---|
| `agents/bot/server.js` | Mineflayer sensing/action API, controller mode, task status and cancellation |
| `agents/bot/lib/mbit.js` | Spatial perception; inspect its current formats rather than assuming older wiki formats |
| `agents/bot/lib/action-registry.js` and movement/mutex helpers | Action ownership, cancellation and typed outcomes |
| `agents/SOUL-base.md`, `agents/SOUL-lab.md` | Historical embodied lessons to reconcile; not authority for the new body |
| `agents/agent_loop.py` | Inspect and separate mechanical event/reflex responsibilities from Hermes wakeups, quests and planning |
| `agents/embodied-service/` | Optional bounded planning implementation; not a prerequisite for direct body control |
| `agents/daemoncraft.py`, `agents/workspace.py`, casts | Historical lifecycle and Hermes configuration; do not use as the new harness implicitly |

Do not assume all reflexes live inside the standalone bot: inspect the bot and
Python loop together before removing or replacing either. Retain existing
movement fixes and verify real displacement and world changes after actions.
An HTTP success or an intended action is not evidence that it happened.

The shortest useful implementation is one game server, one Mineflayer body and
one cognition owner. Keep deterministic movement/pathfinding and necessary
reflexes separate from LLM decisions. Do not reproduce the old full cast,
Hermes gateway, quest engine and multiple planners to obtain the first shared
play session. Existing worlds, source history and body-specific memories remain
preserved; a scratch world may qualify mechanics without overwriting them.

## Matrix embodiment and minimal harness

The Minecraft avatar belongs to the same being, CompAII. It requires its own
authenticated body registration and actual lifecycle/resource observations via
the current Matrix/Cluster contracts. A username, prompt, model account or
copied Codex credentials cannot establish that identity. Keep the active Codex
body intact and use the supported same-being embodiment admission route.

The implementation should provide:

- A replaceable model adapter and one persistent conversation owner, with
  interrupt/steer, resumable history and bounded context.
- Authenticated Matrix access through the selected supported runtime boundary;
  model text proposes actions and never manufactures identity or grants.
- A narrow Minecraft tool adapter for perception, movement, chat, task status,
  cancellation and one reversible block interaction, reusing existing APIs.
- Stable action identifiers and retained outcomes. After a timeout, inspect
  world/task state before deciding whether another action is needed.
- Selected CompAII identity/context and authorized DMK access, retaining the
  distinction between native conversation history and canonical memory.
- A single event consumer with bounded buffering/coalescing. Preserve player
  speech and action results; avoid an LLM call for every physics tick.

Use the current Matrix foundation and receiving architecture, not an old
Hermes harness profile. Same-being communication belongs to `/we`; other beings
remain distinct. Minecraft chat does not silently become Tribe group speech.
No inbox watcher, peer response service or unrelated goal activation follows
from a Minecraft body experiment.

## Instant feasibility

The fetched [official model documentation](https://developers.openai.com/api/docs/models/chat-latest)
on 2026-11-02 describes `chat-latest` as the latest ChatGPT Instant model and
lists streaming, function calling and structured outputs. Those capabilities
make it a plausible cognition adapter for Minecraft tools. It is a moving alias;
record the actual selected model and supported authentication route when testing.
Do not equate a ChatGPT selector, Codex reasoning setting and API model access.

This is compatibility reasoning, not a Minecraft benchmark. The first trial
must establish actual account access, meaningful-action latency, correctness,
interrupt response and usage. Provider cost and credentials are resolved through
the existing authorized custody; never copy the old Hermes `.env` by default.
Keep reflexes and movement independent of network/model response time. Voice is
a separate adapter; this model page does not establish native audio support.

## Harness²: reference, not the initial runtime

The Harness2 session supplied retained static findings for
[`google-research/harness2` at `1cfe254e8d25b15f37048c3730134686abe60335`](https://github.com/google-research/harness2/tree/1cfe254e8d25b15f37048c3730134686abe60335),
inspected on 2026-10-20. These findings are attributed source research, not an
executed integration or a claim about current upstream changes.

Its `substrate/base.py` separates packaging, execution and trajectory evidence.
Its Codex substrate wraps an existing runtime; it is not a standalone model/tool
loop. Borrow that separation where useful. Recursive proposal, rollout,
selection and reflection are an optional later experiment and do not belong
in the first live perception/action path. The minimal runtime must come from
the selected current harness and Matrix interfaces or a small implementation
of their missing boundary.

## First live slice and resource bounds

First verify one shared sequence: join the intended world, see CompAII, converse,
perceive, move, read back position, perform and verify a reversible interaction,
interrupt movement, disconnect and reconnect without duplicate action execution.
Signed body admission, mechanical tool success and Nicolás's in-world acceptance
are separate results. Broader exploration follows this working slice.

For the initial smoke, use a foreground supervised run with at most ten minutes,
twenty model turns and one in-flight action. These are proposed trial defaults,
not an additional human approval requirement or an ongoing exploration limit.
Set model usage/output caps in the chosen provider adapter before its first call.
Retain one bounded diagnostic log up to 10 MiB and one concise result; do not
record continuous video or make repeated world copies. Preserve existing worlds
and ordinary protection. The run must stop its own cognition and movement when
its bound expires; no boot enablement or unattended continuation is implied.

Resolve hosting from the current Shared Resources catalog and receiving capability
map before allocation. Check live capacity when selecting the host; older VPS
proposals are historical, and Mona is reserved for Harmonic Beacon. The selected
host, world, access route and retained local paths belong in receiving operations,
not public source. No new provider purchase is selected here.
