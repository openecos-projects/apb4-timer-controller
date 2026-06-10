# ip-000006

Display name: APB4 Timer Controller

UID: ip-000006

Family: timer

Category: peripheral

Repository: git@github.com:openecos-projects/apb4-timer-controller.git

Upstream: https://github.com/oscc-ip/timer

Upstream author/maintainer: Beijing Institute of Open Source Chip / OSCC-IP

Current baseline: source snapshot from the `20250627` tapeout project

License: MulanPSL-2.0, with selected files carrying Solderpad Hardware License 0.51 provenance notices where present

Status: candidate, silicon-proven source snapshot

This repository is managed as a child repository of `ip-catalog`.

## Summary

APB4-based programmable timer with prescaler, 32-bit counter and compare register, auto reload, capture mode, and overflow interrupt.

The local repository contains a source mirror from the `20250627` tapeout
project for catalog evaluation. The current RTL baseline should be treated as
the tapeout project source snapshot rather than an automatically synchronized
upstream checkout.

## Layout

```text
rtl/       SystemVerilog RTL and required local common support modules
tb/        SystemVerilog testbench files
model/     Simulation models, when present
driver/    Minimal C software access examples, when present
docs/      Datasheet and provenance notes
reports/   Review, lint, simulation, or synthesis report summaries
```

## Top Level

The integration top module is:

```text
apb4_tmr
```

Top-level interfaces:

```text
apb4_if.slave apb4; tmr_if.dut tmr
```

## Catalog Mapping

The corresponding catalog record is expected at:

```text
data/ip/peripheral/ip-000006.yaml
```

The local metadata source is:

```text
ip.yaml
```

## Review Notes

- Upstream repository: https://github.com/oscc-ip/timer
- Upstream default branch observed locally: `main`
- Current source snapshot comes from the `20250627` tapeout project code.
- IP status is recorded as silicon-proven based on the provided tapeout project provenance.
- Common support modules required by the IP have been copied into `rtl/` for standalone catalog review.
- No local passing simulation, lint, synthesis, coverage, or silicon validation report artifact has been added yet.
