# Ares OS
> Ares - Greek god of war, bloodshed, and violence and son of Zeus and Hera.

## Features

* nix* style architecture
* Supports 8 devices wired directly and up to 64 hot-pluggable devices using extended address busses
* Multitasking via process manager
* In-memory virtual filesystem
  * Mountable
    * Server files
    * Physical storage devices: DHDD, EEPROM, CD, RAM
  * Boot information under `/boot`
  * System information under `/sys`
  * Device information under `/dev`
  * Process information under `/proc`

## Boot process

* Create initial RAM disk (in-memory virtual filesystem)
* Mount
* Run the initial executable
