# Apartment Analysis around KL & Selangor

This project demonstrates a simple analysis on apartment around KL and Selangor. There report will be shown in PowerBi and clean by pandas.  

**(Disclaimer: Material used for educational purpose)**

![tittle](https://images.pexels.com/photos/439391/pexels-photo-439391.jpeg)

**Business Goal:**
- Foresee risk property investment 

**Consumer Goal:**
- Affordable house rent

## Explore Data
Tools involve:
- pandas
- PowerBi

Data involve:
```bash
'prop_name
'rent'
'rent_type'
'region'
'district'
'property_type'
'rooms','parking'
'bathroom'
'size'
'furnished_rate'
'facilities_rate'
```

### Schema answer:

#### Foresee risk property investment 
- **Property Condition:**
    Age of the property (2025 - completion year): new, moderate, and old

    | Year     | Price (RM) (annually)     |
    | :-------- | :------- |
    | `0–10` | `2.25 per sq. ft.` | 
    | `10–20` | `4.49 per sq. ft.` | 
    | `20+` | `8.99 per sq. ft.` |


- **Rental Market Risk:**
    
    Competition (number of similar rental properties)
    
    Vacancy rates (how many rental units are empty).
    `Column chart`

#### Affordable house rent
- Rental Prices: 
    Current and historical rental rates. Average rent per square foot/meter
- Income Data:
    Median household income by area
- Market Segmentation: 
    Helps identify areas that cater to specific income groups (affordable, steady, luxury). `Histogram chart`

    | Type     | Formula |
    | :-------- | :------- |
    | `Affordable` | `Total rent * Q1` | 
    | `Steady` | `Total rent * Q2` | 
    | `Luxury` | `Total rent * Q3` |
Rent-to-Income Ratio=(Monthly Rent/Monthly Household Income
 )×100

- Property Features:
Size and type of rental units
Included utilities or amenities
Transportation Accessibility:
Proximity to public transport and major roads
Cost of Living:
Average monthly expenses in the area (utilities, groceries, healthcare)