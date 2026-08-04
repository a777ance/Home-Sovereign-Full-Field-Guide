# Home-Sovereign-Full-Field-Guide

Interactive, step-by-step guide to building a home DNS + ad-blocking stack —
Pi-hole (network-wide ad/tracker blocking) in front of Unbound (private,
DNSSEC-validated recursive resolution) — with optional WireGuard VPN and
Uptime Kuma monitoring blocks.

Fill in your router IP, box IP, and a couple other values once and every
command on the page updates to match, with copy buttons and a saved
progress checklist (stored only in your browser).

Published at **[a777ance.github.io/Home-Sovereign-Full-Field-Guide](https://a777ance.github.io/Home-Sovereign-Full-Field-Guide/)**
via GitHub Pages (`docs/index.html`, deployed by `.github/workflows/pages.yml`).

This is a standalone companion guide — a generalized version of the setup
documented in full at [a777ance/localdns](https://github.com/a777ance/localdns),
adapted so anyone can point it at their own house.

---

## After setup — changing your box later

This wizard gets you to a *first* working box. Once it's running, changing a config
on it (say, tightening Unbound's `interface:` to loopback) is a different job with its
own failure modes — a copy from a stale checkout that silently no-ops, a restart that
reloads the old file and still reports healthy. That per-change procedure — sync the
checkout → diff before overwrite → back up → validate → reload → verify the *effect* —
is written up in the reference stack's
**[Deploy Protocol](https://github.com/a777ance/localDNS/blob/main/docs/DEPLOY-PROTOCOL.md)**
(with the backlog of staged changes in its
[Deploy Queue](https://github.com/a777ance/localDNS/blob/main/docs/DEPLOY-QUEUE.md)).
It's written for that specific reference box, but the six phases carry over to any box
you build from this guide.

---

## 🌈 Bifrost

This repo runs on **[Bifrost](https://a777ance.github.io/localDNS/bifrost.html)** — the
A777ance keyboard-spatial command-composition schema, active from the first token of every
session. The canonical spec lives in the public `localDNS` repo.
