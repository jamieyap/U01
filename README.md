# 0 About the Por Nuestra Salud Study

The Por Nuestra Salud (PNS) study examines intrapersonal and contextual determinants of smoking cessation among Spanish-speaking Mexican American smokers attempting to quit.

# 1 About this Repository

This repository contains code for performing data curation of intensive longitudinal data from the Por Nuestra Salud study (PNS) and documentation. Files corresponding to particular stages of the project are placed under the relevant header.


# 2 Essential

| <img height=0 width=500> File Name <img height=0 width=500> | <img height=0 width=900> Brief Description <img height=0 width=900> |
|:-----------------------------|:-----------------------------------------------------------|
| [PNS_documentation.pdf](https://github.com/jamieyap/MARS/blob/master/PNS_documentation.pdf) | Documents data curation |
| Files within [scripts-analysis](https://github.com/jamieyap/PNS/tree/master/scripts-analysis) | Provides sample R code demonstrating the use of the curated datasets in analysis |


# 3 More Details

## 3.1 Data Curation

| <img height=0 width=500> File Name <img height=0 width=500> | <img height=0 width=900> Brief Description <img height=0 width=900> |
|:-----------------------------|:-----------------------------------------------------------|
| [calc-quit-dates.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/calc-quit-dates.R) | Create a file containing time variables to anchor data analysis: Quit Time, Begin Study Time, and End of Study Time |
| [get-ema-item-names.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/get-ema-item-names.R) | In preparation of merging data corresponding to each EMA type into one file, create new variable names with similar format, e.g., postquit.random.item.XX, and a dictionary mapping the correspondence of original item names and item names in the new format |
| [get-ema-item-responses.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/get-ema-item-responses.R) | Perform data preparation tasks and save intermediate results for further data preprocessing. Data preparation tasks in this script include: 1. exclude EMAs with some indication of unsuccessful delivery, 2. constuct variables for time when EMA was delivered, begun, completed, 3. construct variable indicating whether a response to any item was recorded |
| [identify-smoking-vars.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/identify-smoking-vars.R) | Identify variables in various EMA types which provide information on counts of cigarettes smoked and timing of smoking episode |
| [rules-smoking-quantity.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/rules-smoking-quantity.R) | Apply decision rules to construct a variable capturing counts of cigarettes smoked |
| [rules-smoking-indicator.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/rules-smoking-indicator.R) | Apply decision rules used to construct variable capturing whether any cigarettes were smoked |
| [get-smoking-vars.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/get-smoking-vars.R) | Complete preparaton of smoking-related variables, particularly time variables related to the smoking outcome and save output to individual csv file |
| [get-ema-data-frames-by-type.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/get-ema-data-frames-by-type.R) | Complete preparaton for each type of EMA. Once preparation for each individual type of EMA is complete, save output to individual csv files. |
| [merge-all.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/merge-all.R) | Merge smoking outcome constructed in [get-smoking-vars.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/get-smoking-vars.R) with curated data from all types of EMA into one file |


## 3.2 Checks on Input and Output Data

| <img height=0 width=500> File Name <img height=0 width=500> | <img height=0 width=900> Brief Description <img height=0 width=900> |
|:-----------------------------|:-----------------------------------------------------------|
| [calc-candidate-dates.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/calc-candidate-dates.R) | Get timestamp of earliest Post-Quit EMA and merge dates from multiple sources into one file |
| [smoking-plots.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/smoking-plots.R) | Visualize reported number of cigarettes smoked with respect to days elapsed since timestamp of earliest Post-Quit EMA calculated in [calc-candidate-dates.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/calc-candidate-dates.R) |
| [zoomed-smoking-plots.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/zoomed-smoking-plots.R) | Zoom in on specific time frames |

## 3.3 Scripts Collecting Functions

| <img height=0 width=500> File Name <img height=0 width=500> | <img height=0 width=900> Brief Description <img height=0 width=900> |
|:-----------------------------|:-----------------------------------------------------------|
| [shared-data-manip-utils.R](https://github.com/jamieyap/MARS/blob/master/scripts-shared/shared-data-manip-utils.R) | Contains functions to perform data manipulation tasks and can be utilized in other studies |
| [data-manip-utils.R](https://github.com/jamieyap/MARS/blob/master/scripts-studies/data-manip-utils.R) | Contains functions to perform data manipulation tasks specific to the PNS study |


