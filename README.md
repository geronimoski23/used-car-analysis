## Berkeley Artificial Intelligence and Machine Learning Course

### Practical Application #2

#### Business Understanding

- Identify the key drivers for used car prices.
    - Given a dataset which contains data pertaining to the sales of used cars, can we use tools for data visualization (pandas, numpy, pltly, seaborn), as well as toolds for machine learning and model building (sklearn) to to identify what features of the data set drive the price point of the car
    

#### Data Understanding

- Using data visualization python libraries, we visualize what features the data set contains and start developing an understanding of what features would make sense in building our model.
    - Target
        - price
    - Numerical Features
        - odometer
        - year
        - cylinders
    - Catgorical Features
        - title_status
        - size
        - type 
        - drive
        - transmission
        - fuel
        - manufacturer
        - state
        - condition
    - Unused
        - color
        - VIN
        - region
        - id
- I displayed several bar and scatter plots to display how features correlated with price as well as the value counts for each feature in the data set

#### Data Preparation

- New features were engineered using the current data set in order to create more numerical features as well as normalize, scale, and encode other features

- Two preprocessing pipelines
    - one creates polynomial features with degree 2
    - one uses the regular numerical features
    - scaling and sequential feature selection are used on both

    - non-ordinal categories are one hot encoded
    - ordinal categories are ordinally encoded


#### Model Building

- Lasso, Ridge, and Linear Regression
- Ridge had the best model score, using the polynomial pipeline
    - grid search cv was used to find the best alpha value

#### Findings

- From the model, we were able to extract information about how features were correlated with the price of the car. Below are the features that used car dealerships should look for or stay away from when determining what cars to buy for their dealership.

- Positively Correlated Features
    - diesel fuel
    - aston martin, land rover, porsche manufacturers
    - car weight and year of build
    - cars with a lien on their title
    - cars that used manual transmission
    - cars sold in Alaska
    - buses

- Negatively Correlated Features
    - mercury and fiat manufactured vehicles
    - sedans and wagons
    - cars with high mileage
    - cars sold in Louisiana and Oklahoma
    - cars that could only be sold for parts only
