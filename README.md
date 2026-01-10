# Platform-Metrics-Usage-Dashboard
Overview:

This project focuses on building a single, unified usage-metrics dashboard to help business leaders understand how analytics reports are being created and consumed across Power BI and Cognos.
The dashboard answers practical questions leadership repeatedly:
How many reports exist vs. how many are actually used?
Which reports drive value and which can be retired?
Who is creating content vs. only consuming it?
Where can we reduce maintenance and licensing costs?

Business Problem:

Initially we had usage metrics spread across four separate dashboard pages:
Power BI usage
Cognos usage
Two additional year-level summary pages

There was no way to view combined metrics, which forced users to jump between pages just to compare trends. Several visuals were no longer aligned with leadership’s current decision-making needs, but they still added clutter and noise.
As analytics adoption grew, leadership needed a clean, consolidated view that focused on decision-relevant insights, not legacy metrics.

Dashboard Goal:
The goal of this project was to:
Consolidate Power BI and Cognos usage into one decision-focused dashboard
Improve usability and navigation
Highlight metrics that directly support report rationalization and cost reduction
Enable fast identification of high-value vs. unused reports

Data Preparation & Modeling:

Connected Power BI and Cognos usage datasets into Power BI
Standardized column names and data types across both sources
Appended the datasets to create a single unified usage table
Built a clean semantic model to ensure consistent metrics across visuals
A semantic model acts as a trusted layer that defines relationships, measures, and structure so users always see consistent and accurate results.

Design Choices:
I added high-impact KPI cards such as Report Count, Report Views, Unique Users, Authors, and Consumers, and included an LOB slicer and a Smart Filter (OKVIZ) to allow instant searching of report names and corresponding usage.
To enhance usability, I applied a Top 20 filter on bar charts to avoid excessive scrolling, and created in-page navigation buttons (“Users” and “% Change”) using bookmarks, giving the dashboard an app-like navigation experience.
A semantic model is a clean, organized layer in Power BI that defines how your data is structured—tables, relationships, and measures—so that everyone sees consistent, accurate, and meaningful results in reports.
Why append instead of merge?
Append was used because the goal was to analyze all usage records together across platforms. Merge is only useful when adding columns based on matching keys.
Why standardize columns before appending?
If column names differ—even slightly—Power BI treats them as separate fields, leading to nulls and messy models. Standardization ensured a clean, reliable dataset.
Why Top 20 filters?
Without them, visuals became cluttered and required scrolling, reducing usability and insight clarity.
Why bookmarks?
Bookmarks transformed the dashboard into an interactive experience, allowing users to switch views without navigating away or loading new pages.

Questions that Dashboard Answer:
Why these KPIs?
These KPIs quickly answer the questions leadership cares about most:
How much content exists?
Is it actually being used?
Who is creating vs. consuming analytics?

Business Impact:

Enabled leadership to identify unused or low-value reports for sunsetting
Reduced dashboard noise and improved decision speed
Supported maintenance and licensing cost reduction initiatives
Improved confidence in usage metrics by providing a single source of truth

Key Insights Enabled:

Clear visibility into report sprawl vs. actual consumption
Identification of reports with high maintenance but low usage
Better understanding of creator vs. consumer behavior
LOB-specific adoption trends that were previously hidden

Intended Users:

Analytics leadership
BI platform owners
Governance and enablement teams
Anyone responsible for report lifecycle management

Dashboard Screenshot:
![Platform Metrics Usage Dashboard](https://raw.githubusercontent.com/Devisree24/Platform-Metrics-Usage-Dashboard/main/Platform%20Metrics%20Usage%20Dashboard.png)

