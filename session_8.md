# Stats For DS
## EDA -
### Mean: Good for understanding typical value when there are no big outliers.

### Median: More trustworthy when the data is skewed or messy.

### IQR: Helps detect outliers and understand variability.

## How these stats guide your actions

### When you see:

### Mean ≠ Median → Data is skewed → Might need transformations (log, square root) or robust models.

### Large IQR → High variability → Feature might need scaling.

### Outliers (detected via IQR rule) → Might need capping, removal, or winsorizing.

## Quartiles
* Q1 = the value at the 25% point

* Q2 (median) = the value at the 50% point

* Q3 = the value at the 75% point

### So quartiles are just markers that split your data into 4 chunks.
##  IQR = Q3 − Q1

### It tells you how wide the middle 50% of the data is.

### If IQR is small, the middle of your data is packed tightly.

### If IQR is large, the data is very spread out.
## Covariance
* Covariance measures how two variables move together:

*  If both increase together, covariance is positive.

* If one increases while the other decreases, covariance is negative.

* If there’s no clear pattern, covariance is near zero

## Correlation
### Correlation is a scaled version of covariance that always falls between -1 and 1.

* +1 → perfect positive relationship

* 0 → no relationship

* -1 → perfect negative relationship
