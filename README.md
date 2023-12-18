# Justdial Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Justdial Scraper](https://oxylabs.io/products/scraper-api/web/justdial?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Justdial website effortlessly. This brief guide explains how an Justdial Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Justdial results by providing your own URLs to our service. We can return the HTML for any Justdial page you like.

#### Python code example

The example below illustrates how you can get HTML of Justdial page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.justdial.com/mumbai/search-engine/nct-10425490'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/justdial-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\" class=\"jsx-e751385d4d0f7ab3\"/><link rel=\" ... </html>",
      "created_at": "2023-12-18 11:08:51",
      "updated_at": "2023-12-18 11:09:17",
      "page": 1,
      "url": "https://www.justdial.com/mumbai/search-engine/nct-10425490",
      "job_id": "7142470766339067905",
      "status_code": 200
    }
  ]
}
```
With our Justdial Scraper, you can seamlessly extract public data from any Justdial web page. Gather the relevant restaurant information, such as location, ratings, or cuisine details, to understand the food industry and stay ahead of your competitors. If you have any inquiries, reach out to our support team through live chat or email us at hello@oxylabs.io.