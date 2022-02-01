# SP500-Analysis
`` Attention: a new code trunk has been updated to the notebook. The code trunk is called Generate New Panel for Constituents with 2021 Data. This code trunk takes in data from sp500_constituent_monthly_total_rtns_2021.xlsx (bloomberg data for sp500 constituents 2021 monthly return rate), permno_aft_revise.csv for matching tick name with permno code (manually checked, coding 20 new stocks with 6-digit permno). This code generate new panel_cons.csv to include 2021 data. (Written on 02/01/2022)``
## Code
In this jupyter notebook "sp500Calc.ipynb", all code is included. 
#### For compositions:
- The first code trunk gets SP500 composites' data from WRDS. Result in sp500_cons.csv.
- The second code trunk is basically the same as code trunk 3. only that this code merges in 2021's constituents data as `` attention `` illustrates. 
- The third code trunk transfers the data into panel form, where x-axis is stock's permno code, y-axis is time (month) and monthly return rates are included. Result in panel_cons.csv.
- The fourth code trunk calculates annual return rate by compounding monthly return. Result in ann_panel.csv.
- The fifth code trunk is the first version to generate summary statistics. Results include number of positive return year, positive return month, negative return year, negative return month. Result in summary_for_cons.csv.
- The seventh code trunk summarises number of stocks going up and number of stocks going down by year and month. Result in summary_by_month.csv, summary_by_year.csv.
- The eighth code trunk, based on summary statistics from code trunk four, adds in the number of month for consecutive up period and down period. Result in summary_for_cons2.csv. 
- The nineth code trunk based on summary statistics from code trunk seven, adds in the number of positive return months and negative return months conditional on previous month's situation. Result in summary_for_cons3.csv.
#### For index:
- Code trunk 5 has the same functionalities as that for compositions. Annual return rate for SP500 is calculated and saved in index_ann.csv. Summary statistics are saved in summary_for_ix.csv.
## Data Source
- Data for composites: collected from WRDS API, monthly from 1926 to 2020. sp500_cons.csv
- Data for index: downloaded from WRDS, monthly from 1926 to 2020. index_sp500.csv
## Plots
- "monthly data.xlsx": sheet index_sp500 is from index_sp500.csv. Sheet Jan calculates stats, plots return rates in Jan. and creates chart to describe relationship between Jan. return and annual return. 
- "yearly plot.csv": data comes from index_ann.csv. Graph between annual return rate and year is plotted.
- Plots: AnnualReturn, JanReturn, JanAnnMatrix.
