Udacity_Data-Analyst_Project-4---WeRateDogs_Twitter
Data Gathering

I gathered data from 3 sources, stored in separate files:

WeRateDogs Twitter Enhanced archive, manually downloaded from the Udacity servers.

The image predictions file, programmatically downloaded from the Udacity servers.

The JSON file was also taken from Udacity, since my twitter develope account has still not been registered.

The three files were used to create pandas dataframes.

Assessment & Cleaning

I began the assessment by viewing the information on the archive table first, identifying several quality and tidiness issues. The data was investigated by checking all the data types, value counts, numeric summaries and descriptions.

All rows containing non-null values in the retweeted_status_id , retweeted_status_user_id and retweeted_status_timestamp columns were dropped, as per the requirements. These columns were then also dropped.

The timestamp column was converted to datetime data type. The 4 dog stage columns were melted into the life stage column.

The html strings in the source column were replaced with the display portion of itself.

The rating_numerator and rating_denominator columns were checked for value ranges. While these didn't make sense and didn't follow a standard they were left as they were since it was meant to be humorous.

The data types which were listed as wrong data type were corrected. Some data values such as the data in the names columns was cleaned and names like, "a", "the", "an" etc. were changed to NaN. The same was done for missing values

Some columns such as the dog life stages and p1,p2,p3 columns were merged into one column.

The json_data table itself was cleaned by leaving only the retweet_count and favorite_count columns while the rest were dropped.

The data was cleaned and then the three dataframes were merged into one, using the unique tweet it identifier.

Every issue that was identified has been cleaned and tested in the jupyter notebook.

Storage

The merged master dataframe was stored as a csv file.
