# BasinOS Agentic Layer

**Agentifying a live data twin of the Permian Basin.**

[BasinOS](https://basinos.ignisalgos.com) is a live digital twin of the Odessa–Midland /
Permian Basin region fusing roughly 60 public data feeds: ERCOT grid conditions,
National Weather Service data, air-quality sensors, oilfield activity, earthquakes,
flights, and more.

This repository holds **only the open-source agentic layer** built on top of BasinOS
for the [Open Agentic Web Challenge](https://cognizant-agenticweb.devpost.com/)
(Devpost, submissions close January 11, 2027). BasinOS itself remains private;
everything in this repo is the public layer the challenge requires.

## What this layer does

Following the Open Agentic Web minimum viable specification
([cognizant-ai-labs/agentic-web](https://github.com/cognizant-ai-labs/agentic-web)):

- `agent-manifest.json` — publicly accessible manifest describing the agent network
  and its capabilities, so other agentic websites can discover and call it.
- `basinos.network.json` — the agent network, described in JSON (not code):
  a coordinator plus specialist agents — **grid**, **weather**, **field**, **air** —
  that confer on plain-language questions and ground every answer in live BasinOS
  feed data.
- `runtime/` — the browser runtime that runs the network in the visitor's browser
  (to be vendored from the spec's agentify-website runtime during the build).
- An interaction interface where users (and other agents) talk to the network,
  with an LLM/key configuration panel — visitors bring their own keys, so the
  host pays nothing for inference.

Example questions the network is being built to answer:

- "Is the grid stressed right now, and is weather making it worse?"
- "What's the air like near the drilling activity west of Midland today?"
- "Anything unusual happening in the Basin this morning?"

## Status

In build. Skeleton published for hackathon registration; the network, runtime
wiring and live-data tools land incrementally ahead of the January 11, 2027
deadline.

## License

Apache License 2.0 — see [LICENSE](LICENSE).

## Who

Built by Ignis Algos, Odessa, Texas.
