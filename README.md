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
  * Log spectrums are regularly decreasing after dyadic level 5.
  * After obtaining the Hurst exponents matrix, we calculated the absolute difference of means between Cancer and Control case.
  * We ran a logistic regression with 10 variables selected based on the absolute difference.
  * We randomly selected 67% of the data as a training data in order to create a classifier. Then we used the remaining 33% of the data to test performance.
  * We fitted a logistic regression model on training data and classified the test data 1000 times.
  * Additionally, we tested whether the true responses (Cancer:1 and Control:0) are same as the fitted values through the Wilcoxon Sum Rank procedure 1000 times.
  * We also tested We tested 5 filter with 1000 steps, and chose the Haar filter.
  
### Conclusion
<br/>
<p align="center">
  <img width="1171" alt="haar_filter" src="https://user-images.githubusercontent.com/68215937/102104514-1ee31080-3de3-11eb-87d1-166119f42154.PNG">
</p>

  * We achieved 90.6% accurate classification rate.
  * We conducted classification analysis based on the wavelet based log spectrum.
  * From the logistic classification model, we found that Hurst exponent has the ability to discriminate cancer and control subjects.

