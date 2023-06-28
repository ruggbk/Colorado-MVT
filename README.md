# Capstone---Colorado-Motor-Vehicle-Theft
This project is an investigation into the ongoing surge in motor vehicle thefts observed in Colorado beginning in 2014.

'Colorado MVT Analysis.ipynb' is the primary notebook, and contains almost all content and analysis. The other two jupyter notebooks are just for data ingestion and basic processing. The notebook 'FBI Crime Data API.ipynb' ingests data exclusively from the FBI Crime API. The notebook 'US Census Bureau API & General Economic Info.ipynb', ingest and process data from a variety of sources, including the US Census Bureau API and various .csv files from sources such as the Colorado Department of Revenue and the Bureau of Labor Statistics.

Other files are saved .csv files and pandas dataframes. Saved dataframes include the primary dataframe, 'main_df', as well as the outcome of some API requests that took 5-10 minutes to process.