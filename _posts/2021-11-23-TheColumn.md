---
layout: post
title: Finding Prime Numbers with Python
image: "/posts/primes_image.jpeg"
tags: [Python, Primes]
---

I had the pleasure in completing a hackathon where I was tasked with analyzing subscriber data for The Column and providing recommendations to imporove their advertising processes. Their main objectives were to increase clicks, opens, and minimize unsubscribers for their newsletter.

---

First I imported the required libraries and file

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
summary = pd.read_excel(r'C:\Users\kedei\OneDrive\Documents\Hackathon 1\summary data.xlsx')
```
