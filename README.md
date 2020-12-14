# Projects

#### Projects in classes are as follows.

| URLs | Description |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IRPLS-TensorGLR](https://github.com/hsongchoi/Projects/tree/master/IRPLS-TensorGLR) | Developed a Partial Least Squares (PLS) estimation for tensor generalized linear regression.  |
| [Spatial-prediction-on-Airbnb](https://github.com/hsongchoi/Projects/tree/master/Spatial-prediction-on-Airbnb) | Predicted the optimal price of Airbnb listings in New York City by using the spatial basis function model.  |
| [ovarian](https://github.com/hsongchoi/Projects/tree/master/ovarian) | Developed a new testing modality for an early detection of ovarian cancer. |
| [Intrinsic-values-of-movies](https://github.com/hsongchoi/Projects/tree/master/Intrinsic-values-of-movies) | Develped the model to estimate the movie rating before the movie is relased. |



## Index
* [Iteratively Reweighted PLS Estimation for Tensor Generalized Linear Regression](#Iteratively-Reweighted-PLS-Estimation-for-Tensor-Generalized-Linear-Regression)
* [Spatial Prediction on Airbnb in New York City](#Spatial-Prediction-on-Airbnb-in-New-York-City)
* [Assessment of Regularity in Protein mass spectra in Diagnostics of Ovarian cancer](#Assessment-of-Regularity-in-Protein-mass-spectra-in-Diagnostics-of-Ovarian-cancer)
* [Unearth the intrinsic value of movies](#Unearth-the-intrinsic-value-of-movies)

## Iteratively Reweighted PLS Estimation for Tensor Generalized Linear Regression
 * Here are the [Full Text](https://github.com/hsongchoi/Projects/blob/master/IRPLS-TensorGLR/Final_report.pdf) and the [Slides](https://github.com/hsongchoi/Projects/blob/master/IRPLS-TensorGLR/Slides.pdf) for the project.

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
  <img width="900" alt="ovarian" src="https://user-images.githubusercontent.com/68215937/102039544-080ad280-3d7f-11eb-8fa6-5e0d0a1e29db.PNG">
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
  <img width="800" alt="haar_filter" src="https://user-images.githubusercontent.com/68215937/102104514-1ee31080-3de3-11eb-87d1-166119f42154.PNG">
</p>

  * We achieved 90.6% accurate classification rate.
  * We conducted classification analysis based on the wavelet based log spectrum.
  * From the logistic classification model, we found that Hurst exponent has the ability to discriminate cancer and control subjects.
  * We can validate this method to find patterns of reproducible diagnostic value and contribute to the Ovarian cancer analysis.
  
  ## Unearth the intrinsic value of movies
  
  ### Background
  <br/>
<p align="center">
    <img width="600" alt="movierating" src="https://user-images.githubusercontent.com/68215937/102110431-00344800-3dea-11eb-8083-d96a872063d9.PNG">
  </p> 
  Movies are primarily a source of entertainment. In today’s busy world where people have limited time for entertainment, they should not be disappointed when they take out some time to watch a movie. Public and critics rates of movies as soon as they released help people to make a choice on the movie they want to watch. However, these ratings take time to stabilize. As soon as the movie releases, people who are film enthusiasts of the particular genre of the movie or the star cast usually rate it. Therefore, it is obvious that they tend to give a higher rating to the movie that skews the movie ratings. Among the critic-rating websites as well, the ratings of the movie keep changing until a large number of critics have rated it. This inspired us to address the problem of predicting the stabilized rating of a movie just before the movie is released.
  
  ### Data

  https://data.world/data-society/imdb-5000-movie-dataset  
  Dataset originally contains more than 5000 movies released from the year 1916 to 2016 in 66 countries. The data scientist who provided this data-set, conducted a scraping by using a Python library called “Scrapy”. Data-set contains many important movie information, scraped from IMDB website. (e.g. movie title, director, name, cast list, genres, name of actors etc).  
  Our purpose is to collect the data from as many movie reviewing websites as possible, so that we can get the bias of each websites and provide audiences with reliably estimated scores of unreleased movies on each websites. We randomly chose 30 out of 5000 movies, which were released since 2012, and collected ratings from 5 nation’s biggest movie reviewing websites: Rotten tomatoes (Audiences, Critiques), Flixter, Metacritic, MRQE, IMDB.  
  In order to build a regression model, we needed to introduce dummy variables to categorical variables like color, which indicates whether the movie is black or colored movie, genre, language, country, content_rating. Since there were no directors or actors, who shoot two or more different movies, out of our 30 selected movies, we did not take into account these factors while building regression model.
  
  ### Analysis
  * we built an EM model to find the bias of each movie rating groups and the “true” value of the movie.
  * We used this true value to develop an elastic net model, which enables us to estimate the “true” value of an unreleased movie.
  * We added the true value of the movie to the bias of the movie-rating group to predict the rating of the movie with respect to the corresponding group.
  * We estimated the rating of an unreleased movie with the following equation. We found true values of movies using the elastic-net model and obtained the bias of the rating-website using the EM algorithm.
  <br/>
<p align="center">
  <img width="1000" alt="equation" src="https://user-images.githubusercontent.com/68215937/102108819-3d97d600-3de8-11eb-88e4-3de3986eafae.PNG">
 </p>
 
  ### Conclusion
  * We infer that the audience is positively biased and tends to give a higher rating than critics do. This is evident from the high positive bias if IMDB and Rotten Tomatoes (Audience score) and negative bias of Rotten Tomatoes (Critic score) and Metacritic
  * The “true rating” of the movie is proportional to the average rating of all the reviewing websites which is consistent with our modeling assumptions
  * We estimate the true value of a movie from the elastic net model. Since the values of the covariates in the elastic net model are available before the movie is released and we already know the bias of each reviewing website, we can predict the rating of any movie on each of the nation’s top 5 reviewing website even before the movie is released.
  * The following table compares our estimated ratings with the actual ratings. We observed that our estimated ratings were close to the actual ratings on each of the reviewing websites. The average mean square error in our estimation was 0.47.
    <br/>
<p align="center">
  <img width="1317" alt="result_movie" src="https://user-images.githubusercontent.com/68215937/102109534-04139a80-3de9-11eb-8470-fc47c76e8100.PNG">
   </p>
