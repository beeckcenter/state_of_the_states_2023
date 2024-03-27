# State of the States 2023 Text Analysis
The GitHub repo for text analysis of the 2023 State of the State addresses and press releases for 13 states. Haven't read the blog yet? Check out our write-up of this research [here](). 

## 1. Data Collection: Webscraping\*

###  State of the State Address

### Press Releases
See the scripts below for the webscraping code for press releases on each state's website. 
- [Arizona](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/arizona_scraping_public.ipynb)
- [California](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/california_scraping_public.ipynb)
- [Colorado](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/colorado_scraping_public.ipynb)
- [Connecticut](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/connecticut_scraping_public.ipynb)
- [Idaho](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/idaho_scraping_public.ipynb)
- [Illinois](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/illinois_scraping_public.ipynb)
- [Minnesota](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/minnesota_scraping_public.ipynb)
- [Nevada](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/nevada_scraping_public.ipynb)
- [Ohio](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/ohio_scraping_public.ipynb)
- [Oregon](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/oregon_scraping_public.ipynb)
- [Utah](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/utah_scraping_public.ipynb)
- [West Virginia](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/west_virginia_scraping_public.ipynb)
- [Wisconsin](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_press_releases/wisconsin_scraping_public.ipynb)

## 2. Data Analysis

- **[Analysis of the State of the State Addresses](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/02_data_analysis/02_analysis_sos.ipynb)** <br>
    <ul>
      <li> Preprocessing (addressing outliers, removing custom stop words, hyperparameter tuning, etc.) </li>
      <li> Creating the Term Frequency - Inverse Document Frequency (TF-IDF) matrix </li>
      <li> Principal Components Analysis (PCA) of full dataset and subsets by political party (i.e. Democrat and Republican) </li>
      <li> Regex search extraction of terms related to data and climate </li></ul>
- **[Analysis of Press Releases](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/02_data_analysis/02_analysis_press_releases.ipynb)**

\**This process included a manual review of the robots.txt file to review any restrictions.*

