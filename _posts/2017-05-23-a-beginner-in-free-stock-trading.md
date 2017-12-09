---
layout: post
title:  "A beginner in free stock trading"
date:   2017-05-23 10:00:38 -0500
categories: econ'

---

With new trading platforms and applications truly democratizing the power to buy and sell stocks, there are plentiful interesting and affordable ways to get involved with the stock market. A particulary cool application called [RobinHood](https://www.robinhood.com/) emerged that allowed one to buy and sell stocks without commision, and so I decided to get involved. As a complete beginner with only an Econ 101 exposure to markets and practically zero understanding of finance, I decided to compile some notes about stock trading in general, because I felt there was a shortage of concise, easy information for a complete beginner. The fact of the matter is entire books/bookshelves have been filled with information about investments, but here's a few cents and trading tips for a new investor using a buy and sell platform like RobinHood.
Eventually, I sought to create some Jupyter notebooks that enabled me to get some quick price data analysis information on the stocks that I owned, which are essentially Python scripts into which I imported stock prices using the Yahoo Finance Python module (there are plenty of stock market API's you can use, [Oanda](https://www.oanda.com/), [Quandl](https://www.quandl.com/), etc.) The notebook can be found [here](https://github.com/shamikh-mill/stock-checker/blob/master/price-checker.ipynb).  

Disclaimer- as a complete beginner on a learning experience, some of these strategies can be outright incorrect, in which case I'd love to be informed of and learn the real way to do things. 

- From Investopedia: Stocks are shares in the ownership of a company, and represent a claim on a company's assets and earnings. But it's important to understand that stockholders (or shareholders) don't own the company itself, instead simply the shares of earnings/assets issued by the companies.  
- Portfolio - grouping of financial assets, your shares. 
- Bullish stocks - characterized by rising share prices. 
- Bearish stocks - characterized by falling share prices.  
- You, as the investor, seek to minimize your losses (the total fall in price of your portfolio) and to maximize your return, the gains in price. RobinHood will show you your average cost for your shares for each stock and the total return on that stock, both of which are important to keep track of. 
- The Intuition: Buy stocks at the absolute low, and sell at at the absolute high. (only occurs if you're lucky)
- In the perfect world, you buy a stock when it is bullish and yet at a very low price, perhaps near its 52-week low, and sell a stock when it is very high and bearish. In practice, very few investors are able to achieve this. 

RobinHood allows you to buy and sell stocks on the open market without paying a fee. To be able to trade, you have to register an account using your social security number and wait a few days for approval.  
The app's interface is intuitive and self-explanatory. You can add stocks to your watchlist, and view a graph of its price per share in time periods from a day to five years. It's easy to see using these why FANG stocks (Facebook, Apple, Netflix, and Google) are some of the most high-performing stocks tech stocks- looking back a few years, we see steady, linear increases in their values.

1. Buying- Probably the part of investment that gets the most attention, just because the price you buy at singlehandedly determines whether or not you have an actual return. There is a whole mini-world of analysts who look at so, so many factors both inside companies and in the aggregate economy to try and find the most auspicious shares, the ones that minimize risk and maximize return. Financial advising and investment banking are basically all about that. As a humble stock trader from your phone, how do you know when to buy?  
To determine which stocks to buy, I simply keep an ear out for companies that are doing well- releasing new products soon, etc. It's also important to guage public opinion on these matters. For example, when United Airlines got themselves into the Dr. Dao controversy and took enormous criticism, their stock ($UAL) took a 4% hit (from about $72 to about $68, which is a huge deal) and the company lost millions of dollars.  
But to bring in a more rigorous aspect to buying (or selling for that matter) it's important to check out analyst reviews for stocks. Some great websites for this would be [Barchart.com](https://Barchart.com), [marketwatch.com](https://marketwatch.com), and [stocktwits.com](https://stocktwits.com). Ratings are provided for each stock which advise to overweight (buy more), underweight (sell some), hold (keep your shares). When a stock is marked as overweight, it is expected to "outperform its industry in the market"- from Investopedia this can be "due to a steady stream of positive news, good earnings and raised guidance." In general, these are stocks you'd want to have. 
2. Holding- Dealing in stocks can require a frustrating amount of patience. Sometimes it can be better to hold than to sell your shares even if a stock is bearish; plentiful ratings from online services evidence this.  
3. Selling- important, because while buying can set you up for profit, it's not ensured until you actually sell. It's often hard to sell (bullish stocks) because mentally you want its share price to perhaps continue its upward trend, making you more money, but as outlined in "The Casino Trade" on Investopedia this can often lead to a frustrating loss when you wait too long and eventually just sell off shares at much lower prices than what once was. You can use the websites above for advice on selling as well, of course. Some things to watch for: 
- Sell stocks if they suddenly increase in price, over a very short period. It's best to sell in this scenario because the share can be back down just as fast. 
- Sell stocks when the company seems to be losing to competitors over a long period of time. 

At the end of the day, be sure to keep from selling or buying solely based on emotion or impatience on instead on analyst opinion and real trends. Investopedia explains the more rigorous methodology for buying and selling much better than I: 
[When to buy, sell or hold stocks](http://www.investopedia.com/articles/financialcareers/06/snapdecisions.asp?ad=dirN&qo=investopediaSiteSearch&qsrc=0&o=40186)  
[When to sell stocks](http://www.investopedia.com/articles/stocks/10/when-to-sell-stocks.asp)  


Other RobinHood things:  
- Dividends- Sometimes companies pay out a sum of its earnings to its shareholders. Always good! 
- Check the "History" page in the app to keep track of your transactions (most importantly, the price at which you purchased).  

Happy trading! 



