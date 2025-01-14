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
prop_name
rent
rent_type
region
district
property_type
rooms
parking
bathroom
size
furnished_rate
facilities_rate
```

### Schema answer:

#### Foresee risk property investment 
- **Property Condition:**
    Age of the property (2025 - completion year): new, moderate, and old
    
    Maintanance fee accomandate:
    | Year     | Price (RM) (annually)|
    | :-------- | :------- |
    | `0–10` | `2.25 per sq. ft.` | 
    | `10–20` | `4.49 per sq. ft.` | 
    | `20+` | `8.99 per sq. ft.` |

    Formula = age (current - completion) * price

    X, Y: property_type , completion_rate

    `Column chart`

- **Rental Market Risk:**
    
    Competition (number of similar rental properties):
    
    ↗ similiraty, ↗ Risk

    X, Y: property_type , competition_rate

    Vacancy rates (how many rental units are empty):

    ↗ vacancy, ↗ Risk (oversupply) 

    X, Y: district , vacancy_rate

    `Column chart`

#### Affordable house rent
- **Rental Prices:** 
    Current rental rates. Average rent per square foot/meter
- **Income Data:**

    Median household income by area

    X, Y: district , median_rent
    
    `Demographic chart`    

- **Market Segmentation:**

    Helps identify areas that cater to specific income groups (affordable, steady, luxury).

    Formula: 
    ![alt text](./img/formula1.png)
    
    > - less 30%: Rent is generally considered affordable.
    > - 30%-50%: Rent is becoming burdensome.
    > - Above 50%: Rent is considered highly unaffordable and may indicate financial stress.

    | Type     | Income (RM) |
    | :-------- | :------- |
    | `Affordable (B40)` | `less 4849` | 
    | `Steady (M40)` | `4850 - 10959` | 
    | `Luxury (T20)` | `10960 more ` |

    X, Y: district , income_group

    `Histogram chart`

- **Property & Facilitiy Features:**

    Size and type of rental units included utilities or amenities

    X, Y: district , income_group

    `Histogram chart`

## Implementation
