# Data sources for the indicators featured in "Towards scenario representation of adaptive capacity for global climate change assessments" 


## GDP data (Crespo Cuaresma, 2017; Dellink et al., 2017; Leimbach et al., 2017, Koch and Leimbach, 2021)
For the original set of the SSP scenarios, GDP projections were developed by three parallel efforts that used different underlying economic theories. In this repository they are provided both as total GDP (**gdp.xlsx**) or per capita (**gdp_per_capita.xlsx**). The three estimation models are labeled as: 
* IIASA GDP (Crespo Cuaresma, 2017)
* OECD Env-Growth (Dellink et al., 2017)
* PIK GDP-32 (Leimbach et al., 2017).

Note that the PIK GDP-32 is not available on the country, but on the regional level for 32 regions.

GDP projections can also be directly downloaded from the [SSP database](https://tntcat.iiasa.ac.at/SspDb/dsd?Action=htmlpage&page=10). 

Additionally, the repository contains a data file with updated GDP projections. As part of the [NAVIGATE project](https://www.navigate-h2020.eu/navigator/apply/), a working paper by [Koch and Leimbach (2021)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4011838) presented an update of the SSP projections of GDP per capita wich now incorporate changes in national accounting and PPP conversion incorporated, and the Covid-19 impacts reflected (**gdp_update_2021.xlsx**; variable gdppc).

## Structural change (Leimbach et al., 2023)
Also in the context of the [NAVIGATE project](https://www.navigate-h2020.eu/navigator/apply/), Leimbach et al. (forthcoming) have developed scenarios of economic structural change within the SSP framwework. Of relevance for adaptive capacity are the sectoral shares of employment, covering agriculture, manufacturing and employment. The variables are projected until 2050 and can be found in the **gdp_update_2021.xlsx**, the sectoral employment shares represented by indicators "agr_emp" (agriculture); "man_emp" (manufacturing) and "ser_emp" (service).

## Extreme poverty (Crespo Cuaresma et al., 2018)
The paper calculates poverty patwhays wihtin the SSP scenarios up to the year 2030. The estimation model combines estimates of the worldwide distribution of income and macroeconomic projections of population by age and educationa, as well as income per capita. The indicators are expressed as absolute population affected by extreme poverty (defined as living on less than $1.90 a day, measured in 2011 PPP prices), and the corresponding annual GDP per capita is also provided in the file **extreme_poverty.csv**.

## Remittances (Benveniste et al., 2021)
This paper highlights where and to what extent migration affects projections of income and inequality. Flows of remittances are estimated as part of that effort, using data on the share of income sent as remittances (which is kept constant over time) and costs of sending remittances. Using bilateral remittance estimates, bilateral estimates of migrant stocks and per capita GDP, the authors are able to estimate remittances for origin/destination pairs or on the country level, which is what is provided in this repository under the name **remittances.csv**.

## Income inequality (Rao et al., 2019)
This study combines projections of GDP with assumptions of trajectories of within-country Gini coefficients to derive possible trajectories of income distributions in the SSPs. The econometric model used here is a linear combination of the total factor productivity, educational atttainment, non-resource trade, the labor share of income, and policy variables. The sum-product of the coefficient estimates and the projections of their corresponding explanatory variables from the model are then used to project the income Gini. The data can be found in the file **inequality_gini.xlsx**.

## Urbanization (Jiang and O'Neill, 2017; Chen et al., 2022) 
Expressed as the proportion of the total population that is urban, urbanization projections by Jiang and O'Neill were part of the original set of SSPs. They were modeled as a linear relationship between the difference in urban and rural population growth rates and urbanization level (similar to the UN approach, but modified so that the relationship is estimated separately for each country. The data from Jiang and O'Neill is available in the file **urbanization_2017.xlsx**

The projections were recently updated by Chen et al. They are based on an S-shaped logistic method, based on the findings from previou studies that an S-shaped curve represents three stages of the urbanization process: the initial stage, the growth stage and the mature stage. The historical model is calibrated on two datasets: from the UN Population Prospects and from the World Bank. The data is available in the file **urbanization_2022_wup.csv** and **urbanization_2022_wb.csv**

In both sets of projections, data for countries whose land areas are smaller than 1000 km^2 and populations in 2010 less than 1 million persons are dropped from the sample. 

## Governance, government effectiveness and corruption (Andrijevic, 2019)
Based on the [Worldwide Governance Indicators (WGI)](https://info.worldbank.org/governance/wgi/) and using an econometric approach for panel data, this paper estimates projections of governance indicator for the SSP scenarios. The model is expresses governance as a function of GDP per capita, share of population with secondary education and gender gap in mean years of schooling. The WGI indicator can be used as a composite indicator with six underlying dimensions, or the dimensions can be used as standalone indicators. This paper delivers projections of the composite indicator and of two underlying components, namely government effectiveness (gov.eff) and control of corruption (corr.cont), all of which can be found in the file **governance.csv**

## Rule of law (Soergel et al., 2021)
As part of a study on sustainable development pathways and projections of progress towards the SDG, projections of an indicator of the quality of rule of law were made with the aim of measuring SDG 16. Authors calculate the projections using linear fixed-effects regression models with education, population and GDP as the predictors. The work of Andrijevic et al. (2019) here was extended by using a different indicator and by including the endogenous effects of mitigation costs and international transfers on GDP per capita. Rule of law indicator can be found in the file **rule_of_law.csv**. 

## Population and education (KC and Lutz, 2017) 
Demographic data is available at the [website](http://dataexplorer.wittgensteincentre.org/wcde-v2/) of the Wittgenstein Centre for Demography and Global Human Capital  or can be directly loaded in R with the package [wcde](https://cran.r-project.org/web/packages/wcde/index.html) (Abel et al., 2022). The data is available for the historical period from 1950 or as projections for SSPs 1,2 and 3
Indicators of interest suggested in the context of human capacity dimensions of adaptive capacity are, for example: 
* population size; in the wcde package "pop"
* age strcuture (population size by broad age); in the wcde package "bpop" 
* distribution of educational attainment (also disaggregated by sex and age); in the wcde package "prop"
* mean years of schooling (also disaggegated by sex and age); in the wcde package "mys"

## Human Development Index (Crespo Cuaresma and Lutz, 2015)
This paper mamkes use of the advances in demographic and economic projections in the SSPs, to combine the future pathways of life expectancy, education and income into a projected version of the Human Development Index (HDI) of the United Nations Development Programme (2013). The HDI has been computed following the same formula as used by the UNDP, namely the geometric mean of the three dimensions: health (life expectancy), education (geometric average of actual and expected educational attainment measured by years of schooling) and income (gross national income (GNI) per capita). The data is available in the file **hdi.csv**. 

## Migration Flows (Benveniste et al., 2021)
Estimates of migration flows are part of the same study by Benveniste et al. (2021) as the remittances flows suggested here as an indicator relevant for the economic dimension of adaptive capacity. Migration flows are implicit parts of the SSP population projections (KC and Lutz, 2017), while in this stud they are made explicit with the use of a gravity model (Jones and O'Neill, 2016) that summarizes the quantative effects of push and pull factors on migration flows. The data included in the **migration_flows.csv** file is available on the country level, expressed as absolute number of migrants (in '000).

## Gender Inequality Index (Andrijevic et al., 2021)
Based on the Gender Inequality Index (GII) from the UNDP, this study provides future trajectories of the indicator. Specficially, the GII indicator is a geometric average of three dimensions: health (measured by maternal mortality and adolescent birth rate), empowerment (%  of women in parliament and secondary education) and labor market (labor force participation). The GII is then modeled as a function of GDP, education and gender gap in education, which allows for internally-consistent projections along the five SSP scenarios. The indicator is expressed on a scale from 0 to 1. It is available in **gii.csv**

## Gender gap in mean years of schooling (KC and Lutz, 2017)
data is available at the [website](http://dataexplorer.wittgensteincentre.org/wcde-v2/) of the Wittgenstein Centre for Demography and Global Human Capital as the variable **gender gap in mean years of schooling** or can be directly loaded in R with the package [wcde](https://cran.r-project.org/web/packages/wcde/index.html) (Abel et al., 2022) where the variable is called **ggapedu15**. 

### References
1.	Crespo Cuaresma, J. Income projections for climate change research: A framework based on human capital dynamics. Global Environmental Change 42, 226–236 (2017).
2.	Dellink, R., Chateau, J., Lanzi, E. & Magné, B. Long-term economic growth projections in the Shared Socioeconomic Pathways. Global Environmental Change 42, 200–214 (2017).
3.	Leimbach, M., Kriegler, E., Roming, N. & Schwanitz, J. Future growth patterns of world regions – A GDP scenario approach. Global Environmental Change 42, 215–225 (2017).
4.	Koch, J. & Leimbach, M. Update of SSP GDP projections: capturing recent changes in national accounting, PPP conversion and Covid 19 impacts. Available at SSRN: https://ssrn.com/abstract=4011838 (2022).
5.	Leimbach, M., Marcolino, M. & Koch, J. Structural change scenarios within the SSP framework. Futures. (2023)
6.	Crespo Cuaresma, J. et al. Will the Sustainable Development Goals be fulfilled? Assessing present and future global poverty. Palgrave Commun 4, (2018).
7.	Rao, N. D., Sauer, P., Gidden, M. & Riahi, K. Income inequality projections for the Shared Socioeconomic Pathways (SSPs). Futures 105, 27–39 (2019).
8.	Jiang, L. & O’Neill, B. C. Global urbanization projections for the Shared Socioeconomic Pathways. Global Environmental Change 42, 193–199 (2017).
9.	Chen, S. et al. Updating global urbanization projections under the Shared Socioeconomic Pathways. Sci Data 9, (2022).
10.	Benveniste, H., Cuaresma, J. C., Gidden, M. & Muttarak, R. Tracing international migration in projections of income and inequality across the Shared Socioeconomic Pathways. Clim Change 166, (2021).
11.	Andrijevic, M., Crespo Cuaresma, J., Muttarak, R. & Schleussner, C. F. Governance in socioeconomic pathways and its role for future adaptive capacity. Nat Sustain 3, 35–41 (2020).
12.	Soergel, B. et al. A sustainable development pathway for climate action within the UN 2030 Agenda. Nat Clim Chang 11, 656–664 (2021).
13.	KC, S. & Lutz, W. The human core of the shared socioeconomic pathways: Population scenarios by age, sex and level of education for all countries to 2100. Global Environmental Change 42, 181–192 (2017).
14.	Crespo Cuaresma, J. & Lutz, W. The demography of human development and climate change vulnerability: a projection exercise. Vienna Yearb Popul Res 241–261 (2015).
15.	Andrijevic, M., Crespo Cuaresma, J., Lissner, T., Thomas, A. & Schleussner, C. F. Overcoming gender inequality for climate resilient development. Nat Commun 11, 1–8 (2020).
 
