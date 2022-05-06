# Machine-Learning-Final-Project---Sorkin-Harley

## Dataset
I am using a dataset that tracks used car prices of 7 different makes in the UK. The makes include: Audi, BMW, Toyota, Skoda, VW, Ford, and Huyandai.

The dataset initially had the columns 'model', 'year', 'price', 'transmission', 'mileage', 'fuelType', 'tax', 'mpg', 'engineSize', and 'Make'. I added the columns 'avgPrice' and 'avgMpg' (of each model) to help get a better sense of the data.

## Initial Findings

I started by making a pairplot of all the data to look for any trends.

![image](https://user-images.githubusercontent.com/92001255/165655860-56393fd4-8e37-4eff-b9dd-fb7f21f42e2f.png)


The first set of data that caught my attention was year vs price.

![image](https://user-images.githubusercontent.com/92001255/165656499-7391a5f6-dcf9-45ae-acd0-c8e630c17dea.png)

I separated the data by make, and then found regression data for transmission type. The flatter the regression line, the more value that type of transmission will hold over the years. For every make, manual transmissions held their value the best, followed closely by automatic for all but the Skoda brand.

Next I looked at mileage vs price.

![image](https://user-images.githubusercontent.com/92001255/165656965-985d050e-1ab7-41ad-8dd1-c1b0d2a7511d.png)

Again, I separated the data by make. Like the last plot, the flatter the regression line, the more value that make will hold despite higher mileage. From this data we can see that Audi and BMW lose value the fastest the more mileage is on the car.

I also looked at avgPrice vs avgMpg.

![image](https://user-images.githubusercontent.com/92001255/165657696-5bff7286-eed5-4415-941b-311fe09707f4.png)

This data shows that as the price of a model rises, typically the mpg drops. This is helpful for beginning to understand what factors affect price.

## Data Prep

I removed the 'tax' column as it had no correlation to the rest of the data. Then I used Lable Encoding to encode the 'model', 'transmission', 'fuelType', and 'Make' columns. OneHotEncoding gave issues with the regression models when used on make and model.

I also added the columns 'avgPriceMake', 'maxPriceMake', and 'maxPriceModel'.

## Linear Regression and SGD Regression scores

My linear regression scores yielded around 85% accuracy when training on 90% of randomly sampled data with little variation when the training sample was reduced. The SGD regressor, on the other hand, could not find a model to fit the data no matter how much training was done.
