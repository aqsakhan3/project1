**Overview**:

This project focuses on preparing a raw dataset for reliable analysis. Before any dashboard, report, or model can be trusted, the underlying data has to be accurate and consistent. The objective here was not to build visualizations, but to establish data integrity: locating every missing value, duplicate record, and formatting inconsistency in the dataset, correcting each issue in a transparent and auditable way, and confirming the final result is error-free.
The entire process was carried out in Microsoft Excel using built-in formulas.

**Dataset**:

The source file is data/Dataset_for_Data_Analytics.xlsx, containing 1,200 e-commerce order records across 14 columns: OrderID, Date, CustomerID, Product, Quantity, UnitPrice, ShippingAddress, PaymentMethod, OrderStatus, TrackingNumber, ItemsInCart, CouponCode, ReferralSource, and TotalPrice.

**Approach**:

**Auditing the data**: Every column was systematically checked for missing values, duplicate order IDs, invalid date entries, and numeric precision issues. This step used Excel functions such as COUNTBLANK, COUNTIF, ISNUMBER, and ROUND to quantify problems before making any changes. The audit found 309 blank CouponCode entries, representing orders placed without a coupon rather than a data error. No duplicate order IDs, invalid dates, or precision issues were found.

**Cleaning the data**: A separate sheet was built to read the raw data and apply corrections without altering the original source. Text fields were trimmed of extra whitespace and standardized in casing using functions like TRIM, PROPER, and UPPER. Currency values were rounded to two decimal places with ROUND. Missing CouponCode entries were filled with a clearly labeled "No Coupon" value using an IF condition, rather than deleting those rows. Order totals were recalculated from quantity and unit price to guarantee internal consistency.
