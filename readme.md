# Overview

This document outlines the comprehensive data cleaning process applied to the customer, products, regions, and transactions datasets. The cleaning procedures were executed in Power BI using the Power Query Editor to ensure that the data is uniform, consistent, and accurate.

## Datasets
- **Customer Dataset**
- **Products Dataset**
- **Regions Dataset**
- **Transactions Dataset**

---

## 1. Customer Dataset 

**Columns:** CustomerID, Email, updated_phone_number, City, State, Country, Gender, Age, Updated_Joined_date, updated_last_purchase_date, TotalSpent, LoyaltyPoints, PurchaseFrequency, CustomerSegment, PreferredPaymentMethod, MaritalStatus, Updated_Account_creation_date, AccountStatus, LastUpdated, Updated_Referrer_Id, FeedbackRating, Domain of mail, country_code.

### Cleaning Steps
1. **Import Data:** Loaded the dataset into Power BI through Get Data > Text/CSV.
2. **Remove Invalid Email Domains:** Filtered the Email column to exclude invalid domains.
3. **Standardize Phone Numbers:** Formatted phone numbers consistently (e.g., +1-123-456-7890).
4. **Handle Missing Values:** Addressed missing values logically, either by filling or imputing.
5. **Correct Data Types:** Ensured that each column had the appropriate data type (e.g., Date, Number, Text).
6. **Extract Email Domains:** Added a new column for the domain of the email addresses.
7. **Create Derived Columns:** Classified customers based on TotalSpent and LoyaltyPoints.
8. **Standardize Date Formats:** Applied uniform date formatting across all relevant columns.
9. **Standardize Country Codes:** Ensured country codes were consistently formatted (e.g., adding +).

---

##2. Product Dataset
**Columns:** ProductID, ProductName, Category, Price, StockStatus, Supplier, Updated_Price, Updated_StockStatus, LastUpdated, Discontinued.

### Cleaning Steps
1. **Remove Duplicates:** Identified and removed duplicate entries based on ProductID.
2. **Handle Missing Values:** Imputed missing values for Price and StockStatus as needed.
3. **Standardize Price Formats:** Ensured that all prices were consistently formatted (e.g., $100.00).
4. **Correct Data Types:** Verified that Price is a number and ProductName is text.
5. **Update Discontinued Products:** Marked products as Discontinued where applicable.

---

## 3. Regions Dataset 

**Columns:** RegionID, RegionName, Country, State, Updated_RegionName, LastUpdated, CountryCode.

### Cleaning Steps
1. **Remove Invalid Regions:** Filtered out any incomplete or invalid RegionName entries.
2. **Standardize Country Codes:** Ensured consistency in CountryCode formatting (e.g., +1 for the US).
3. **Handle Missing Values:** Used fill-down logic to address missing region or country data.
4. **Correct Data Types:** Confirmed that RegionName is formatted as text and CountryCode as a number.

---

## 4. Transactions Dataset 

**Columns:** TransactionID, CustomerID, ProductID, TransactionDate, Quantity, TotalAmount, PaymentMethod, DiscountApplied, LastUpdated.

### Cleaning Steps
1. **Remove Duplicates:** Ensured uniqueness of TransactionID by eliminating duplicates.
2. **Handle Missing Data:** Imputed or removed entries with missing Quantity and TotalAmount.
3. **Correct Data Types:** Ensured TransactionDate is in date format and TotalAmount is a number.
4. **Standardize Payment Methods:** Achieved consistency in the PaymentMethod column (e.g., Credit Card, PayPal).
5. **Update Discounts:** Verified that values in the DiscountApplied column were consistent.

---

## Conclusion

The cleaning and standardization processes have been successfully completed for each dataset. All datasets are now consistent, error-free, and structured effectively for analysis and reporting in Power BI.
