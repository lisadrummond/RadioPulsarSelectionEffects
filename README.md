# RadioPulsarSelectionEffects: Pulsar population data release
*Data release accompanying our study of observational selection effects on the radio pulsar mass distribution.*

This directory contains the data products accompanying the paper 'Observational selection effects have a minimal impact on the radio pulsar mass', by Lisa V. Drummond, Katerina Chatziioannou and Emmanuel Fonseca. All data tables are text files with column names in the first commented line. The largest selection function table is a compressed text file.

## Contents

- `hyperposterior_samples/`: samples for the final population model, with and without selection effects.
- `selection_function/`: the full five-dimensional selection function and its one-dimensional selection fraction marginals.
- `individual_pulsar_posteriors/`: mass and inclination samples for each of the 46 pulsars.
- `example_usage.ipynb`: a simple notebook that loads and plots examples of the released data.

Masses are in solar masses, inclinations are in degrees, orbital periods are in days, spin periods are in seconds, and logarithms are base 10. The individual posterior columns are `mp_msun`, `mc_msun`, and `inclination_deg`.

The selection injections are uniform in pulsar mass, companion mass, eccentricity, `log10(Pb/day)`, and `log10(Ps/s)`. Each one-dimensional selected-fraction marginal averages over the uniform injected distributions of the other four variables; it is not reweighted by the inferred population.

The selection grid contains 38 pulsar-mass bins, 36 companion-mass bins, 36 eccentricity bins, 36 log-orbital-period bins, and 24 log-spin-period bins.

The underlying injection run for the selection function contains 10^7 points; the release instead provides an easier to use binned version of the selection function.
