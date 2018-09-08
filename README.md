# Mark III

An API for creating Wiremod Expression 2 operating systems.

The Mark III comes with a simple BIOS, Eos, which initializes the system, runs a POST, and runs a
default executable which by default is Ares, a simple `*nix`-like OS.

See `usr/share/doc` for more documentation.

## Graph

```
      I/O devices
           ▲
  ┌────────│──── API ──────────────┐
  │        ▼                       │
  │ Kernel Functions ◀──▶ Drivers │
  │     ▲        ▲                 │
  │     │        │                 │
  │     │        ▼                 │
  │     │   Event System           │
  │     │        ▲                 │
  └─────│────────│─────────────────┘
        ▼        ▼
  Firmware (BIOS, OS, Boot loader)
```
