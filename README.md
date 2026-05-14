# Third Person HUD Map Pip Fix

Companion BepInEx plugin for Nuclear Option QoL.

When QoL's `thirdPersonHUD` option is enabled, the third-person HUD targeting pip can remain active while the map is open. This can cause one target-select input to select both a map target and a world target behind the map.

This plugin suppresses the third-person HUD/pip while the map is open, preventing accidental double target selection.

## Requirements

- Nuclear Option
- BepInEx 5
- QoL

## Tested behavior

- QoL `thirdPersonHUD = true`
- Third-person pip is suppressed while the map is open
- Map target selection still works
- No double target selection from the third-person pip behind the map

## Implementation hygiene

- No `Update()` loop
- No polling
- No timers
- No recurring scene scans
- No diagnostic file output
- Hook/event driven only

## Installation

Install through NOMM/NOMNOM when available, or manually place:

```text
ThirdPersonHudMapPipFix.dll
