# Activity: Editing Files in Linux

## Instructions

### Issue: Some prices are missing or incorrect in the file: `stock_sample.csv`.

1. Identify the products with an incorrect price.
2. Using the symbols for those products, look for the correct price in the file: `stock2022_09_28.csv`.
3. Using `vi`, edit the `stock_sample.csv` file and add the correct prices for the lines with the wrong price.

#### Steps:
- Open the file with `vi`.
- Navigate to the lines with incorrect prices using the arrow keys.
- Enter insert mode by pressing `i` and correct the prices.
- Exit insert mode by pressing `Esc`.
- Save and quit by typing `:wq`.

### The client would like additional information to be included in the `stock_sample.csv` file.

1. Find the product information from `stock2022_09_28.csv` for TSLA, MSFT, MS.
2. Add this information to the `stock_sample.csv` file.
3. The client asks that the new data be added starting line 4. Anything from lines 4 to 10 should be moved down.
4. To ensure you're on target, display the line numbers in your `vi` tab.

#### Steps:
- Open the file with `vi`.
- Navigate to the location where the new data should be added using the arrow keys.
- Enter insert mode by pressing `i` and add the new data.
- Exit insert mode by pressing `Esc`.
- Move existing lines down as necessary using `dd` to cut and `p` to paste below.
- Display line numbers by typing `:set nu`.
- Save and quit by typing `:wq`.

### Big news: The New York Stock Exchange has just been bought by Wiley and is now the Wiley US Stock Exchange.

1. The client is requesting our help to change some information in bulk, as we displayed some skills using `vi`.
2. Use `vi` to edit the file `sample_stock.csv`.
3. Use the search tool in `vi` to search for "New York Stock Exchange."
4. Use the `substitute (s)` command within `vi` to search and replace the occurrences of "New York Stock Exchange" with "Wiley US Stock Exchange."
5. Save and quit your file.

#### Steps:
- Open the file with `vi`.
- Enter command mode by pressing `Esc` (if not already in command mode).
- Use the search and replace command `:%s/New York Stock Exchange/Wiley US Stock Exchange/g`.
- Save and quit by typing `:wq`.

