### Matplotlib – 
 the core plotting library in Python. Good for basic plots like line charts, scatter plots, bar charts.

### Seaborn – 
built on Matplotlib but easier for statistical plots and prettier visuals.

``` python
import matplotlib.pyplot as plt

# Sample data
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# Create a plot
plt.plot(x, y)

# Add title and labels
plt.title("My First Line Plot")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")

# Show the plot
plt.show()
```
## changing colour and style 
```python
plt.plot(x, y, color='red', linestyle='--')
```
or we can combine them
```python
plt.plot(x, y,'r--') # red dashed lines
```
### Line style
  '-' → solid

 '--' → dashed

 ':' → dotted

 '-.' → dash-do
### Markers
'o' → circle

'x' → cross

'^' → triangle up

's' → square

## Matplot Basic Plot Types
Use scatter for points, plot for trends.

For categorical data, bar is usually best.

Frequency data → histogram.

For proportions → pie chart.


| Type         | Function / Use Case            | Function Example              |
| ------------ | ------------------------------ | ----------------------------- |
| Line Plot    | Trends over time or numbers    | `plt.plot(x, y)`              |
| Scatter Plot | Relationships between points   | `plt.scatter(x, y)`           |
| Bar Chart    | Compare categories             | `plt.bar(categories, values)` |
| Histogram    | Frequency distribution         | `plt.hist(data, bins=...)`    |
| Pie Chart    | Proportion of parts of a whole | `plt.pie(values, labels=...)` |

## Matplot Attributes

| Attribute          | Purpose                            | Example                |
| ------------------ | ---------------------------------- | ---------------------- |
| `color` / `c`      | Line or marker color               | `color='red'`          |
| `linestyle` / `ls` | Line style: solid, dashed, dotted  | `linestyle='--'`       |
| `marker`           | Shape of points (for scatter/line) | `marker='o'`           |
| `s`                | Size of points (scatter only)      | `s=100`                |
| `xlabel`           | Label for x-axis                   | `plt.xlabel("X")`      |
| `ylabel`           | Label for y-axis                   | `plt.ylabel("Y")`      |
| `title`            | Plot title                         | `plt.title("My Plot")` |
| `plt.show()`       | Display the plot                   | `plt.show()`           |

## Seaborn
```python
import seaborn as sns
import matplotlib.pyplot as plt  # still needed for plt.show()
```

Seaborn works best with DataFrames.

Automatically makes plots prettier than Matplotlib.

Use hue, style, size for grouped plots. 


## Common Seaborn Plot Types
| Plot Type           | Use Case / What it Shows         | Function Example                   |
| ------------------- | -------------------------------- | ---------------------------------- |
| `sns.lineplot()`    | Trend over continuous variable   | `sns.lineplot(x=x, y=y)`           |
| `sns.scatterplot()` | Relationship between 2 variables | `sns.scatterplot(x=x, y=y)`        |
| `sns.barplot()`     | Compare categories (avg values)  | `sns.barplot(x=category, y=value)` |
| `sns.histplot()`    | Distribution of numeric data     | `sns.histplot(data, bins=10)`      |
| `sns.countplot()`   | Counts per category              | `sns.countplot(x=category)`        |
| `sns.boxplot()`     | Show spread & outliers           | `sns.boxplot(x=category, y=value)` |
| `sns.heatmap()`     | Correlation matrix / grids       | `sns.heatmap(data)`                |

## Seaborn Attributes

| Attribute | Purpose                                     | Example                                         |
| --------- | ------------------------------------------- | ----------------------------------------------- |
| `data`    | Data source (Pandas DataFrame or array)     | `sns.scatterplot(data=df, x='age', y='height')` |
| `x`, `y`  | Variables to plot                           | `x='column1', y='column2'`                      |
| `hue`     | Grouping by category (colors automatically) | `hue='gender'`                                  |
| `palette` | Color palette                               | `palette='Set2'`                                |
| `style`   | Marker style by category                    | `style='gender'`                                |
| `size`    | Marker size by category                     | `size='score'`                                  |
| `kind`    | For `sns.catplot()` type: bar, box, etc.    | `sns.catplot(kind='bar', x='cat', y='val')`     |
