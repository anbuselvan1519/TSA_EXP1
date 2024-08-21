## Developed by: Anbuselvan.S
## Register No:212223240008
## Date: 
# Ex.No: 01-A PLOTTING OF TIME SERIES DATA OF YAHOO STOCK PREDICTION

# AIM:
To Develop a python program to Plot a time series data for yahoo stock prediction

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
   
# PROGRAM:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
data=pd.read_csv("/content/yahoo_stock.csv")
data.head()
data['Date']=pd.to_datetime(data['Date'])
data.set_index('Date',inplace=True)
mean_value=data['Volume'].mean()
print("Mean Volume:", mean_value)
plt.plot(data.index, data['Volume'],color='b')
plt.xlabel('Date')
plt.ylabel('Volume')
plt.title('Volume Over Time')
plt.show()
```
# OUTPUT:
![image](https://github.com/user-attachments/assets/9952e1eb-c27e-4301-971d-a57768be0566)

# RESULT:
Thus we have created the python code for plotting the time series of given yahoo stock prediction
