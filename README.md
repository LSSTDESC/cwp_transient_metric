# TODO

## TODO 1:

We have simulated light curves with `kraken 2026`, `kraken 2044` and `nexus
2097` cadences in addition to the old baseline minion 1016.
We want to add `altsched` cadences from Daniel Rothschild.

## TODO 2:

We'll run each set of light curves through training + testing with
Daniel M's latest and greatest RNN + LSTM classifier.

## TODO 3:

The resulting output is safe for people involved in PLAsTiCC to play
with (provided models aren't identified).
We need Jupyter notebooks that take the output and:

a) for each of these cadences compare classification accuracy by class
to give a general sense of what science is helped and hurt by different
cadences

b) see if we can find approximate relationships between classification
accuracy per class and various properties of the cadence

## TODO 4:
Write. A lot. Fast.
