# Drinking Water Access in The World - Dashboard
-	[Overview](#overview)
-	[Results](#results)
#
### Overview
The Drinking Water Access dashboard shows global data on how countries around the world have gained access to safe drinking water and improved sanitation from 2015 to 2024. It also highlights progress in drinking water services including  basic, limited, surface water, and safely managed, which have changed each year across different continents.

#
##### Data Source:
* Yale University
* WHO and UNICEF
* Map Shape: https://github.com/Rizka-F/World-Map-241-Country
#
##### Tools:
* Microsoft Excel: Data Cleaning, Query
* PowerBI: Visualisation
#
### Results
##### This dashboard is divided into two main pages there are,  "Drinking Water and Sanitation Index" page and the "Water Service" page.
- The "Drinking Water and Sanitation Index" page shows progress data about drinking water and sanitation in every continent and sub-continents each year
- The "Drinking Water Services" page shows data about improvement in drinking water services across every continent.
  To support the world data visualisation, I created a separate table specifically for the world data, independent from the main dataset.
```DAX
World drinking water access table =
SELECTCOLUMNS(
    FILTER(
        'at least basic_safely world',
        'at least basic_safely world'[COUNTRY, AREA OR TERRITORY] = "WORLD"
    ),
    "Country", 'at least basic_safely world'[COUNTRY, AREA OR TERRITORY],
    "Year", 'at least basic_safely world'[Year],
    "At least basic", 'at least basic_safely world'[At least basic],
    "Basic", 'at least basic_safely world'[Basic],
    "Limited", 'at least basic_safely world'[Limited],
    "Surface water", 'at least basic_safely world'[Surface water],
    "Unimproved", 'at least basic_safely world'[Unimproved],
    "Safely managed", 'at least basic_safely world'[Safely managed]
)
```
##### Map Shape
For the map visualisation in the "Drinking Water and Sanitation Index" page, I used a GeoJSON file from maps.kyd, which includes 241 countries. The map colouring in the dashboard reflect data values for the year 2024. 

##### Tooltips
I created a tooltip page for the “Drinking Water and Sanitation Index” section. This tooltip displays both the drinking water index and sanitation data for each country. When the cursor points to a specific country, the tooltip automatically shows that country’s data.
Meanwhile, for the “Drinking Water Services” page, I used the default tooltip provided by Power BI.
#
* Drinking Water and Sanitation Index Page
  - Main Page of Water and Sanitation Index
    <img width="1533" height="859" alt="ichasoegit1w" src="https://github.com/user-attachments/assets/ec2bf790-9e2d-4615-9ec8-e9ec5a1bd0c3" />
    
 
  - Continent-Sub and Year Slicer
    <img width="1529" height="853" alt="ichasoegit2w" src="https://github.com/user-attachments/assets/6c592070-6f9d-4bcf-96a2-6c3cdf10ac38" />
    

  - Tooltips on Drinking Water and Sanitation Page
    <img width="1437" height="811" alt="ichasoegit5w" src="https://github.com/user-attachments/assets/d9b3e4f5-e60a-41f6-b26e-4369bef245df" />
    <img width="1447" height="805" alt="ichasoegit7w" src="https://github.com/user-attachments/assets/929af329-256b-4b1c-8edf-1fe6424fa478" />
    <img width="1443" height="809" alt="ichasoegit6w" src="https://github.com/user-attachments/assets/f391d699-0474-430b-a8ff-7dc607a56fd2" />
#
* Drinking Water Services Page
  - Main Page of Water Services
    <img width="1439" height="805" alt="ichasoegit10w" src="https://github.com/user-attachments/assets/a11501a6-c46c-4e7f-a272-18ba20f8c997" />

    
  - Continent Group and Year Slicer
    <img width="1539" height="855" alt="ichasoegit4w" src="https://github.com/user-attachments/assets/224fce85-211f-4e31-9210-2914113ba536" />
    
    
  - Tooltips on Drinking Water Services Page
    <img width="1537" height="859" alt="ichasoegit3w" src="https://github.com/user-attachments/assets/f19dc11f-3731-4ea8-825c-09894ccbdccb" />
    
    <img width="1443" height="811" alt="ichasoegit9w" src="https://github.com/user-attachments/assets/c4fb5f47-7c49-4906-8ec3-072865a6b151" />

    <img width="1445" height="807" alt="ichasoegit8w" src="https://github.com/user-attachments/assets/456453aa-c557-46ab-ab22-83591e77fc6f" />



  
