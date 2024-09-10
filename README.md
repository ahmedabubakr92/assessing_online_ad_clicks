# Assessing Online Ad Clicks for Significance

## Project Overview

This project analyzes the impact of different ad text colors on click-through rates for Fred’s burger bistro in Brisbane. Fred ran an online advertising campaign where 30 different text colors were tested over a month to determine if any color outperformed blue in generating clicks. Using statistical analysis, particularly permutation tests, this project explores whether any color leads to a significantly higher click-through rate.

## Problem Statement

Fred, the owner of a burger bistro, wants to increase his customer base by optimizing the performance of his online ads. His goal is to determine if any ad text color generates more clicks than the blue ads he’s been using. Over a month, Fred tested 30 different colors, and this project analyzes the resulting data to identify statistically significant differences in click-through rates.

## Data Description

The dataset consists of 30 rows, each representing a different color, and 41 columns, tracking daily click and view counts over 20 weekdays. Each color received 100 daily views. The dataset is structured as follows:

	•	**Color**: The text color used in the ad.
	•	**Click Count: Day 1** - Day 20: The number of times an ad of a specific color was clicked on each day.
	•	**View Count: Day 1 - Day 20**: The number of times an ad was viewed (consistently 100 views per day).

## Key Steps and Analysis

	1.	Data Cleaning:
	•	Redundant “View Count” columns were removed, as all view counts were consistently 100.
	•	The dataset was cleaned to focus on click counts for each color.
	2.	Permutation Testing:
	•	A permutation test was conducted to compare the click-through rates of blue against the other 29 colors. The test determines whether the observed differences in click rates are statistically significant.
	3.	Bonferroni Correction:
	•	To account for multiple comparisons, the Bonferroni correction was applied, adjusting the significance level to 0.05 / 29 = 0.00172, ensuring we avoid false positives.
	4.	Visualization:
	•	P-values from the permutation tests were visualized using a heatmap, highlighting any significant differences between colors and blue.

Results

	•	Ultramarine emerged as a potentially better-performing color, with a higher click-through rate compared to blue. However, after applying the Bonferroni correction, its p-value of 0.0034 was not statistically significant.
	•	The project concludes that Fred may consider replacing blue with ultramarine, but further testing is recommended to confirm its effectiveness.

Conclusion

While no statistically significant results were found after adjusting for multiple comparisons, ultramarine showed promise as a viable alternative to blue. The project highlights the importance of focusing on meaningful comparisons, as testing too many variables can introduce unnecessary uncertainty.

Next Steps

Fred can:

	1.	Conduct a focused experiment comparing only blue and ultramarine to verify the results.
	2.	Use the insights from this analysis to optimize future advertising strategies and increase click-through rates.

Technologies and Tools Used

	•	**Python**: For data analysis and statistical testing.
	•	**Pandas**: For data manipulation and cleaning.
	•	**NumPy**: For numerical computations and permutation testing.
	•	**Matplotlib** & **Seaborn**: For data visualization, including heatmaps.
	•	**Chardet**: For detecting the encoding of the CSV data file.
