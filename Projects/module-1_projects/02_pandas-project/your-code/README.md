The notebook data-wrangling.ipynb contains examination and cleaning of the sharkattack.csv dataset als contained in this folder.

sharkattack_clean.csv is the output file. 

For the purpose of cleaning, columns were inspected for being redundant, messy or in wrong format.

What was done per column?

Case Number: 
    Dropped since it has no additional information value
Date:
    Converted to pandas datefime format
Year:
    Dropped since it has no additional information value
Type:
    Already clean column, merged "Boating" and "Boat" Types
Country:
    Already clean column, uppercased all, removed ? characters and trailing whitespaces
Area:
    Already clean column, uppercased first letter of all words, remove ? and � characters, reomve trailing whitespaces
Location:
    Same as Area column.
Activity:
    Very heterogeneous column with lengthy descriptions of victim activity. Left as it is.
Name:
    Left as it is.
Sex:
    Converted to binary float with 1 for Male and 0 for Female
Age:
    Converted to float.
Injury:
    Very heterogeneous column with descriptions of victim injury. Left as it is.
Fatal (Y/N):
    Converted to binary float with 1 for Fatal and 0 for non-Fatal
Time:
    Converted to time of the day in 24h format
Species:
    Converted into shark species names: e.g. white shark -> white.
Investigator or Source:
    Very heterogeneous, left as it is.
pdf:
    Duplicate of href. Dropped
href formula:
    Duplicate of href. Dropped
href:
    Left as it is.
Case Number.1 and Case Number.2:
    Dropped, as no info value.
original order:
    Dropped, as no info value.
Unnamed: 22 and Unnamed: 23:
    Dropped, as no info value.



Methods used:

.isna()
.sum()
.drop()
.loc()
.value_counts()
.rename()
.gt(1)
.duplicated()
.str.replace()
.pd.to_datetime()
.isnull()
.index
.str.title()
.str.lstrip()
.str.rstrip()
.str.replace()
.str.contains()
.fillna()
.str.extract()
.dropna()
.reset_index()
.pd.to_numeric()
.describe()
.len()


