# Projects

#### Projects in classes are as follows.

| URLs | Description |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Spatial-prediction-on-Airbnb](https://github.com/hsongchoi/Projects/tree/master/Spatial-prediction-on-Airbnb) | Predicted the optimal price of Airbnb listings in New York City by using the spatial basis function model.  |
| [ovarian](https://github.com/hsongchoi/Projects/tree/master/ovarian) | Developed a new testing modality for an early detection of ovarian cancer. |
| [Intrinsic-values-of-movies](https://github.com/hsongchoi/Projects/tree/master/Intrinsic-values-of-movies) | Develped the model to estimate the movie rating before the movie is relased. |



## Index

* [Spatial Prediction on Airbnb in New York City](#Spatial-Prediction-on-Airbnb-in-New-York-City)
* [Assessment of Regularity in Protein mass spectra in Diagnostics of Ovarian cancer](#Assessment-of-Regularity-in-Protein-mass-spectra-in-Diagnostics-of-Ovarian-cancer)
* [Unearth the intrinsic value of movies](#movies)


## Spatial Prediction on Airbnb in New York City

<br/>
<p align="center">
  <img width="600" alt="Price_NYC" src="https://user-images.githubusercontent.com/68215937/102038266-a85ef800-3d7b-11eb-9a61-a019d82389c8.PNG">
</p>

 * Predicted the optimal price of Airbnb listings in New York City by applying the spatial basis function model.
 * Compared MSE of our method with that of simple, Ridge, and Lasso regression.
 * Verified how the spatial basis function expansion is accurate for the prediction of the price of Airbnb. 

## Assessment of Regularity in Protein mass spectra in Diagnostics of Ovarian cancer

<br/>
<p align="center">
  <img width="1211" alt="ovarian" src="https://user-images.githubusercontent.com/68215937/102039544-080ad280-3d7f-11eb-8fa6-5e0d0a1e29db.PNG">
</p>

Using wavelet-based tools, we developed a new testing modality for an early detection of ovarian cancer.

### Background
  * Unlike other cancers, mortality rates for OC have declined only slightly since 1971 because of the unavailability of early detection tests and treatments.
  * Only 15 percent of ovarian cancer patients are diagnosed early.

### Data
  * 162 O varian cancer(OC) patients and 91 Control subjects
  * Protein mass spectral data obtained by PBSII SELDI-TOF mass spectrometer
    * Intensities at distinct M/Z values (the range of M/Z: 0.0000786 to 19995.513)
    * Only intensity data from 4001 to 13001 were used.

### Analysis
  * Using Wavelet based log spectrum with a specific filter, we estimated the slopes for <img src="https://latex.codecogs.com/gif.latex?2^{10}" />  data packet.
  
