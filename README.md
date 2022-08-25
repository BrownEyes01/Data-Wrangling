# Data Wrangling carried out on WeRateDogs Twitter Page [@dog_rates](https://twitter.com/dog_rates)
## Introduction
WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. In this project, analysis was carried out on the data gotten from the twitter account.
## Dataset
For the data gathering, three datasets were gathered in different ways:
- We Rate Dogs' Enhanced Twitter Archive: The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, tweets that had dog ratings alone were extracted. This dataset was available in **csv** format.
- Additional Data via the Twitter API : Additional data needed was extracted via the twitter API and saved to a file in json format. This file consisted of two distinct columns which were particularly needed: retweet count and favorite count.
- Image Predictions File :  Also every image in the archive was run through a neural network that can classify breeds of dogs. The result were compiled in a table which was in a tsv format and consisted of top3 image predictions, with their image_url, tweet_id and image number that corresponded to the most confident prediction.
## Summary of Findings
After going through the wrangling process (gathering, assessing, cleaning) and then storing the cleaned data in a master dataframe, the data can now be analyzed to generate insights and visualization.
In order to get insights from the data, we queried the data set a bit. From these queries, we had some information which includes:
- Tweets that have one image were mostly predicted and from the confidence level of the predictions, we had more of them as dog i.e True
- The mean of the first prediction confidence is approximately 60% and the minimum and maximum value were 4.4% and 100% respectively.
- The average retweet count was 2900 and the average favorite count was 9049.
- Of the four stages, we have more dogs that were classified as pupper, which from the definitions are dogs that are young and small and not so inexperienced. Can also be classified as the dog equivalent of a baby.
## Key Insights for Presentation
- View the content on nbviewer: Jupyter Notebook
- Alternatively you can download the HTML file in the subdirectory and view content locally on any browser.
## Getting Started
> For testing and development purposes, these instructions will help you get a copy of the project up and running on your system.
### Prerequisites
- Installing Jupyter notebook, this can be gotten from the Anaconda Navigator or Anaconda Prompt.
- You would also need to install Python and some of it's libraries (can be installed either using **conda** or **pip**)
  - Pandas
  - Numpy
  - Matplotlib
  - requests
  - tweepy
  - json
### Installaton
The following shows how to get a development environment running Here are the installation steps:
- Download the Anaconda installer. Choose the Python 3.6 or higher version, and the appropriate 64/32-bit installer.
- Refer to the installation instructions here.
- Verify the installation, as mentioned here

</br> If you already have Anaconda installed, use the ```environment.yaml``` to create the exact environment I used during the project by typing the line below into the Anaconda terminal in the same folder where the environment file is saved on your computer.
```
conda env create -f environment.yaml
```
OR If you're not using Conda, you can use pip to install dependencies with the requirements.txt file by typing this line into your terminal
```
pip install -r requirements.txt
```
## Built With
- [Anaconda](https://www.anaconda.com/) - Dependency Management
- [Jupyter Notebook](https://jupyter.org/) - Data Analysis Documentation

## Authors
- Frances Uzedu
## License
- This project is licensed under the GNU License- see the LICENSE for details.
## Acknowledgements
- Udacity ALX-T Data Analyst Nanodegree
