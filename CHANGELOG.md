# Changelog
All notable changes to this project are relative to version 0.1.0 and will be documented in this file.

## [Unreleased]
## [0.2.0] - 2022-10-07


### Changed - indexes used are from v0.2
- changed opamps to MCP6004 and MCP6002 as low power, low voltage, rail-to-rail, MOSFET-input opamps
- changed R102 from 10kΩ to 7kΩ for wider duty-cycle range
- changed C201 from 20nF to 1µF for lower pitch
- changed C202 from 100nF to 22nF for lower influence to the pitch
- changed R203 from 10kΩ to 1MΩ for pushing the cutoff of the high-pass filter down
- changed R501 from 2kΩ to 10kΩ for -21dB attenuation for equal perceived loudness of triangle and rectangle
- changed RV501 to logarithmic scale for exponential sweep from triangle to rectangle
- changed RV601 to logarithmic scale for organic sweep in frequency cutoff


### Added - indexes used are from v0.2
- added pull down resistor R301 due to input capacity of the opamp
- added buffer cap C401 for stability of VDD/2
- added clipped non-inverting amplifier to feedback of the main filter for limited feedback and sound improvement
- added whole power amplifier and line-out section (section 7xx) with volume knob, a small power amplifier for a small on-board speaker and buffered line-out with nominal output impedance


### Removed
- pulldown resistor R31