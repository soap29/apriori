# apriori


useful links:

https://www.geeksforgeeks.org/how-to-drop-one-or-multiple-columns-in-pandas-dataframe/
https://www.kaggle.com/code/benroshan/sentiment-analysis-amazon-reviews
https://stackoverflow.com/questions/52670115/pandas-df-corr-one-variable-across-multiple-cols
https://stackoverflow.com/questions/59480191/calculating-the-survival-rate-of-a-group-with-pandas#:~:text=Save%20this%20answer.,Show%20activity%20on%20this%20post.&text=So%20100%25%20of%20the%20females,(1%2F3)%20survived.
https://pandas.pydata.org/pandas-docs/stable/user_guide/reshaping.html#combining-with-stats-and-groupby
https://www.geeksforgeeks.org/how-to-add-metadata-to-a-dataframe-or-series-with-pandas-in-python/
https://stackoverflow.com/questions/42111182/get-list-of-x-minimum-distances-by-their-indices
https://levelup.gitconnected.com/bi-tri-and-n-grams-with-python-a9717264e6f2
https://www.kaggle.com/code/ibtesama/getting-started-with-a-movie-recommendation-system
https://medium.com/nerd-for-tech/how-to-plot-timeseries-data-in-python-and-plotly-1382d205cc2
https://builtin.com/data-science/data-wrangling-pandas
https://stackoverflow.com/questions/58435648/applying-transaction-encoder-on-dataset
https://www.kdnuggets.com/2019/05/complete-exploratory-data-analysis-visualization-text-data.html/2



METADATA:

drf.info()

# store in hdf5 file format
storedata = pd.HDFStore('college_data.hdf5')
 
# data
storedata.put('data_01', drf)
 
# including metadata
metadata = {'scale': 0.1, 'offset': 15}
 
# getting attributes
storedata.get_storer('data_01').attrs.metadata = metadata
 
# closing the storedata
storedata.close()
 
# getting data
with pd.HDFStore('college_data.hdf5') as storedata:
    data = storedata['data_01']
    metadata = storedata.get_storer('data_01').attrs.metadata
 
# display data
print('\nDataframe:\n', data)
 
# display stored data
print('\nStored Data:\n', storedata)
 
# display metadata
print('\nMetadata:\n', metadata)
