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






