# Credit-Score-Binning: automate the process of binning credit scores into predefined 5-point ranges

https://github.com/AniaSupady/Credit-Score-Binning/blob/main/Binning.ipynb


Creating the Bins: The code first constructs the bin boundaries. The L1, L2, R1, and R2 variables, combined with np.arange(), generate the start and end points for the 5-point bins (e.g., 315-320, 321-326, etc.). The combined and sorted list, band, acts as the precise set of boundaries for all credit score ranges.

Efficient Binning: The core of the code's efficiency lies in the pd.cut() function. This function takes the raw credit score data (df['score']) and the predefined bin boundaries (bins=band) and automatically assigns each score to the correct 5-point interval. This is much faster and cleaner than manual if-else logic, especially for a large number of bins.

Analysis: After binning the data, the code uses value_counts() to count how many credit scores fall into each bin. This analysis allows you to observe the distribution of credit scores and, as you mentioned, can be used to track credit drift over time. By running this code on data from different time periods, you can compare the distribution of scores and see if the scores are shifting into higher or lower bins.
