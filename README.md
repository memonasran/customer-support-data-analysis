Customer Support Ticket Analysis

Analysis of customer support tickets using Excel, SQL, Python, and Power BI.

Files
data/raw/tickets.csv
data/raw/teams.csv
excel/analysis.xlsx
sql/setup.sql
sql/queries.sql
python/analysis.py
powerbi/dashboard.pbix
outputs/

Dataset

13 ticket rows including 1 duplicate → 12 clean rows

4 teams

Lookup key: team_id

SLA breach: resolution_hours > 24

Month order: Jan → Feb → Mar

SQL

Dialect: SQLite 3.x

Run:

sql/setup.sql
sql/queries.sql


Queries cover department averages, SLA-breaching teams, top breach channels, and data integrity.

Python

Run from the repository root:

python python/analysis.py


Outputs:

outputs/python_chart.png
outputs/clean_data.csv
outputs/python_summary.csv

Power BI

Open:

powerbi/dashboard.pbix


Sources:

data/raw/tickets.csv
data/raw/teams.csv


Relationship:

teams[team_id] 1 → * tickets[team_id]


Use Home → Refresh to update the dashboard.

Excel

excel/analysis.xlsx contains Raw, Lookup, Clean, and Summary sheets with duplicate removal, XLOOKUP, breach calculation, and PivotTable analysis.

Reconciliation

Results were cross-checked across Excel, SQL, Python, and Power BI using the same 12 clean records.
