# Earthquake-prediction-using-Machine-learning-models

A project done for the course CSE3505 - Essentials of Data Analytics under <b>ELANGO N M</b>
<h3>Team members</h3>
<ul>
<li><b>AKASH R 20BCE1501</b> Github: <a href="https://github.com/akash-r34">akash-r34</a></li>
<li><b>ARJUN BHARANI 20BCE1505</b> Github: <a href="https://github.com/ArjunBharani">ArjunBharani</a></li>
<li><b>SHIVAM SHARMA 20BCE1442</b> Github: <a href="https://github.com/shivams-23">shivams-23</a></li>
<li><b>AKSHAY GIRISH 20BCE1573</b> Github: <a href="https://github.com/Akshaykviit023">Akshaykviit023</a></li>
</ul>
<h2>Abstract</h2>
Earthquakes are natural disasters that can cause significant damage and loss of life. Accurate prediction of earthquakes is essential for developing early warning systems, disaster planning, risk assessment, and scientific research.
This project aims to predict the magnitude and probability of Earthquake occurring in a particular region from the historic data of that region using various Machine learning models.

<h2>Dataset</h2>
The dataset used in this project is called the "SOCR Earthquake Dataset," and it contains information about earthquakes that have occurred with a magnitude of 3.0 or greater worldwide.

Each row in the dataset represents a single earthquake event and includes the following information:

<ul>
<li>Date and time of the earthquake in UTC (Coordinated Universal Time)</li>
<li>Latitude and longitude(in degree) of the epicenter, which is the point on the Earth's surface directly above where the earthquake occurred</li>
<li>Depth of the earthquake, measured in kilometers</li>
<li>Magnitude of the earthquake on the Richter scale</li>
<li>SRC = source</li>
<li>nst - number of stations used for solution (range: 0 to ...)</li>
<li>close - distance of closest station to epicenter (range: 0 to ...)</li>
<li>rms - root-mean-squared residual of solution (range: 0. to 1.)</li>
<li>gap - azimuthal gap (range: 0 to 360)</li>
</ul>

The Richter scale is a logarithmic scale that measures the magnitude of an earthquake based on the energy released by the earthquake. Each increase of one unit on the Richter scale represents a tenfold increase in the amplitude of the seismic waves generated by the earthquake.<br>

The dataset contains earthquake events from January 2, 2017, to December 31, 2019, which includes a total of 37,706 earthquakes. This dataset could be used for a variety of purposes, such as studying earthquake patterns and trends over time or for predicting future earthquake activity

<h2>Introduction</h2>
The SOCR Earthquake Dataset can be used to build machine learning models to predict earthquakes or to better understand earthquake patterns and characteristics. Here are a few possible ways machine learning models can be used with this dataset:
<br>
<br>
<ol>
<li>Earthquake prediction: You can use this dataset to build a model that predicts when and where an earthquake might occur based on past earthquake data. You could use techniques such as time series analysis, clustering, or classification to identify patterns in the data and make predictions.</li>

<li>Magnitude prediction: You can use this dataset to build a model that predicts the magnitude of an earthquake based on other factors such as location, depth, or the number of seismic stations that recorded the earthquake. You could use regression techniques to build this model.</li>

<li>Risk assessment: You can use this dataset to identify areas that are at higher risk of earthquakes based on historical earthquake data. You could use clustering or classification techniques to identify patterns in the data and identify areas with similar characteristics.</li>

<li>Anomaly detection: You can use this dataset to detect anomalies or outliers in the data, which could represent earthquakes that are unusual or unexpected. You could use techniques such as clustering or classification to identify patterns in the data and detect anomalies.</li>

<li>Data visualization: You can use this dataset to create visualizations of earthquake data, which could help you identify patterns and relationships in the data. You could use techniques such as scatter plots, heat maps, or geographic information systems (GIS) to visualize the data.</li>
</ol>
<br>
These are just a few examples of the many ways that machine learning models can be used with the SOCR Earthquake Dataset. The specific approach you take will depend on your research question and the goals of your analysis. In this project we focus mainly on Earthquake prediction and Magnitude prediction.
<br>
<h2>Class diagram</h2>
<div align="center">
<img src="https://user-images.githubusercontent.com/113085803/229195883-8aec511d-0e24-46c4-8cd2-67e4bdfb759c.png"/>
</div>
<h2>Data visualization</h2>
Software used: <b>Tableau</b>
<br>
<br>
<div align="center">
  <img src="https://user-images.githubusercontent.com/113085803/229277065-c75d240b-1b1c-4a42-a43a-53311275cdf0.png"/><br>
  <b><i>Figure 1<br> Earthquake (identified by Event ID) and the number of stations recording it</i></b>
  <br>
  <br>

  <img src="https://user-images.githubusercontent.com/113085803/229278389-8b9951d6-a06b-4316-bed9-fa220b5170a8.png"/>
  <b><i>Figure 2<br>Earthquake based on its magnitude</i></b>
  <br>
  <br>
  
  <img src="https://user-images.githubusercontent.com/113085803/229277078-5e2a9ab0-10af-43f6-a862-7727770659ec.png"/>
  <b><i>Figure 3<br>EEarthquake based on its magnitude type</i></b>
  <br>
  <br>
  
  <img alt ="[Earthquake magnitude and depth over the years]"
       src="https://user-images.githubusercontent.com/113085803/229277278-88821402-2d5d-4beb-8644-e2b0b9bd73c0.png"/>
  <b><i>Figure 4<br>Earthquake magnitude and depth over the years</i></b>
  <br>
  <br>
