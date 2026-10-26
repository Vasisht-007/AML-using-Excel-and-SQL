# AML-using-Excel-and-SQL
A small rule-based system that flags transactions that could be linked to money laundering, built on ~52,000 bank transactions (2022 to 2025).

What I did
Cleaned the data in Excel: removed 624 duplicates, fixed inconsistent spellings, and converted five currencies to euros.
Scored every transaction with four red flags, one point each:
Amount over €40,000
Amount just under the limit (€9,000 to €10,000), a common way to dodge reporting thresholds
Failed or manual-review AML check
Transaction on a closed, frozen or dormant account
Labelled 2+ points as "high risk", since one flag can be a coincidence but two deserve a look.
Built an interactive Power BI dashboard with KPIs, yearly trend, city chart, risk split and a top high-risk table, filterable by year, city, risk level and customer type.
Key findings
14,218 transactions (27.3%) were high risk, worth about €520M (~40% of all value).
Inactive-account activity and failed AML checks were the strongest drivers, each about 6x more likely to be high risk.
Results were very even across years, cities, channels and customer types.
Limitations

About half the transactions were marked "fraud", far above any real bank, and almost every customer had just one transaction. The dataset is likely synthetic, so this shows the method works, not that real laundering occurred. The rules also look at one transaction at a time and depend on my chosen exchange rates.
