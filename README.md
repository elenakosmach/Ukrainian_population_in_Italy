### Ukrainian Population in Italy 2023

This project visualizes the distribution of the Ukrainian population across Italian municipalities in 2023, using data from ISTAT. The analysis and visualization were conducted using various R libraries, including `shiny`, `tidyverse`, `plotly`, `ggplot2`, `sf`, and `tmap`. The project is structured into multiple components:

1. **Data Preparation**:
   - **Population Data**: The `Municipalities.xlsx` file contains population data for each municipality. The dataset is cleaned by removing the last row and stripping extra details from the `Territory` column.
   - **Spatial Data**: Municipal boundaries are read from a shapefile (`Com01012024_WGS84.shp`). The shapefile is cleaned by removing unnecessary columns and ensuring the geometries are valid. For the latest Italian municipal boundaries updated to 2024, you can download the shapefiles by clicking the link below: https://drive.google.com/drive/folders/1eU74TKnlEF7WcdUwQu9opt_R7U5OePny?usp=sharing

2. **Data Merging**:
   - After cleaning, the population and spatial data are merged based on the municipality names to create a single dataset. Invalid and empty geometries are corrected and removed, ensuring accurate spatial representation.

3. **Bubble Map Visualization**:
   - A bubble map is created to visualize the Ukrainian population across Italy. Municipalities are grouped into population bins, and bubble sizes are mapped accordingly. This allows for easy comparison of population sizes across different regions.

4. **Interactive Shiny App**:
   - The project also includes an interactive Shiny application, allowing users to filter the municipalities based on the minimum number of Ukrainian residents. The filtered data is dynamically reflected in the map, providing a customizable view of the data.
   - http://127.0.0.1:4867/

5. **Output**:
   - The final output is an interactive map where the user can explore the distribution of the Ukrainian population in Italy. The map is also saved as a stand-alone HTML file (`Ukrainians_in_Italy_2023.html`) for easy sharing.

This project showcases how R can be used to integrate spatial data, visualize demographic distributions, and create interactive web applications with Shiny.


