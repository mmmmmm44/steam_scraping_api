# Unlocking Steam's API to Track Trending Games

This is the folder for the medium article "Unlocking Steam's API to Track Trending Games".

## Usage

1. Install *requests* package using *pip* or *conda*
2. Run *steam-category-scraper.ipynb*. It will create a folder namely *search_results_{yyyymmdd}* which *yyyymmdd* is the date of running the scraper. It has the following file structure, for instance.

    ```bash
    |-- search_results_20240528
    |   |-- globaltopsellers_20240528.pkl
    |   |-- popularcommingsoon_20240528.pkl
    |   |-- popularnew_20240528.pkl
    |   |-- specials_20240528.pkl
    |   |-- topsellers_20240528.pkl
    ```

    Each pickle file corresponds to a category shown in Steam's front page.

3. To read the results, please refer to the *Read search results of a particular date* in the same jupyter notebook.
