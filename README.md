# The great multivariate time series classification bake off

Results for the paper "The great multivariate time series classification bake off: a
review and experimental evaluation of recent algorithmic advances" published in Data
Mining and Knowledge Discovery, which compares multivariate time series classification
algorithms on 26 equal length datasets from the UEA archive.

The paper is open access and available from
[Springer](https://doi.org/10.1007/s10618-020-00727-3).

## Contents

| Path | Description |
|---|---|
| [results](results) | Test accuracy of 12 classifiers on the 26 UEA datasets (Figures 7, 8, 9 and 11) |

Each `<classifier>_TESTFOLDS.csv` file has one row per dataset and one column per
resample, with 30 resamples in total. Resample 0 is the default train/test split.
`DTW_I`, `DTW_D` and `DTW_A` are the independent, dependent and adaptive versions of
1-nearest neighbour DTW, and `HIVE-COTEv1` is HIVE-COTE. The results for the classifiers
only in Figure 12 (InceptionTime, MUSE, TapNet and MrSEQL) are not included.

## Datasets

The 26 equal length multivariate datasets are from the
[UEA Multivariate Time Series Classification Archive](https://www.timeseriesclassification.com/dataset.php).
More information on the datasets is available at
[timeseriesclassification.com](http://www.timeseriesclassification.com).

## Running the classifiers

The paper used the Java implementations in the
[tsml](https://github.com/time-series-machine-learning/tsml-java) toolkit where
possible, and Python implementations in `sktime` otherwise. Table 2 of the paper lists
where each classifier is implemented, and Sections 4.1 and 4.2 describe how to run them.

Most of the classifiers are now available in the
[aeon](https://github.com/aeon-toolkit/aeon) Python package, which follows the
`scikit-learn` interface, i.e. `RocketClassifier`, `HIVECOTEV1`,
`CanonicalIntervalForestClassifier`, `ResNetClassifier`,
`ShapeletTransformClassifier` and `KNeighborsTimeSeriesClassifier`.

## Citation

If you use this work, please cite the paper:

```bibtex
@article{ruiz2021great,
  title={The great multivariate time series classification bake off: a review and experimental evaluation of recent algorithmic advances},
  author={Ruiz, Alejandro Pasos and Flynn, Michael and Large, James and Middlehurst, Matthew and Bagnall, Anthony},
  journal={Data Mining and Knowledge Discovery},
  volume={35},
  number={2},
  pages={401--449},
  year={2021},
  publisher={Springer},
  doi={10.1007/s10618-020-00727-3}
}
```

## Contact

For questions about the paper or this repository, feel free to email the authors or
contact us on the [aeon Discord](https://discord.gg/D6rzqHGKRJ).
