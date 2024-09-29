# Predicting Apartment Pricing in Daegu

## Business Problem Understanding
***Context***

A business is selling apartments in Daegu, a city in South Korea. As one of the urban areas in the nation, the demand for housing is high. At the same time, the city has limited residential land, making apartments one of the solutions. This makes analyzing apartment prices, influenced by various internal and external factors, a topic of great interest.

Apartment units are typically offered by individual owners or companies, who list them on platforms and set their own prices. However, adjusting these prices to match market conditions can be challenging. Overpricing may lead to difficulty in securing buyers, while underpricing can result in reduced profits for the seller.

Target: Sale Price



***Problem Statement***

Management is searching for the best way to predict sale prices, as this is essential for maximizing their profit. If they overprice the apartments, they risk losing customers, while underpricing could reduce their profit potential.

Currently, management has a method to predict apartment sale prices, but it is considered too simplistic for handling large datasets. They have been predicting apartment prices using rule-based model based on the median for each hallway type (terraced, mixed, and corridor). The median prices are 275,840 won for terraced, 155,799 won for mixed, and 87,968 won for corridor apartments.

Therefore, the problem statements are as follows:

1. What factors influence apartment pricing in Daegu?
2. What is the best model for predicting apartment prices, and how does this model forecast pricing in Daegu?
3. How can the business benefit from the model?



***Analytic Approach***

Management plan to build a best model to predict apartment pricing in Daegu. They plan to use the Machine Learning algorithm. Machine learning operates using models that are driven by algorithms, which can be fully reliant on data. Unlike rule-based algorithms, machine learning is highly scalable with increasing amounts of data. As the algorithm is exposed to more data, it improves its ability to identify key features, leading to enhanced performance (Source:socure.com).

Therefore, I will assist management in developing the best model for predicting apartment prices using a machine learning algorithm. Since this involves predicting apartment prices, it will be approached as a regression problem.


***Metric Evaluation***

The model will be evaluated using Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R-squared. This project will primarily focus on RMSE, as apartment prices vary widely, ranging from lower-end to higher-end units. These price differences are crucial in predicting pricing accurately. RMSE is preferred because it places greater emphasis on larger errors by squaring them before averaging, making it more sensitive to outliers. In this project, large deviations in predicted prices could have significant financial consequences.

## Variable Description
| Variable | Description |
|---- | ---- |
| HallwayType | Type of Apartment (terraced, mixed, and corridor)|
| TimeToSubway | Time needed to the nearest subway station (in range of: 0-5 min; 5-10 min; 10-15 min; 15-20 min; and no_bus_stop_nearby)|
| SubwayStation | The name of the nearest subway station, there are 7 nearest subway and 1 no subway nearby|
| N_FacilitiesNearBy(ETC) | The number of Electronic Tolls Collection facilities nearby (0, 1, 2, and 5) |
| N_FacilitiesNearBy(PublicOffice) | The number of public office facilities nearby (0, 1, 2, 3, 4, 5, 6, 7) |
| N_SchoolNearBy(University) | The number of universities nearby (0, 1, 2, 3, 4, 5) |
| N_Parkinglot(Basement) | The number of the parking lot (0, 18, 56, 76, 79, 108, 181, 184, 203, 218, 400, 475, 524, 536, 605, 798, 930, 1174, 1270, 1321)|
| YearBuilt | The year the apartment was built (1978, 1980, 1985, 1986, 1992, 1993, 1997, 2003, 2005, 2006, 2007, 2008, 2009, 2013, 2014, 2015)|
| N_FacilitiesInApt | Number of facilities in the apartment (1, 2, 3, 4, 5, 7, 8, 9, 10)|
| Size(sqf)| The apartment size (in square feet)|
| SalePrice| The apartment price (Won)|
