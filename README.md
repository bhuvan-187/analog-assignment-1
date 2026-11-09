# Design and Simulation of a Common Source MOSFET Amplifier

Open index.html in a modern browser. The interactive graphs use Chart.js from jsDelivr, so an internet connection is needed to load the plotting library. No build step or local server is required.

## Included

- Responsive engineering dashboard with SVG circuit diagram
- Adjustable sine source amplitude and frequency
- Transient input and output plots
- Nonlinear NMOS square-law current model in saturation and triode
- DC operating point, transconductance, signed small-signal gain, gain in dB, and phase
- Small-signal frequency response with CS enabled and disabled
- Interactive source bypass control and reset

## Model assumptions

The parameter Kn is treated as the square-law coefficient beta = 40 mA/V², with ID = beta/2 · (VGS − VTH)² in saturation. The transient model also uses the corresponding triode-region equation. Channel-length modulation, body effect, gate current, device capacitances, temperature, and noise are omitted.

Values not specified in the project brief are set to C1 = 10 µF, C2 = 10 µF, CS = 100 µF, Rsig = 600 Ω, and RL = 1 MΩ. The waveform solver integrates the coupling and bypass capacitor states and solves the nonlinear drain/source equations at each time step. The frequency-response plot is a small-signal estimate around the DC operating point.

