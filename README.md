# Lab 3: Variance, Correlation, and Covariance in the UBC Weather Station Data

## **Purpose**

In this lab I analyze local (UBC weather station) and global temperature anomaly time-series for the period between 1950-2017. 

In this lab, I utilize linear regression analysis to ask the following three questions regarding the local and global temperature time-series.

1. Is there a trend in the temperature time series?

2. Are the temperature time series correlated with specific internal or external climate forcing (e.g. atmospheric CO2, El Nino oscillation)?

3. Do your results support the claim that there is a global warming trend and that it is caused by increased CO2 concentrations in the atmosphere?

## **My Learning Goals**

- Be able to perform simple linear regression and multiple linear regression analysis in Python.
- Use statistical measures such as coefficients of determination and linear regression coefficients to describe relationships between time-series.
- Evaluate the importance of different factors in explaining the variability of this time-series.
- Assess whether my visualizations allow me to make conclusions about specific hypotheses.

## **Notebook contains**

1. One figure containing the raw time-series of the 7 variables, with linear regression for both temperature time-series (PART 1 & 2)
2. One figure containing histograms of temperature before/after 1985 for local (UBC) and global temperatures (PART 3)
3. One figure containing a scatterplot of the UBC temperature against the global mean temperature (PART 5)
4. The `Lab3_results_spreadsheet` with Table 1 and Table 2 filled with regression results (PART 6 & 7)
5. `table_1.png` and `table_2.png` image contain same results from spreadsheet
6. One figure containing a scatterplot of global mean temperature anomaly against temperature predicted by a multiple linear regression of the 5 forcing variables (PART 8)
7. Analysis at the end
 
### **1. The Data**
`lab3_data.xlsx` data file contains time-series data for the following 8 variables:

1. **The date**, formatted as a *decimal year* (decimal year = year + month/12). For example, June 2000 would be “2000.46”.

2. **UBC air temperature anomaly**. This data was recorded at the UBC weather station. The anomaly is relative to the 1961-1990 mean seasonal cycle and is expressed in degrees Celsius.

3. **Global mean air temperature anomaly**. This data was collected by the Climate Research Unit. Anomaly is also relative to the 1961-1990 mean seasonal cycle and is expressed in degrees Celsius.

4. **Total solar irradiance (TSI)**. These values represent the flux of solar energy entering through the top of the atmosphere in W/m<sup>2</sup>. This data comes from the SATIRE project (monthly means) and from Lean et al. (2000) (yearly means), which have been combined to obtain monthly TSI over the 1950-2016 period.

5. **Global mean stratospheric aerosol optical depth (AOD)**. The AOD is a dimensionless value that represents the concentration of aerosols suspended within the atmosphere (particulate matter, smoke, salt, dust etc.). This data was obtained from the Goddard Institute for Space Study. A constant value was assumed for the period 2012-2016 for which no data was available.

6. **Atmospheric CO2 concentration**. This data was obtained from the Earth Policy Institute and is expressed in units of ppm, (parts-per-million).

7. **Anthropogenic SO2 emissions**. This data was obtained from the Pacific Northwest National Laboratory and is expressed in units of Tg/year (Teragrams/year, i.e. 10^9 kilograms/year).

8. **Multivariate ENSO Index (MEI)**. The MEI is a dimensionless variable that is positive during El Niño, and negative during La Niña, phases of the El Niño-Southern Oscillation.
