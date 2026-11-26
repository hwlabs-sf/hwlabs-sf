### HW Labs Engineering

A hardware studio in Shenzhen. We take a product from schematic to a unit that
passes test: the board, the firmware on it, and the bench that proves it.

Most of the work is the unglamorous part. A buck converter that drops out at cold
start, a CAN bus that loses arbitration under load, a pogo fixture that fails a
good board because one probe wore through. We like problems that have a
measurement attached.

---

**What we do**

| Discipline | What it covers |
| :--- | :--- |
| Product boards | 2–8 layer mixed-signal, power and RF. STM32, ESP32, nRF52, FPGA. USB-C PD, battery management, motor drive, sensor front ends. |
| Embedded firmware | Bare metal and RTOS. Field-oriented control, CAN-FD, BLE, LoRa, Wi-Fi. Bootloaders, DFU, production provisioning and calibration. |
| Factory test | Pogo-pin fixtures, automated bring-up, per-unit pass/fail logs a line operator can read, burn-in and end-of-line calibration. |
| DFM and sourcing | Stack-up, impedance, annular ring and solder mask checks, dual-source BOM, 7–14 day PCBA in Shenzhen. |

Engagements are fixed-scope. A DFM + dual-source BOM audit is **$690**, credited in
full against production if the build goes ahead within 30 days.

**Repositories**

- **[foc-canfd-joint-node](https://github.com/hwlabs-sf/foc-canfd-joint-node)** — a 42 mm,
  48 V / 15 A brushless joint controller for humanoid and legged robots: STM32G431, DRV8323RS,
  six 1.45 mΩ FETs, Kelvin-sensed shunts, a 14-bit on-axis encoder, CAN-FD, and the field-oriented
  control firmware that runs it.
- **[sfp-10g-bert-pocket](https://github.com/hwlabs-sf/sfp-10g-bert-pocket)** — a
  10.3125 Gbit/s SFP+ bit-error-rate tester: 64-bit parallel PRBS-31 in Verilog, an
  SFF-8472 poller over I2C, a four-layer AC-coupled carrier, and a host CLI that
  turns diagnostic bytes into dBm. Both RTL testbenches and the DFM check run in
  the test suite.
- **[kicad-dfm-precheck](https://github.com/hwlabs-sf/kicad-dfm-precheck)** — the
  linter we run before every fab release: a pure-Python KiCad S-expression checker
  for thin annular rings, placeholder part values, and pins left on
  `unconnected-*` nets.

The Python tools run on the standard library alone. `python -m unittest` inside
any of them, no install step.

Client production boards stay under mutual NDA, so what is public here is
representative reference designs and the tooling we use on every board — not
customer work. Ask and we will walk you through the relevant one on a call.

**How we work**

- One page of scope, a fixed price, and a date. No retainers.
- Every claim in a report has a measurement behind it: a scope capture, a log line,
  a photo of the fixture. If we did not measure it, we say so.
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
