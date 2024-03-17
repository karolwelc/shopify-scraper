# Shopify Products Scraper

This is Shopify products Scraper. The script retrieves data from the products.json file of Shopify shop. 
Then, for each product, it makes an additional query to the 
product page to retrieve data from meta tags.

All scraped information is saved to a CSV file (products.csv)

#### Why is this useful?

Unfortunately, the /products.json endpoint does not contain meta tags. To export all product parameters, it is necessary to query each product directly.

That's why a script was created. To do it automatically!

### 🔥 Installation
```
git clone https://github.com/karolwelc/shopify-scraper.git
cd shopify-products-scraper
pip install -r requirements.txt
```

### 🚀 Usage

```
python scraper.py -t https://www.shopifyshop.com
```

Output:

```
python scraper.py -t https://www.shopifyshop.com
[+] Starting script
[+] Checking products page
 ├ Scraping: https://www.shopifyshop.com/products/nami-nude-corn-outlet
 ├ Scraping: https://www.shopifyshop.com/products/sniegowce-damskie-czarne-boom-snow-boots-black-grape
 ├ Scraping: https://www.shopifyshop.com/products/mini-pouch-mokka-croco
 ├ Scraping: https://www.shopifyshop.com/products/saszetka-etui-na-karty-damskie-mini-pouch-black-ink-croco
 ...
[+] Scraping done
 ```

Script will generate products.csv with this header:
```
Name,URL,Meta Title,Meta Description,Product Description
```

You can use `-v` flag to save Product Variants in separated rows.

```
Name,Variant Name,Price,URL,Meta Title,
```
then script synchronize Variant Name and Price also.
