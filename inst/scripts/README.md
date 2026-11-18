# Test data in `inst/testdata`

All files in `inst/testdata` are synthetic and are used by the examples, the unit tests and the
vignette. They are distributed under the package license, Artistic-2.0.

## DepMap-format tables and association results

`Model.csv`, `CRISPRGeneEffect.csv`, `OmicsSomaticMutationsMatrixHotspot.csv`,
`OmicsSignaturesProfile.csv`, `OmicsArmLevelCNA.csv` and the `tab_assoc_*.xlsx` files are
generated with a fixed seed by `PRISM_test_data.R`. They follow the layout of DepMap releases
but contain no DepMap data: cell lines come from `gDRtestData::create_synthetic_cell_lines()`
and features and values are random.

## Chemical genomics synthetic data

`cgs_data.qs2` is a synthetic table of GR and RV drug response metrics for a chemical genomics
screen: several hundred drugs, alone and co-treated with one anchor drug, in two cell lines. It
is used to test `analyze_cgs()` and `plot_cgs_ranking()`. Identifiers are placeholders
(`DrugName_<n>`, `drug_moa_<n>`, `CellLineName_<n>`, `Tissue_1`). The table was created by hand
for the tests, without a generating script.
