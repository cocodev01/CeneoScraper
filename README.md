# CeneoScraper

## CSS selectors of the opinions' components in [Ceneo.pl](https://www.ceneo.pl/) service

|Components|Variable/Dictionary key|Data type|Selector|
| :- | :- | :- | :- |
|Opinion|opinion/single\_opinion|tag, dictionary|`div.js\_product-review`|
|Opinion ID|opinion\_id|string|`data-entry-id"`|
|Opinion’s author|author|string|`span.user-post__author-name`|
|Author’s recommendation|recommendation|bool|`span.user-post__author-recomendation > em`|
|Score expressed in number of stars|score|float|`span.user-post__score-count`|
|Opinion’s content|description|string|`div.user-post__text`|
|List of product advantages|pros|string|`div.review-feature__col:has( > div.review-feature__title--positives) > div.review-feature__item`|
|List of product disadvantages|cons|string|`div.review-feature__col:has( > div.review-feature__title--negatives) > div.review-feature__item`|
|How many users think that opinion was helpful|like|int|<p>`button.vote-yes["data-total-vote"]`</p><p>`button.vote-yes > span`</p><p>`span[id^=votes-yes]`</p>|
|How many users think that opinion was unhelpful|dislike|int|<p>`button.vote-no["data-total-vote"]`</p><p>`button.vote-no > span`</p><p>`span[id^=votes-no]`</p>|
|Publishing date|publish\_date|string|`span.user-post__published > time:nth-child(1) ["datetime"]`|
|Purchase date|purchase\_date|string|`span.user-post__published > time:nth-child(2) ["datetime"]`|

## Python libraries used in this project
1. Requests
2. BeautifulSoup
3. Json
4. Os
5. Translate
6. Numpy