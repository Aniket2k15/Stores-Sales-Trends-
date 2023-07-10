## Libraries used : Padas, Numpy, Matplotlib, Seaborn

### 2 Datasets - sales_train and stores_data

## 1st Dataset - Sales_train_data

### 8 features, each contains 1017209 data points, 1 target variable (sales)

## Features 
* Id: transaction ID (combination of Store and date)
* Store: unique store Id
* Sales: sales/day, this is the target variable
* Customers: number of customers on a given day
* Open: Boolean to say whether a store is open or closed (0 = closed, 1 = open)
* Promo: describes if store is running a promo on that day or not
* StateHoliday: indicate which state holiday (a = public holiday, b = Easter holiday, c = Christmas, 0 = None)
* SchoolHoliday: indicates if the (Store, Date) was affected by the closure of public schools

## Basic Stats of the Data
* Average sales amount per day = 5773 Euros
* Minimum sales per day = 0
* Maximum sales per day = 41551 
* Average number of customers = 633, minimum number of customers = 0, maximum number of customers = 7388

## 2nd Dataset - Store_info data
### 10 columns, each has 1115 records

## Features
* StoreType: categorical variable to indicate type of store (a, b, c, d)
* Assortment: describes an assortment level: a = basic, b = extra, c = extended
* CompetitionDistance (meters): distance to closest competitor store
* CompetitionOpenSince [Month/Year]: provides an estimate of the date when competition was open
* Promo2: Promo2 is a continuing and consecutive promotion for some stores (0 = store is not participating, 1 = store is participating)
* Promo2Since [Year/Week]: date when the store started participating in Promo2
* PromoInterval: describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g. "Feb,May,Aug,Nov" means each round starts in February, May, August, November of any given year for that store

## Basic Stats 
* On average, the competition distance is 5404 meters away (5.4 kms)

## Exploring 1st Dataset - Sales_train
* This data don't have any null value
* Average 600 customers per day, maximum is 4500 (note that we can't see the outlier at 7388!)
* Data is equally distibuted across various Days of the week (~150000 observations x 7 day = ~1.1 million observation)
* Stores are open ~80% of the time
* Data is equally distributed among all stores (no bias)
* Promo #1 was running ~40% of the time
* Average sales around 5000-6000 Euros
* School holidays are around ~18% of the time

<img width="869" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/989257a1-5ffb-4510-be90-ce2c1a4fe3e9">
<img width="320" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/05f21068-f1ee-45b2-bcdb-3d2520ae4093">

## Let's view the values of how many store are open and closed. And remove the closed stores from the data 
<img width="196" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/e28ba1ed-798c-4e9e-a54d-9a3fa4c11782">
* Around 172817 stores are removed 
* Average sales = 6955 Euros,	average number of customers = 762	(went up)

## Exploring 2nd Dataset - Store_info 
* Null Data

<img width="260" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/97e45a2a-6cfb-44ae-969d-e5eb97912f7d">

* Handling Null values

<img width="720" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/69c9b86f-9e86-422a-bce5-1a78731efde7">

<img width="606" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/5cc6df6e-2dd3-4cdf-a3dc-0ff964aa7303">

## Let's view the corelation of sales with its features 

<img width="229" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/881bc82c-8060-4974-9420-db957edac90a">

## The average sales and number of customers per month 

<img width="452" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/b7dc49e8-8bc9-418d-ba7d-37e0c9967bf7">

<img width="449" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/40b53227-5a44-4e89-968b-77ea7b290b5a">

## The sales and customers per day of the month 

<img width="452" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/dfdccc9c-8f81-4f3e-bdd5-f46c746b7f69">

<img width="447" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/8740346c-7756-4d93-b703-b5b5325762f8">

## The sales according to Days of the week 

<img width="453" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/3235d3fb-cc10-48f6-b43d-51531f020f8f">

<img width="452" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/f567f45d-1ea5-4ef5-90fb-b0d21c49a7b2">


# Predicting Sales through Facebook Prophet
### Prophet is a procedure for forecasting time series data where non - linear trends are fit yearly, weekly, daily, plus holiday effects 

<img width="389" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/3702324b-5e04-4e8b-aa6d-27226cd46c74">

<img width="532" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/4fe2f7ee-6458-4c6e-935a-ccef9910cff1">

<img width="477" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/defd29e1-58db-4b96-bb22-f2b4ab5e4a2c">

<img width="479" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/e2385328-7dd4-4436-b1de-8da5564a3114">

<img width="478" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/68d0fe7e-a183-42a4-935b-c29c7d181479">

## Predictions using holidays for a specific store

<img width="404" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/f0297cd6-44fc-44b4-a687-05a80ed367bc">

<img width="439" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/d9a1e167-7030-4ec8-a549-cbcbf47baa2f">

<img width="443" alt="image" src="https://github.com/Aniket2k15/Stores-Sales-Trends-/assets/138878014/e29c68ea-652e-484c-a1d3-aba73b6bb4a5">


























