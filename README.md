# plane-acquisition-data

**This repository looks at the risks of aircrafts to determine which aircraft the company should purchase.**

Company x is looking to diversify its portfolio by venturing into the aviation industry and have tasked me with determining which aircraft has the lowest risk.The objective is to analyze accident data from the National Transportation Safety Board and make data proven recommendations on the aircrafts to purchase.The dataset contained civil aviation accident and selected incidents in the United States and international waters.I first had to filter the data into the relevant categories before aggregating and visualizing it.The results yielded a list of various aircrafts that i will recommend to the aviation division of the company.

##INTRODUCTION

The dataset contains information about various aspects of the accident like accident date,fatalities and injuries,location,weather conditions etc.
The objective was to filter the data into its distinct categories and make certain analysis.

##DATA UNDERSTANDING AND ANALYSIS

I filtered the data into its distinct categories and visualized the data in the juputer Notebook(plane.ipynb) and the tableau interactive dashboard linked below.

https://public.tableau.com/app/profile/john.thiongo/viz/accidentdatatodetermineplaneacquisition/ACCIDENTDATA

**1.Event Date**

I plotted an area chart in the dashboard of the total fatal and total injuries data over the years .
The chart showed that the number of fatalities was constant with rises and falls while the number of injuries fell sharply in the 2000s.

**2.Location**

The location column of the dataset containing countries was highlighted on a map on the dashboard.

**3.Weather condition**

The weather conditions at the time of the accidents was recordes under three main categories:
  1.VMC - Visual meteorological conditions
  The weather conditions were good enough to fly by visual reference.
  2.IMC - Instrument meteorological conditions
  The weather was below the minimums required for flying by visual reference.
  3.UNK - Unknown 
  The weather conditions were not recorded.
The packed bubbles on the dashboard indicating weather conditions show a larger bubble in good conditions as compared to bad.

**4.Aircraft Craft Category**

I further filtered the entire dataset to contain only airplanes as the other categories of aircraft were not suited fot the companies goals .
``
df=df[df['Aircraft Category'].str.strip()=='Airplane']
``
**5.Engine type**

The type of engine in an aircraft is very important.
The document attached highlights the advantages and disadvantages of the various engine types.

**6.Make and Model**

I filtered the models of the planes by their count and then plot a bar graph showcasing models against number of accidents.

**7.Injury Severity and Aircraft Damage**

A bar graph of injury severity against aircraft damage indicates a high number of injuries even with substantial damage to the aircraft

##Recommendations

I would recommend the plane models that appear on the last cell of the jupyter notebook as they have the least number of accidents.

 which models have the least accidents
``
df['Model'].value_counts().sort_values(ascending=True).head(10).index.tolist()
``
