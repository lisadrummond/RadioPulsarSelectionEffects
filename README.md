# RadioPulsarSelectionEffects: Pulsar population data release
*Data release accompanying our study of observational selection effects on the radio pulsar mass distribution.*

This directory contains the data products accompanying the paper 'Observational selection effects have a minimal impact on the radio pulsar mass', by Lisa V. Drummond, Katerina Chatziioannou and Emmanuel Fonseca. All data tables are text files with column names in the first commented line. The largest selection function table is a compressed text file.

## Contents

- `hyperposterior_samples/`: samples for the final population model, with and without selection effects.
- `selection_function/`: the full five-dimensional selection function and its one-dimensional selected fraction marginals.
- `individual_pulsar_posteriors/`: mass and inclination samples for each of the 46 pulsars.
- `example_usage.ipynb`: a simple notebook that loads and plots examples of the released data.

The hyperposterior columns use the notation of the paper. For pulsar mass, `mu_p_1` and `mu_p_2` are $\mu_{1,m_p}$ and $\mu_{2,m_p}$, the means of the two components; `sigma_p_1` and `sigma_p_2` are $\sigma_{1,m_p}$ and $\sigma_{2,m_p}$, their standard deviations; `f_p` is $f_{m_p}$, the fraction in the first component; and `mpop` is $M_{\mathrm{pop}}$, the upper mass cutoff. For companion mass, `mu_c_1`, `mu_c_2`, `sigma_c_1`, `sigma_c_2` and `f_c` are $\mu_{1,m_c}$, $\mu_{2,m_c}$, $\sigma_{1,m_c}$, $\sigma_{2,m_c}$ and $f_{m_c}$ with the corresponding meanings. For eccentricity, `sigma_e0` is $\sigma_{1,e}$, the standard deviation of the component with mean fixed at zero; `mu_e_2` and `sigma_e_2` are $\mu_{2,e}$ and $\sigma_{2,e}$, the mean and standard deviation of the second component; and `f_e0` is $f_e$, the fraction in the component with mean fixed at zero. For orbital period, `mu_log10_pb` and `sigma_log10_pb` are $\mu_{P_b}$ and $\sigma_{P_b}$, the mean and standard deviation of the Gaussian distribution in $\log_{10}(P_b/\mathrm{day})$. For spin period, `mu_log10_ps` and `sigma_log10_ps` are $\mu_{P_s}$ and $\sigma_{P_s}$, the mean and standard deviation of the Gaussian distribution in $\log_{10}(P_s/\mathrm{s})$. The `log_likelihood` and `log_prior` columns give the log likelihood and log prior for each sample.

The selection injections are uniform in pulsar mass, companion mass, eccentricity, `log10(Pb/day)`, and `log10(Ps/s)`. Each one-dimensional selected fraction marginal averages over the uniform injected distributions of the other four variables; it is not reweighted by the inferred population. The underlying injection run for the selection function contains 10^7 points; the release instead provides an easier to use binned version of the selection function.

Masses are in solar masses, inclinations are in degrees, orbital periods are in days, spin periods are in seconds, and logarithms are base 10. The individual posterior columns are `mp_msun`, `mc_msun`, and `inclination_deg`.
