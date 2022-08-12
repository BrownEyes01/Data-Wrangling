## Data Wrangling carried out on WeRateDogs Twitter Archive
> Data wrangling caried out on this project consisted of 3 steps
- Gathering Data
- Assessing Data
- Cleaning Data
### Gathering Data
> The data used for this project was gathered in 3 different ways. The twitter-archive-enhanced data which was in a csv format and provided by WeRateDogs from their archive. It contained about 5000+ basic tweets but tweets that had dog ratings alone were extracted.
</br> Also every image in the archive was run through a neural network that can classify breeds of dogs. The result were compiled in a table which was in a tsv format and consisted of top3 image predictions, with their image_url, tweet_id and image number that corresponded to the most confident prediction.
</br> Additional data needed was extracted via the twitter API and saved to a file in json format. This file consisted of two distinct columns which were particularly needed: retweet count and favorite count.
</br> All 3 files were read into a pandas dataframe to be used for further assessment.
### Assessing Data
> Two types of assessment were carried out on the datasets; visual and programmatic.
The visual involves assessing the data visually to spot issues and discrepancies associated with the data. Some of the issues include:
- Some values in the name column are in lowercase and appear to not be dog names.
- Non-descriptive column names.
- Inconsistent alphabet case.
The programmatic involves using code and functions to detect the issues and discrepancies in the data. Some of the issues include:
- Erroneous datatypes.
- Outliers in some columns.
- Duplicated column across the dataframes.
</br> There are two type of issues that needed cleaning in the data, we had the **Quality Isuues** and **Tidiness Issue**.
</br> Tidiness issue has more to do with the structure. They say a data is not tidy until
-Every obsevation is a row
-Every variable is a column
-Every type of obsevation unit is a table.
![Screenshot (51)](https://user-images.githubusercontent.com/106492366/180768452-41bc6db1-6a71-4fcf-942c-148dcf3f6c43.png)

### Cleaning Data
> Using the **define-code-test** framework for cleaning data, each issues identified during the assessment were cleaned. First, the process of cleaning an issue was defined in succint terms, then the cleaning code required then test the cleaning code to ensure the cleaning process worked.
For example, we have a dataframe (df) with an erroneous datatype: float instead of int in a column
- **Define**: Changing the datatype to integer using the astype method
- **Code**: df.column.astype(int)
- **Test**: df.info() *this shows the information of the dataframe, so here we can confirm the datatype has changed*
![Screenshot (50)](https://user-images.githubusercontent.com/106492366/180768612-b8bdc2d8-7fe8-4469-a077-0dcef291dd8c.png)


### Storing Data
> The cleaned and final data was then stored into a csv file, twitter_archive_master.csv which will then later be used for further analysis.
![Screenshot (46)](https://user-images.githubusercontent.com/106492366/180764517-1bbf3873-db90-4ac6-af48-15dc18259b20.png)

### Analyzing and Visualizing the Data
> After going through the wrangling process (gathering, assessing, cleaning) and then storing the cleaned data in a master dataframe, the data can now be analyzed to generate insights and visualization.
In order to get insights from the data, we queried the data set a bit. From these queries, we had some information which includes:
- Tweets that have one image were mostly predicted and from the confidence level of the predictions, we had more of them as dog i.e True
- The mean of the first prediction confidence is approximately 60% and the minimum and maximum value were 4.4% and 100% respectively.
- The average retweet count was 2900 and the average favorite count was 9049.
- Of the four stages, we have more dogs that were classified as pupper, which from the definitions are dogs that are young and small and not so inexperienced. Can also be classified as the dog equivalent of a baby.

#### Distribution of the Dog stages
![Screenshot (53)](https://user-images.githubusercontent.com/106492366/180769675-c730986e-4d27-4ac0-bbb2-8904722b45f7.png)

> You can check and make reference to the code [here](https://github.com/BrownEyes01/Data-Wrangling/blob/main/Project2.ipynb) in details.
</br> Thank You!
