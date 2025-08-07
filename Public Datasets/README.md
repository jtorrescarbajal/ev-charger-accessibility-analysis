# Data Directory: EV Charger Accessibility Analysis

This folder contains all the public datasets used for the EV charger accessibility capstone project. All sources are publicly available, cited in the main README and paper.

## EV Registration Data

### `WA_Electric_Vehicle_Population_Data.csv`  
- **Source:** Washington State Department of Licensing  
- **URL:** https://catalog.data.gov/dataset/electric-vehicle-population-data  
- **Description:** ZIP-level count of registered EVs in Washington as of 2025.  
- **Use:** Used as a proxy for local EV demand in the model.

### `ODOT-EV-Data.csv`  
- **Source:** Oregon Department of Energy  
- **URL:** https://www.oregon.gov/energy/Data-and-Reports/Pages/Oregon-Electric-Vehicle-Dashboard.aspx  
- **Description:** County-level EV registration data; ZIP-level approximated manually.  
- **Use:** Incorporated to estimate EV ownership for Oregon ZIP codes.

### `CA_Vehicle_Population_Last_updated_04-30-2025_ada.csv`  
- **Source:** California Energy Commission  
- **URL:** https://www.energy.ca.gov/files/zev-and-infrastructure-stats-data  
- **Description:** ZIP-level statistics on Zero Emission Vehicles and chargers.  
- **Use:** Used to gather EV ownership and public charger counts in California.

## Public Charger Locations

### `alt_fuel_stations.csv`  
- **Source:** U.S. Department of Energy AFDC  
- **URL:** https://afdc.energy.gov/data_download  
- **Description:** Contains locations and attributes of public EV chargers in the U.S.  
- **Use:** Filtered for CA, OR, WA; aggregated to ZIP code level for modeling.

## Demographic & Geographic Data

### Various 
- **Source:** U.S. Census Bureau, American Community Survey  
- **URL:** https://data.census.gov  
- **Description:** ZIP-level data including population, income, and renter/homeowner rates.  
- **Use:** Predictor variables for modeling EV charger need.

### `RUCA2010zipcode.csv`  
- **Source:** USDA ERS RUCA ZIP Approximation File  
- **URL:** https://www.ers.usda.gov/data-products/rural-urban-commuting-area-codes/  
- **Description:** Categorizes ZIP codes as urban or rural.  
- **Use:** Binary `is_Urban` variable used in the model.

## Processed / Derived Data

### `Model_Dataset.csv`  
- **Description:** Final cleaned dataset used for modeling. Includes transformed columns like log population, EVs per 1,000 residents, and charger-to-EV ratio.  
- **Use:** Input for training and testing the machine learning model.

---

## Notes

- All data was accessed between **July–August 2025**.
- Datasets were filtered to include **only ZIP codes in California, Oregon, and Washington**.
- Sensitive information was not used; all data is public.

