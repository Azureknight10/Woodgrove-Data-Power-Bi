# Data Dictionary – Woodgrove Ads

## dim_date
- **Grain**: One row per calendar date.
- Columns:
  - DateKey (int, e.g., 20240131)
  - Date (date)
  - Month (string, e.g., "Jan")
  - MonthNumber (int)
  - Quarter (string, e.g., "Q1")
  - Year (int)

## dim_account
- **Grain**: One row per customer account.
- Columns:
  - AccountId (int)
  - AccountName (string)
  - Region (string, e.g., "North America")
  - Industry (string)

## dim_rep
- **Grain**: One row per sales rep.
- Columns:
  - RepId (int)
  - RepName (string)
  - ManagerName (string)
  - Region (string)

## dim_product
- **Grain**: One row per ad product.
- Columns:
  - ProductId (int)
  - ProductName (string, e.g., "Microsoft Search Ads")
  - Channel (string: "Search", "Display", "Video")

## fact_opportunity
- **Grain**: One row per opportunity.
- Columns:
  - OpportunityId (int)
  - AccountId (int, FK → dim_account)
  - RepId (int, FK → dim_rep)
  - ProductId (int, FK → dim_product)
  - CreatedDate (date)
  - CloseDate (date, nullable)
  - Stage (string, e.g., "Qualified", "Proposal", "Negotiation", "Closed Won", "Closed Lost")
  - Amount (decimal, potential revenue)
  - IsWon (boolean)

## fact_revenue
- **Grain**: One row per booking/revenue transaction.
- Columns:
  - BookingId (int)
  - AccountId (int, FK → dim_account)
  - RepId (int, FK → dim_rep)
  - ProductId (int, FK → dim_product)
  - BookingDate (date)
  - RevenueAmount (decimal)

## fact_campaign_perf
- **Grain**: One row per account–product–day campaign performance.
- Columns:
  - CampaignId (int)
  - AccountId (int, FK → dim_account)
  - ProductId (int, FK → dim_product)
  - Date (date, FK → dim_date)
  - Impressions (int)
  - Clicks (int)
  - Spend (decimal)
  - Conversions (int)
  - RevenueAttributed (decimal)
