---
layout: post
title: The Column Subscriber Analysis
image: "/posts/thecolumn_share.png"
tags: [Python]
---

I had the pleasure in being tasked with analyzing subscriber data for The Column and providing recommendations to imporove their advertising processes. Their main objectives were to increase clicks, opens, and minimize unsubscribers for their newsletter.

---

First I imported the required libraries

```ruby
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
sns.set()
import plotly.express as px
import numpy as np
from sklearn.cluster import KMeans
from sklearn.preprocessing import MinMaxScaler
import scipy 
import statsmodels.api as sme
from statsmodels.tsa.ar_model import AR,AutoRegResults
```
I then read in my file
```ruby
summary = pd.read_excel(r'C:\Users\kedei\OneDrive\Documents\Hackathon 1\summary data.xlsx')
```
Starting maximizing the open rate of the newsletter, I visuaze a strip plot of the most common hours the newsletter is actually opened by subscribers

```ruby
ax = sns.stripplot(x='Hour', y='Opens', data=summary)
```
![alt text](/img/posts/thecolumn_share.png "Strip Plot")
