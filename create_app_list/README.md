# Scraping information of all games from Steam with Python

This is the folder for the medium article "Scraping information of all games from Steam with Python".

## Usage

1. Install *requests* package using *pip* or *conda*
2. Run *steam-applist-scraper.py*. It will create a folder namely *checkpoints* with the following file structure

    ```bash
    |-- checkpoints
    |   |-- apps_dict-ckpt-fin.p
    |   |-- error_apps_list-ckpt-fin.p
    |   |-- excluded_apps_list-ckpt-fin.p
    ```

    |File|Description|
    |---|---|
    |apps_dict-ckpt-fin.p|It stores the information of games.|
    |error_apps_list-ckpt-fin.p|It stores a list of appid which returns error status code.|
    |excluded_apps_list-ckpt-fin.p|It stores a list of appid which cannot be accessed. (i.e. successful respond status code yet no information)|

3. To read the checkpoints, please refer to *read-steam-applist.ipynb* and run the jupyter notebook.
