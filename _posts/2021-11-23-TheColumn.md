---
layout: post
title: The Column Subscriber Analysis
image: "/posts/Clicks Analysis.jpg"
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
