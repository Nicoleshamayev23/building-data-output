To add additional data to the FINAL ORNL DATA REQUEST.csv please see the following steps.

1. Go to https://www.nyc.gov/site/planning/data-maps/open-data/dwn-pluto-mappluto.page and download the latest PLUTO data which contains info about all the buildings in NYC.

2. Open the file in excel and select the "zipcode" or "postcode" column. Then go to Data > Filter and click the dropdown button

3. Check "select all" and unselect the zipcodes you need.

4. Select all the data in the spreadsheet except the column names (use Shift+down arrow then shift+right arrow from cell A2 as a shortcut), then hit ctrl+- to delete all the rows that arent in your location range.  Note: the pluto file is very large and requires a lot of power and some time to do this. Ask Paul to work on a high speed computer for better results. Save when done computing. 

5. Go to https://overpass-turbo.eu/. Enter the following into chat gbt: "write a query in overpass turbo to select all the buildings in #### manhattan along with all their data." Replace the #### with your choice location. Multiple locations also work in turbo, just write it to chat gbt.

6. Paste the code into the left text box in overpass turbo and hit "run"
   
7. Hit "export" and select "download" next to the GeoJSON option.

8. Load the GeoJSON into QGIS
   
9. ???? how to get all correct columns in there

10. ??????

11. Export from QGIS as a csv 

12. Create a new spreadsheet and copy over the column names from FINAL ORNL DATA REQUEST.csv

13. Begin filling in the columns based on the turbo output. Note: The "WKT" column in turbo is "Footprint2D" in the FINAL ORNL DATA REQUEST.csv

14. Note the format of the values in FINAL ORNL DATA REQUEST.csv and use ctrl+H to remove any parenthesis or extra words in the cells. 

15. If the the turbo file is missing many floor values, please see the following steps

16. In the turbo file, use =CONCATENATE(H2, " ", L2) where H2 is the addr:housenumber column and L2 is the addr:street to merge the entire address of a building into one cell. Use this full address to paste into your new csv file.

17. Use a vlookup equation to fill in the missing floor value cells referencing the the cleaned pluto data. Note a vlookup equation