</div>

<h2>Implementation</h2>
We will use four models in this project:
<ol>
<li>Linear regression</li>
<li>Support Vector Machine(SVM)</li>
<li>NaiveBayes</li>
<li>Random Forest</li>

</ol>
<h3>Linear Regression</h3>
<p>Linear regression is a type of supervised machine learning algorithm that is used to model the linear relationship between a dependent variable (in this case, earthquake magnitude) and one or more independent variables (in this case, latitude, longitude, depth, and the number of seismic stations that recorded the earthquake).</p>

<p>The basic idea behind linear regression is to find the line of best fit through the data that minimizes the sum of the squared residuals (the difference between the predicted and actual values of the dependent variable). The coefficients of the line of best fit are estimated using a method called ordinary least squares, which involves minimizing the sum of the squared residuals with respect to the coefficients.</p>

<p>In this situation, we have used multiple linear regression to model the relationship between earthquake magnitude and latitude, longitude, depth, and the number of seismic stations that recorded the earthquake. The multiple linear regression model assumes that there is a linear relationship between the dependent variable (magnitude) and each of the independent variables (latitude, longitude, depth, and number of seismic stations), and that the relationship is additive (i.e., the effect of each independent variable on the dependent variable is independent of the other independent variables).</p>

<p>Once the model has been fit to the data, we can use it to predict the magnitude of a new earthquake given its latitude, longitude, depth, and the number of seismic stations that recorded it. This can be useful for earthquake monitoring and early warning systems, as well as for understanding the underlying causes of earthquakes and improving our ability to predict them in the future.</p>

<div align="center">
<img src="https://user-images.githubusercontent.com/113085803/229284656-286a3290-3c96-4929-ae31-761456cbc3e4.png"><br>
<b><i>Figure 5<br>Multiple linear regression plot using seaborn library(python)</i></b>
 <br>
 <br>
</div>

<p>The linear regression equation used in our multiple linear regression model for earthquake magnitude prediction with latitude, longitude, depth, and number of seismic stations as independent variables can be written as:</p>

<p>Magnitude = -0.6028 * Latitude + 1.2012 * Longitude - 0.0008 * Depth + 0.0239 * No_of_stations + 0.1573</p>

<p>Where:</p>
<ul>
<li>Magnitude is the dependent variable, representing the magnitude of the earthquake</li>
<li>Latitude, Longitude, Depth, and No_of_stations are the independent variables</li>
<li>The coefficients (-0.6028, 1.2012, -0.0008, and 0.0239) represent the slopes of the regression line for each independent variable</li>
<li>The intercept (0.1573) represents the predicted magnitude when all independent variables are zero.</li>
<li>This equation allows us to predict the magnitude of an earthquake based on its latitude, longitude, depth, and the number of seismic stations that recorded it. By plugging in the values of the independent variables for a given earthquake, we can obtain an estimate of its magnitude.</li>
</ul>

<h3>SVM</h3>
<p>Support Vector Machines (SVM) is a type of supervised machine learning algorithm that can be used for both regression and classification tasks. The basic idea behind SVM is to find the best boundary that separates the data into different classes or predicts a continuous output variable (in this case, earthquake magnitude).
</p>
<p>
In SVM, the data points are mapped to a higher-dimensional space where the boundary can be easily determined. The best boundary is the one that maximizes the margin, which is the distance between the boundary and the closest data points from each class. This boundary is called the "hyperplane."
</p>
<p>
For regression tasks, SVM uses a similar approach but instead of a hyperplane, it finds a line (or curve in higher dimensions) that best fits the data while maximizing the margin. This line is the "support vector regression line."
</p>
<p>
SVM can handle both linear and non-linear data by using different kernels that transform the data into a higher-dimensional space. Some commonly used kernels include linear, polynomial, and radial basis function (RBF) kernels.
</p>
<p>
Once the SVM model has been trained on the data, it can be used to predict the magnitude of a new earthquake given its features (latitude, longitude, depth, and number of seismic stations). This can be useful for predicting the magnitude of earthquakes in real-time and for better understanding the factors that contribute to earthquake occurrence.
</p>
<div align="center">
<img src="https://github.com/akash-r34/Earthquake-prediction-using-Machine-learning-models/blob/main/images/SVM_plot.png"><br>
<b><i>Figure 6<br>SVM plot using matplotlib.pyplot library(python)</i></b>
 <br>
 <br>
</div>
<p>
The predicted values from SVM model when evaluated using metrics of linear regression:
<br>
MSE = 0.53
<br>
with R<sup>2</sup> = -1.92
<br>
</p>




<h3>Naive Bayes</h3>
---FINISH THE MODEL DESCRIPTION HERE--

<h3>Random Forest</h3>
---FINISH THE MODEL DESCRIPTION HERE--



