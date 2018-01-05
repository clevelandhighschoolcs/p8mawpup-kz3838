# tweet Scraper
This was made for my IB Computer Science Class
# To setup my web scraping have all the following:

- [ ] install notepad++ (if not already installed)
- [ ] install [python version 2.7.14](https://www.python.org/downloads/) (if not already installed)
- [ ] setup your virtual enviroment
- [ ] Download the code 

Once you have the code downloaded put it into a blank notepad++. Make sure to install the BeautifulSoup liberary in your virtual enviroment. Type this into your cms to install it. 

```CMD
  pip install bs4
```

# how to run the program 
Now all you gotta do is type in the virtual enviroment:

```CMD
  python (yourfilenamehere).py 
```

# I got my information from http://www.pythonforbeginners.com/python-on-the-web/web-scraping-with-beautifulsoup/
Code below:


from bs4 import BeautifulSoup

import requests

url = raw_input(//*[@id="stream-item-tweet-932220338808770560"]/div[1]/div[2]/div[3]/div)

r = requests.get("http://"+url)

data = r.text

soup = BeautifulSoup(data)

for link in soup.find_all('a'):
	print(link.get('href'))
