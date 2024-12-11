# Solar-Wind-Data-Analysi
Solar Wind Data Analysis - Correlation Between Solar Wind Speed and Proton Density

README

Solar Wind Data Analysis

This repository contains a Python script for analyzing solar wind data from the OMNI dataset. The script processes daily data, applies linear regression, and computes Pearson correlations for different solar cycles.

Files in Repository

omni_m_daily.dat: The dataset containing daily OMNI solar wind data.

solar_wind_analysis.py: The Python script for data processing, visualization, and analysis.

Description of the Script

1. Data Loading and Cleaning

Input File: The OMNI dataset (omni_m_daily.dat).

Column Specifications:

Column widths and names are predefined based on the OMNI dataset format.

Placeholder values (e.g., 999.9, 9999.0, 9999999.0) are replaced with NaN for cleaning.

Rows with NaN in Bulk_Flow_Speed or Proton_Density are dropped to ensure meaningful analysis.

2. Functions in the Script

filter_by_solar_cycle(data, start_year, end_year):
Filters the dataset for a given range of years corresponding to a solar cycle.

linear_fit(x, m, c):
Defines a linear function (y = mx + c) for fitting purposes.

plot_and_calculate(data, title):

Creates a scatter plot of Bulk_Flow_Speed vs. Proton_Density.

Fits a linear regression line to the data.

Calculates the Pearson correlation coefficient.

Displays the plot with annotations, titles, and grid lines.

analyze_solar_cycles(data, cycle_periods):
Iterates over defined solar cycles, filters the data, and performs analysis using the above functions. Returns Pearson correlation coefficients for each cycle.

3. Solar Cycle Periods

The script allows flexible analysis of solar cycles. Currently defined periods:

Solar Cycle 23: 1996-2008

Solar Cycle 24: 2009-2019

Additional cycles can be added by updating the solar_cycles dictionary.

4. Output

Scatter plots with linear regression lines and Pearson correlation coefficients.

Correlation results printed in the console.

Instructions to Use

Prerequisites:
Ensure the following Python libraries are installed:

pandas

numpy

matplotlib

scipy

Run the Script:

python solar_wind_analysis.py

Input File:
Place the omni_m_daily.dat file in the same directory as the script or update the file_path variable in the script to point to its location.

Modify Solar Cycle Periods:
Update the solar_cycles dictionary to include additional or custom periods.

Example Output

Scatter plot: Bulk Flow Speed vs. Proton Density for Solar Cycle 23.

Console Output:

Solar Cycle 23 Pearson Correlation: 0.85
Solar Cycle 24 Pearson Correlation: 0.78

Contributions

Feel free to contribute by:

Adding new features or solar cycle periods.

Reporting bugs or suggesting improvements.

License

This project is licensed under the MIT License.

