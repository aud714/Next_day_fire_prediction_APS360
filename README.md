# Next day fire prediction - APS360
This is a deep learning model developed for the final project of the course APS360 Applied Fundamentals of Deep Learning at the University of Toronto. It utilizes transfer learning and a Recurrent Neural Network (RNN) to predict the spread of wildfires.
- Decreased final training loss by 93.4%.
- Trained from Next Day Wildfire Spread dataset, which contained remote-sensing images (TFRecord format) of past US wildfires
- Divided into sets of 13 images:
  - 1st-11th → environmental factor images
  - 12-13th → previous and current fire masks
  - Label → current fire masks
- Data Processing using PyTorch:
  1. Loaded and converted the TFRecord data to 3-channel upscaled RGB image tensors (input to AlexNet)
  2. Remove uncertain data with gray pixels

# Introduction
With the annual summer wildfires increasing in frequency and severity, wildfires and their spread have become prevalent concern in the world today. To tackle this issue, our team created a deep learning project to forecast wildfire spread. This model takes in sequential image data from a dataset of past and present fire masks and environmental factors like wind patterns, rainfall, and temperature.
To handle large number of samples and diverse variables of the image data, deep learning is the ideal model for analyzing large and complex datasets with many features, providing more accurate predictions than statistical methods. The sequential nature of the datasets make it challenging to capture wildfire spread, therefore we employed transfer learning and a recurrent neural network (RNN). RNNs have demonstrated proficiency in sequential data predictions. Our model outputs a single map image indicating the spread of fire based on the input images of environmental factors and previous day’s fire map.
Through precise fire forecasts, our project aims to offer early warnings, facilitating timely evacu- ations for life and property protection. Additionally, this aids in directing firefighting resources to high-risk zones, reducing risks for firefighters. This proactive strategy enhances wildfire contain- ment, safeguarding forests and wildlife.
