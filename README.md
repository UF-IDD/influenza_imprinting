# Data used in the manuscript _Assessing evidence of immune imprinting in serological patterns of influenza immune response_

Details on the data, the simulations, and the models that were fitted are given
in the ``Material and methods'' section in the manuscript.


## Fluscape HI titers

The columns in the dataset are as follows:
- `part_id`: Individual participant identifier.
- `part_age_at_sampling`: The age a participant had when the sample was taken.
- `part_age_at_isolation`: The age the participant would have had when the
  strain being tested was circulating.
- `part_gender`: The gender of the participant.
- `visit`: The visit during which a sample was taken, where
  - `V1`: 2009-2011;
  - `V2`: 2011-2012;
  - `V3`: 2013-2014;
  - `V4`: 2014-2015.
- `subtype_year`: The subtype (H3N2 or H1N1) and year the strain was
  circulating.
- `lab_round`: The samples were processed and analysed in three distinct rounds.
- `time_since_start`: The number of days elapsed starting from the first sample.
- `subtype_first_exposure`: The subtype a participant would have been likely
  first exposed to first early in life (non-probabilistic).
- `log2_HI_Titer`: The transformed inverse two-fold serial dilutions ($z$),
  where, if $x$ are the titers, $z = log_2(x / 5)$, and with $z = 0$ when titers
  were undetectable.


## Simulation output

For a more detailed description of the simulations, see Material and methods in
the manuscript. The columns in this dataset (`simulation_output.parquet`) are as
follows:
- `part_id`: Individual participant identifier.
- `model_iteration`: Identifier for the stochastic realization of the model (out
  of 100).
- `part_age_at_sampling`: The age a participant had when the sample was taken.
- `part_age_at_isolation`: The age the participant would have had when the
  strain being tested was circulating.
- `visit`: The visit during which a sample was taken (2004 and 2014).
- `strain_year`: The year the H3N2 strain was circulating (to match those
  available in the Fluscape data).
- `subtype_first_exposure`: The subtype a participant would have been likely
  first exposed to first early in life (non-probabilistic).
- `log2_HI_Titer`: The transformed inverse two-fold serial dilutions ($z$),
  where, if $x$ are the titers, $z = log_2(x / 5)$, and with $z = 0$ when titers
  were undetectable.

