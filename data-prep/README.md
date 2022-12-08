Step 1 - Generate Customers 

```commandline
 python datagen_customer.py 1000000 99 profiles/main_config.json -o customers.csv
```
Note: this is not fast!

Step 2 - Save customers to a DB

Create a customers table and load the csv (I used SQLProStudio)

```sql
CREATE TABLE `customers` (
  `ssn` varchar(31) NOT NULL,
  `cc_num` varchar(31) NOT NULL,
  `first_name` varchar(65) NOT NULL,
  `last_name` varchar(65) NOT NULL,
  `gender` char(1) NOT NULL,
  `street` varchar(127) NOT NULL,
  `city` varchar(65) NOT NULL,
  `state` char(2) NOT NULL,
  `zip` varchar(15) NOT NULL,
  `lattitude` float NOT NULL,
  `longitude` float NOT NULL,
  `city_pop` int(11) NOT NULL,
  `job` varchar(127) NOT NULL,
  `dob` date NOT NULL,
  `acct_num` varchar(65) NOT NULL,
  `profile` varchar(255) NOT NULL,
  PRIMARY KEY (`ssn`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;
```


