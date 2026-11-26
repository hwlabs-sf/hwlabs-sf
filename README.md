### HW Labs Engineering

A small hardware lab in Shenzhen. We do FPGA bring-up, board design, firmware, and the bench
that proves a board works before it ships.

Most of our work is the unglamorous part: a differential pair that rings at 3.1 GHz, a buck
converter that drops out at cold start, a ring network that recovers but settles one round late.
We like problems that have a measurement attached.

---

**What we do**

| Discipline | What it covers |
| :--- | :--- |
| FPGA & high-speed I/O | Multi-gigabit serial links, SFP+ optics, custom framing, timing closure, on-board capture |
| Board design & DFM | Schematic to fab package, stack-up, impedance, annular ring and solder-mask checks, dual-source BOM |
| Firmware & test benches | Bare-metal and RTOS firmware, pogo-pin fixtures, automated bring-up scripts, pass/fail logs a customer can read |
| Failure analysis | Root-cause a dead board or a flaky link, then hand over the measurement that shows the fix |

Engagements are fixed-scope. A DFM + dual-source BOM audit is **$690**, credited in full against
production if the build goes ahead within 30 days.

**Repositories**

- **[fpga-optical-ring-bench](https://github.com/hwlabs-sf/fpga-optical-ring-bench)** — a sanitized
  case study of a 10.3125 Gbps bidirectional redundant optical ring on an FPGA (1 master, 3 slaves),
  plus `ring_audit.py`, a small CLI that checks A/B sequence continuity and slot accounting in the
  master's telemetry.
- **[kicad-dfm-precheck](https://github.com/hwlabs-sf/kicad-dfm-precheck)** — a pure-Python KiCad
  S-expression linter that catches thin via annular rings, placeholder part values, and pins left on
  `unconnected-*` nets before the boards are ordered.

Both run on the standard library alone. `python -m unittest` in either directory, no install step.

**How we work**

- One page of scope, a fixed price, and a date. No retainers.
- Every claim in a report has a measurement behind it: a scope capture, a log line, a photo of the
  fixture. If we did not measure it, we say so.
- Files we hand over are the ones you can rebuild from: sources, not just outputs.
- We are in UTC+8 and answer within one business day.

**Contact** — [hello@hengwu.online](mailto:hello@hengwu.online) · [hengwu.online/labs](https://hengwu.online/labs/)

---

**Projects and tooling we follow**

Work by other people that we use, read, or learn from. None of it is ours.

- [LimesKey/parsnip-node](https://github.com/LimesKey/parsnip-node) — a compact USB-C node; the kind
  of board where every millimetre of the stack-up is a decision.
- [greatscottgadgets/amalthea](https://github.com/greatscottgadgets/amalthea) — open hardware done
  properly: schematics, layout, and the reasoning published together.
- [KooroshTorabi/ina228-current-profiler](https://github.com/KooroshTorabi/ina228-current-profiler) —
  low-side current profiling with a part that deserves more use than it gets.
- [romixlab/better_erc](https://github.com/romixlab/better_erc) — a sharper electrical rules check
  for KiCad; useful because ERC catches what you told it to catch, and nothing else.
- [emilkowalski/skills](https://github.com/emilkowalski/skills) — interface craft notes. We build
  instruments, not landing pages, but the discipline about detail transfers.

<sub>Shenzhen, China · UTC+8 · <a href="https://hengwu.online/labs/">hengwu.online/labs</a></sub>
