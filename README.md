# Super Pages Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Super Pages Scraper](https://oxylabs.io/products/scraper-api/web/superpages?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Super-Pages website effortlessly. This brief guide explains how an Super-Pages Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Super Pages results by providing your own URLs to our service. We can return the HTML for any Super Pages page you like.

#### Python code example

The example below illustrates how you can get HTML of Super Pages page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.superpages.com/los-angeles-ca/restaurants'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/super-pages-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta name=\"charset\" content=\"utf-8\"><meta http-equiv=\"X-UA-Com ... </html>",
      "created_at": "2023-12-18 11:11:50",
      "updated_at": "2023-12-18 11:11:52",
      "page": 1,
      "url": "https://www.superpages.com/los-angeles-ca/restaurants",
      "job_id": "7142471515836069889",
      "status_code": 404
    }
  ]
}
```
With our Super Pages Scraper, you can seamlessly pull public data from any Super Pages web page. Harvest the essential restaurant information, such as ratings, customer reviews, or cuisine descriptions, to evaluate the local food scene and stay one step ahead in your culinary adventure. If you have any queries, feel free to reach out to our support team through live chat or drop us an email at hello@oxylabs.io.
