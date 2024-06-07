# Efficiently Scraping Steam Game Reviews with Python: A Comprehensive Guide

This is the folder for the medium article "Efficiently Scraping Steam Game Reviews with Python: A Comprehensive Guide".

## Usage

1. Install *requests* package using *pip* or *conda*
2. Run all cells in "Scrape Reviews" section in *steam-review-scraper.ipynb*. Change the `appid` and the name of the game respectively in the cell as below. Change the `params` for other customization.

    ```python
    review_appname = "ELDEN RING"           # the game name
    review_appid = 1245620                  # the game appid on Steam

    # the params of the API
    params = {
            'json':1,
            'language': 'english',
            'cursor': '*',                  # set the cursor to retrieve reviews from a specific "page"
            'num_per_page': 100,
            'filter': 'recent'
    }
    ```

    Change the time range of the reviews to be scraped in the region below

    ```python
    time_interval = timedelta(hours=24)                         # the time interval to get the reviews
    # end_time = datetime.fromtimestamp(1716718910)               # the timestamp in the return result are unix timestamp (GMT+0)
    end_time = datetime.now()
    # start_time = end_time - time_interval
    start_time = datetime(2024, 1, 1, 0, 0, 0)
    ```

    The scraped reviews are stored with structure as following. A run of the code produces a .pkl file.

    ```bash
    |-- {appid}_{appname}
    |   |-- {appid}_{appname}_reviews_yyyymmdd-hhmmss_yyyymmdd-hhmmss.pkl
    ```

3. To read the scraped comments, please refer to the "Read a review pickle object" section of file *steam-review-scraper.ipynb*

