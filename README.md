# Big_Data
In this repository, I will upload all the notebooks we cover in the Big Data and Text Management course.



ps: nella prova del 8 gennario compaiono dei ? nel dataset. sono missing value semantici. occorre capire come gestirli
se la prof ti dice di considerarli come nan la soluzione più comoda è caricare il dataset in questo modo
df = pd.read_csv(
    'adult.csv',
    sep=',',
    na_values='?'
)
in questo modo "?" viene automaticamente convertito in NaN. dunque df.isnull().sum() ora li rileva

un altra soluzione invece può essere:
df.replace('?', np.nan, inplace=True)
df.dropna(inplace=True)
