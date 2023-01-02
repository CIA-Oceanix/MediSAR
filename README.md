# MediSAR

## Links

- MediSAR-2014 - NYA
- [MediSAR-2015](www.kaggle.com/rignak/medisar2015)
- MediSAR-2016 - NYA
- MediSAR-2017 - NYA
- MediSAR-2018 - NYA
- MediSAR-2019 - NYA
- MediSAR-2020 - NYA
- MediSAR-2021 - NYA
- MediSAR-2022 - NYA
- MSG/SEVIRIS collocations
- Sentinel3/OLCI collocations

## Summary

MediSAR is a extensive dataset of Synthetic Aperture Radar (SAR) observations of the Mediterranean Sea. It contains all the Interferometric Wide (IW) observations acquired by the Sentinel-1 satellites from the ESA mission Copernicus.

SAR observation are affected by the sea surface roughness. Several meteorological and oceanic processes impact this sea surface roughness: it increases with the wind speed or the hydrometeors, but decrease in presence of biological surfactant such as oil pollution or biofilm. Therefore, it is possible to infer these processes from the SAR observation.

## Content

This dataset contains data from 2014 to 2022, both included. Due to size limitation, a kaggle dataset is provided for each year. Each IW product is contains in a folder `{YYYY}/{YYYY}-{MM}-{DD}/{YYYY}{MM}{DD}t{hh}{mm}{ss}`. These folders contains:

- The SAR observations of co- (vv) and cross- (vh) polarization channels. Downscaled at 200 m/px and stored as uint16.
- The rain estimation, as four-class segmentation roughly based on 1 mm/h, 3 mm/h and 10 mm/h. These segmentations are described in [10.48550/ARXIV.2207.07333](https://arxiv.org/abs/2207.07333). There are stored at 400 m/px on four channels, the transparency corresponding to the land mask.
- The biological slicks, as a binary image at 200 m/px.
- The convective cells, as uint3 image at 400 m/px.

## Notebooks

- Search file on given lat/lon coordinates.
- Aggregate the observations for seasonal comparison.

## Changelog

**2023-01-01:** First upload. 

## Roadmap

- Upload of years 2014, 2016, 2017, 2018, 2019, 2021 & 2022.
- S3 OLCI colocalizations for ocean colour.
- Wind estimation with rain-invariant model.
