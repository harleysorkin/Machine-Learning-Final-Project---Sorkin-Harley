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

My plan is to find a model relating make, model, year, mileage, transmission, fuelType, engineSize, and mpg to accurately predict the price of a car on the used market in the UK. As far as I can tell, the tax value comes from an outside factor and is unpredictable with the given data. 
