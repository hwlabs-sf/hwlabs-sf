### HW Labs — Independent AI/Python & Embedded Hardware Workbench

HW Labs is my one-person engineering practice, run out of Shenzhen. I write the
Python, lay out the board, bring the first prototype up on the bench, and ship
it. No agency layers, no account managers, no handoffs.

Two things, often in the same product:

**A — AI, RAG and Python automation.** Citation-grounded retrieval over tables
and documents, Playwright/HTTPX scrapers, PDF and CSV ETL, FastAPI back ends.
The kind of pipeline where every answer has to point at the cell it came from.

**B — 2–4 layer boards, MCU firmware, quick-turn prototypes.** KiCad schematic
and layout, STM32 / ESP32 / nRF52 and Verilog, JLC or Shenzhen PCBA in 7–14 days,
then bring-up on my own bench: rails, USB-UART console, peripheral-by-peripheral
functional checks, and a log you can read.

---

**What I take on**

| Discipline | What it covers |
| :--- | :--- |
| AI and data pipelines | RAG with citations back to the source cell or page, scrapers that survive layout changes, PDF/CSV ETL, FastAPI services, thin React front ends. |
| Product boards | 2–4 layer mixed-signal and power. STM32, ESP32, nRF52. USB-C PD, battery management, motor drive, sensor front ends. |
| Embedded firmware | Bare metal and RTOS. Field-oriented control, CAN-FD, BLE, LoRa. Bootloaders, DFU, production provisioning. |
| Bring-up and DFM | Stack-up, impedance, annular ring and solder mask checks, dual-source BOM, 7–14 day PCBA, first-article functional test with logs and photos. |

Fixed-scope pilots start small: a **$90–$290** scraper, RAG endpoint, or a 48-hour
KiCad DFM and schematic audit. Larger work is one page of scope, a fixed price,
and a date.

**Repositories**

- **[doc-table-rag-engine](https://github.com/hwlabs-sf/doc-table-rag-engine)** —
  citation-grounded retrieval over tables and key-value documents, in pure Python.
  Every answer comes back with the row it was read from, or it comes back empty.
- **[foc-canfd-joint-node](https://github.com/hwlabs-sf/foc-canfd-joint-node)** — a
  42 mm, 48 V / 15 A brushless joint controller for legged robots: STM32G431,
  DRV8323RS, six 1.45 mΩ FETs, Kelvin-sensed shunts, a 14-bit on-axis encoder,
  CAN-FD, and the field-oriented control firmware that runs it.
- **[sfp-10g-bert-pocket](https://github.com/hwlabs-sf/sfp-10g-bert-pocket)** — a
  10.3125 Gbit/s SFP+ bit-error-rate tester: 64-bit parallel PRBS-31 in Verilog, an
  SFF-8472 poller over I2C, a four-layer AC-coupled carrier, and a host CLI that
  turns diagnostic bytes into dBm.
- **[kicad-dfm-precheck](https://github.com/hwlabs-sf/kicad-dfm-precheck)** — the
  linter I run before every fab release: a pure-Python KiCad S-expression checker
  for thin annular rings, placeholder part values, and pins left on
  `unconnected-*` nets.

The Python tools run on the standard library alone. `python -m unittest` inside
any of them, no install step.

Client production boards stay under mutual NDA, so what is public here is
representative reference designs and the tooling I use on every board — not
customer work.

**How I work**

- One page of scope, a fixed price, a date. No retainers.
- Every claim in a report has a measurement behind it: a log line, a meter
  reading, a photo of the fixture. If I did not measure it, I say so.
- What I hand over is what you can rebuild from: sources, not just outputs.
- I am in UTC+8 and answer in writing within one business day.

**Contact** — [hello@hengwu.online](mailto:hello@hengwu.online) · [hengwu.online/labs](https://hengwu.online/labs/)

---

**Projects and tooling I follow**

Work by other people that I use, read, or learn from. None of it is mine.

- [LimesKey/parsnip-node](https://github.com/LimesKey/parsnip-node) — a compact USB-C node; the kind
  of board where every millimetre of the stack-up is a decision.
- [greatscottgadgets/amalthea](https://github.com/greatscottgadgets/amalthea) — open hardware done
  properly: schematics, layout, and the reasoning published together.
- [KooroshTorabi/ina228-current-profiler](https://github.com/KooroshTorabi/ina228-current-profiler) —
  low-side current profiling with a part that deserves more use than it gets.
- [romixlab/better_erc](https://github.com/romixlab/better_erc) — a sharper electrical rules check
  for KiCad; useful because ERC catches what you told it to catch, and nothing else.
- [emilkowalski/skills](https://github.com/emilkowalski/skills) — interface craft notes. I build
  instruments, not landing pages, but the discipline about detail transfers.

<sub>Shenzhen, China · UTC+8 · <a href="https://hengwu.online/labs/">hengwu.online/labs</a></sub>
