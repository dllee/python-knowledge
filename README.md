# Python Knowledge

Useful Python tips

Using gspread with pandas
pandas is a popular library for data analysis. The simplest way to get data from a sheet to a pandas DataFrame is with get_all_records():

import pandas as pd

dataframe = pd.DataFrame(worksheet.get_all_records())
Here’s a basic example for writing a dataframe to a sheet. With update() we put the header of a dataframe into the first row of a sheet followed by the values of a dataframe:

import pandas as pd

worksheet.update([dataframe.columns.values.tolist()] + dataframe.values.tolist())
For advanced pandas use cases check out these libraries:

gspread-pandas
gspread-dataframe
