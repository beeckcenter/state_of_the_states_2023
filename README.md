# State of the States 2023 Text Analysis
Each year, the “State of the State'' speech is a governor’s prime opportunity to outline their top priorities to the public.
[The Beeck Center for Social Impact + Innovation]() analyzed all 50 2023 State of the State addresses (or the equivalent annual budget address or inaugural speech) and dove deeper into governor’s priorities by analyzing a year’s worth of press releases for the 13 states that have participated in our [Data Labs](https://beeckcenter.georgetown.edu/projects/data-labs/) program. This GitHub repo includes the code used to collect the data and conduct text analysis. 
 
Haven't read the blog yet? Check out our write-up of this research [here](https://beeckcenter.georgetown.edu/the-state-of-the-states-what-governors-across-the-us-prioritized-in-2023/). 

## Our Methodology
To enhance our understanding of these speeches and press releases, we harnessed the power of statistics using Python to identify frequent terms and topics from a large amount of documents. 

First, this involved scraping the annual State of the State address for all 50 states and an average of 279 press releases from 13 state governor websites. 

Next, we converted the text into numerical data with a [Term Frequency - Inverse Document Frequency (TF-IDF)](https://www.learndatasci.com/glossary/tf-idf-term-frequency-inverse-document-frequency/) matrix. 

Finally, we used the unsupervised machine learning technique [Principal Components Analysis (PCA)](https://builtin.com/data-science/step-step-explanation-principal-component-analysis) to identify underlying patterns in the large dataset and group terms into larger principle components, which we then interpreted as key policy priorities. 

## Data Collection: Scraping PDFs and Websites\*

###  State of the State Address
To gather the text for all State of the State speeches (or the equivalent inaugural or budget address), we scraped a combination of PDFs and individual websites using both the `BeautifulSoup` and `Selenium` packages. See the scripts below.
- [Scraping PDFs](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_sos_addresses/scraping_sos_pdfs.ipynb)
- [Scraping Websites](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/01_data_collection/scraping_sos_addresses/scraping_sos_websites_public.ipynb)

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

\**This process included a manual review of each website's robots.txt file to review any restrictions.*

## Data Analysis

- [Analysis of the State of the State Addresses](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/02_data_analysis/02_analysis_sos.ipynb) <br>
    <ul>
      <li> Preprocessing (addressing outliers, removing custom stop words, hyperparameter tuning, etc.) </li>
      <li> Creating the Term Frequency - Inverse Document Frequency (TF-IDF) matrix </li>
      <li> Principal Components Analysis (PCA) of full dataset and subsets by political party (i.e. Democrat and Republican) </li>
      <li> Frequent term analysis by political party </li></ul>
- [Analysis of Press Releases](https://github.com/beeckcenter/state_of_the_states_2023/blob/main/02_data_analysis/02_analysis_press_releases.ipynb) <br>
    <ul>
        <li> Preprocessing (addressing outliers, removing custom stop words, hyperparameter tuning, etc.) </li>
        <li> Creating a Term Frequency - Inverse Document Frequency (TF-IDF) matrix for each state </li>
        <li> Principal Components Analysis (PCA) of each state dataset </li>
    </ul>

