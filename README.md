# Text-Mining-The-New-York-Times-Articles

The set of functions return the over time frequency of occurrence of the words in the dictionary for the collection of articles tagged as being geolocated in a specific country, as they might be potential indicators of the topic or sentiment expressed in the article's texts. Note that the idea is not to filter out articles by searching on the article's body, headline and byline for a particular term, but to mine text from all articles indistinctively of their content.

· Before jumping directly to the code and check how to use the repository's functions [here](https://github.com/nilmolne/Text-Mining-The-New-York-Times-Articles/blob/master/Code/HowToUse.ipynb), make sure to check the **constraints** section [below](https://github.com/nilmolne/Text-Mining-The-New-York-Times-Articles/blob/master/README.md#considerations-and-constraints).

· The project was initially built to demonstrate the value economists may gain from a more conscious application of text mining techniques. If you ever wonder how can it be used in the field of economics, check out a simple but relevant example [here](https://github.com/nilmolne/Text-Mining-The-New-York-Times-Articles/tree/master/Example%20in%20Economics#application-example-in-economics).

· Don't forget to check the NYT API Terms of Service [here](https://developer.nytimes.com/tou), particularly if you are planning to use their articles for more than a learning exercise.

## Considerations and Constraints

1. The frequency of occurrence of the words in the dictionary is presented on a monthly basis even though the articles are published on a given day. Hence, the results of the text mining process are expressed in this form:
  
  * All calculated frequencies of occurrence for each article within a month, for all months analyzed, are summed to give a monthly added frequency of occurrence which is later normalized by the amount of published articles in that given month.
 

2. Best when used for NYT foreign news articles:

  * The API allows only for 101 pages of articles of any kind for a given date. Being an American journal, the amount of articles tagged as 'local' often exceeds the pages allowed. Hence, the results lack consistency since the amount of articles left unexplored remain unknown. 
  
  * Bear in mind that when looking for all news articles published and not filtering for a particular term, the amount of articles returned by the API increase considerably. Now, if you need to approach the construction of the article corpus differently, make sure to review the *get_articles_url(...)* function.


3. Time resolution of the results:

  * As pointed out on the first consideration, the frequency of occurrence of the words in the dictionary is presented and normalized on a monthly basis. However, feel free to adjust your resolution of interest by tuning the functions *get_monthly_results(...)* and *visualize_results(...)*.
