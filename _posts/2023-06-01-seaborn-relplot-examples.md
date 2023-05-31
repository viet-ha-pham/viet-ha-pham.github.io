---
layout: post
title: "Seaborn: Drawing relplots"
categories: seaborn
tags: [seaborn, visualization]
---
```python
import seaborn as sns
```


```python
tips = sns.load_dataset("tips")
```


```python
tips.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>total_bill</th>
      <th>tip</th>
      <th>sex</th>
      <th>smoker</th>
      <th>day</th>
      <th>time</th>
      <th>size</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>16.99</td>
      <td>1.01</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10.34</td>
      <td>1.66</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>21.01</td>
      <td>3.50</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>23.68</td>
      <td>3.31</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>24.59</td>
      <td>3.61</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>25.29</td>
      <td>4.71</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>4</td>
    </tr>
    <tr>
      <th>6</th>
      <td>8.77</td>
      <td>2.00</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>7</th>
      <td>26.88</td>
      <td>3.12</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>4</td>
    </tr>
    <tr>
      <th>8</th>
      <td>15.04</td>
      <td>1.96</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>9</th>
      <td>14.78</td>
      <td>3.23</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>




```python
sns.relplot(data=tips, x = "total_bill", y = "tip")
```




    <seaborn.axisgrid.FacetGrid at 0x2894e31c790>




    
<img src="/assets/images/output_3_1.png">
    



```python
sns.set_theme()
```


```python
sns.relplot(data=tips, x = "total_bill", y = "tip")
```




    <seaborn.axisgrid.FacetGrid at 0x2894ea96f40>




    
<img src="/assets/images/output_5_1.png">
    



```python
sns.relplot(data=tips, x = "total_bill", y = "tip", hue="sex")
```




    <seaborn.axisgrid.FacetGrid at 0x2894ea80790>




    
<img src="/assets/images/output_6_1.png">
    



```python
sns.relplot(data=tips, x = "total_bill", y = "tip", hue="sex", size="size")
```




    <seaborn.axisgrid.FacetGrid at 0x2894ebe8790>




    
<img src="/assets/images/output_7_1.png">
    



```python
sns.relplot(data=tips, x = "total_bill", y = "tip", hue="sex", size="size",style="smoker")
```




    <seaborn.axisgrid.FacetGrid at 0x2894ec72040>




    
<img src="/assets/images/output_8_1.png">
    



```python
sns.relplot(data=tips, x = "total_bill", y = "tip", hue="sex", size="size",style="smoker", col="time")
```




    <seaborn.axisgrid.FacetGrid at 0x2894ebf6f40>




    
<img src="/assets/images/output_9_1.png">
    



```python
sns.relplot(data=tips, x = "total_bill", y = "tip", hue="sex", size="size",style="smoker", col="day", row="time")
```




    <seaborn.axisgrid.FacetGrid at 0x2894ea802e0>




    
<img src="/assets/images/output_10_1.png">
    

