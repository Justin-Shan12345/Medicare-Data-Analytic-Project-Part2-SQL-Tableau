# Medicare Data Analysis and Dashboard Part 2

## Table of Contents
1. [Introduction](#introduction)
2. [Tools Used and Dashboard Preview](#tools-used-and-dashboard-preview)
3. [Limitations](#limitations)

## Introduction
This is a continuation of the Medicare Data Analysis and Dashboard project. In part 2, a dashboard is created using HCPCS code as the focal point for the analysis. This Medicare HCPCS Code Search Dashboard allows users to explore Medicare claim data associated with HCPCS codes and generate insights regarding claim sizes across the United States.

Key Features:
1. Search by HCPCS Code or State: The top section of the dashboard allows users to select a specific HCPCS code or a state to filter the data and focus the analysis on particular regions or procedures.
2. Total Claim Cost Overview: The dashboard provides a summary of the total claim cost across all states, highlighting the overall scale of Medicare claims for the selected HCPCS codes.
3. Number of Healthcare Providers (HCPs): A summary figure indicates the total number of HCPs (healthcare providers) with claim records for the selected HCPCS codes, giving insight into how many providers are associated with these claims.
4. Map Visualization: The map in the middle of the dashboard visually represents the total claim size by state using a color gradient. States with higher total claims are shown in darker shades of blue, allowing for easy geographical comparison.
5. Claim Ranking by State: A table ranks each state by the total claim amount, helping users identify which states have the largest or smallest claim volumes. For example, California (CA), Florida (FL), and Texas (TX) are among the states with the highest total claims.
6. Top 50 HCPs by Claim Size: Another section of the dashboard displays the top 50 healthcare providers by total claim size, showing relevant information such as the provider's name, type, state, city, and total claim amount. This feature helps users see which providers are driving the largest claim amounts in the system.
7. Adjustable Filters: Users can adjust the number of top HCPs displayed and choose to view data for all HCPCS codes or specific ones, providing flexibility in the analysis.

Purpose:
This dashboard is designed to enable users, such as analysts, policymakers, or healthcare providers, to quickly and visually explore Medicare claims data, identify trends, and gain insights into the distribution of claims related to specific medical procedures across the U.S. The geographic and provider-based breakdowns make it useful for assessing the financial landscape of Medicare-funded healthcare services.


**Please refer to Part 1 for details on data cleaning and preparation using the link below**： 
https://github.com/Justin-Shan12345/Medicare-Data-Analytic-Project---SQL-Tableau

**Link to dashboard**: https://public.tableau.com/app/profile/chung.hsi.shan/viz/MedicareDashboard-HCPCScodesearch/Dashboard1#1

**Link to dataset**: https://data.cms.gov/provider-summary-by-type-of-service/medicare-physician-other-practitioners/medicare-physician-other-practitioners-by-provider-and-service

## Tools Used and Dashboard Preview
- **PostgreSQL**: Used for all data cleaning, transformation and analysis.
- **Tableau**: Dashboard creation and data visualization.
- Below is a screenshot taken from the Dashboard, which is created using Tableau:

![Dashboard 1 (2)](https://github.com/user-attachments/assets/8ace2235-1796-4c4b-9c5e-030b6bac1cb5)


## Limitations
- Only Medicare Part B (Outpatient Services) non-institutional claims (excluding
DMEPOS) are used for the creation of the dashboard, meaning Part A (Inpatient
Services), C (Medicare Advantage Plan), and D (Prescription Drug Coverage) part of
Medicare was not included, thus the analysis can only be generalized to Part B of
Medicare.
- The dataset only includes healthcare providers who are not affiliated with an
institution. 
- To protect the privacy of Medicare beneficiaries, any aggregated records that are
derived from 10 or fewer beneficiaries are excluded. Therefore volume HSPCS codes are
not part of the analysis and the total sum calculated may be a slight underestimation
of the true Medicare Part B totals.
- Due to the dataset size limit on Tableau Public, only the following provider specialties are selected (Rheumatology, Neurology, Endocrinology, Hematology, Pediatric Medicine, Medical Genetics and Genomics)
- Private insurance and other insurance claims are not taken into account in the analysis.
- Some providers bill under both an individual NPI and an organizational 
NPI. In this case, users cannot determine a provider’s actual total because there is
no way to identify the individual’s portion when billed under their organization.
- For the limitations listed above, the data do not represent a healthcare provider's
entire practice. 
