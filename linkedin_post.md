# DataDNA November 2026: entry write up

**How to enter (from the challenge rules):**
• Post on LinkedIn with **one image** of the report. Use `page1_executive_summary.png`.  
• Tag **@Onyx Data**, **@SmartFrames UI**, **@Data Career Jumpstart** and **@Packt**, and use **#dataDNA**. Type the @ and pick each page from LinkedIn's list so the tags link properly.  
• Then fill in the entry form on the challenge page with the link to your post. One entry per person. Deadline: 24 November.

## LinkedIn post

Every health system cleared its pandemic backlog. Except the UK's.

This is my entry for the #dataDNA November challenge from @Onyx Data: 32 countries, 212 regional health systems and 28 quarters of data (2018 to 2024), written up as a report for a policy unit's board.

Here's what the data says.

📈 The shock came in two waves. ICU occupancy jumped 9.5 pts in the acute phase, but emergency care broke down later. ED 4 hour performance hit its low of 64.6% in 2022 Q3, during recovery, not at the height of the pandemic.

⏳ Waits nearly doubled everywhere. In 2021 elective waits were 1.88× their 2019 level, and 20 of 32 countries rose by about the same amount. Sweden, Norway, Denmark, Finland and Germany were back to 1.07× by the second half of 2022.

🇬🇧 The UK never came back down. In 2024 its waits were still 1.99× the 2019 level, when no other country was above 1.67×, and 1.35× the EU average. The UK also spends 13.7% less per person than EU members.

👩‍⚕️ Staff are part of the story. Burnout peaked in 2022 and moves with vacancies (r = 0.58, or 0.73 within countries). UK vacancies run at 1.66× the EU rate, and UK burnout is falling half as fast as in other high income countries.

🩺 Recorded heart disease and diabetes rise steadily in every WHO region. Recorded cancer falls 1.8% a year in low income countries, which looks like a detection gap rather than good news.

My recommendation to the board: a UK elective recovery plan tied to staff retention, with burnout tracked as an early warning for vacancies.

How I built it:
• Power BI: Power Query, a star schema (with the inactive relationship the brief asked for) and 76 DAX measures. Averages instead of sums, UK vs EU as two CALCULATE measures, trend slopes with LINESTX and correlation with SUMX  
• A blue theme with my own icons, 6 pages, and method notes behind every number  
• A Python version (pandas, NumPy, matplotlib) built from the same raw files. It checks the data first, then works out all 22 headline figures again. All 22 match the report.

The full project, the .pbix and the notebook are linked in the comments 👇

Synthetic data from the DataDNA November 2026 challenge.

Thanks to @SmartFrames UI, @Data Career Jumpstart and @Packt for supporting the challenge.

#dataDNA #PowerBI #DAX #DataAnalytics #Python #HealthcareAnalytics #DataVisualization #OpenToWork

## First comment

🔗 The project (Power BI .pbix, DAX and the Python notebook): https://github.com/bamidele-yetunde/DataDNA_Health_System_Performance

## Entry form text

**Portfolio or project title:**
Every health system cleared its elective backlog, except the UK's

**Short description:**
A 6 page Power BI report for a board, covering 32 countries and 212 regional health systems from 2018 to 2024. It looks at the pandemic shock in acute care, how elective backlogs recovered (the UK against the EU and the Nordics), health spending, pressure on the workforce, and long running disease trends. It is built on a star schema with 76 DAX measures: averages rather than sums, the UK and the EU as separate CALCULATE measures, LINESTX trend slopes and SUMX correlations. A method notes page gives the measure, filter and period behind every headline number. I also rebuilt it in Python (pandas) from the same raw files, and all 22 headline figures match exactly.

**Tools used:** Power BI (Power Query, DAX, data modelling); Python (pandas, NumPy, matplotlib) as a cross check.
